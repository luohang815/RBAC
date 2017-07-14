# RBAC权限控制
用户-----角色-----权限 用户和权限间接相连（将用户分配角色  权限分配给角色）

                                      RBAC模块功能
                                      
           用户管理                       角色管理                     权限管理
         1、用户列表                     1、角色列表                  1、权限列表
         2、添加用户                     2、添加角色                  2、添加权限
         3、编辑用户                     3、编辑角色                  3、编辑权限
         4、设置角色                     4、设置权限
        
        权限控制流程
        1、访问客户列表
        2、检验权限
        3、反馈（1.有权限 2.无权限）
        
        数据库设计(user)
        1、用户
            id
            name
            email
            is_admin
            status
            updated_time
            created_time
        2、角色(role)
            id
            name
            statues
            updated_time
            created_time
        3、用户角色关系(user_role)
            id
            uid
            role_id
            created_time
        4、权限(access)
             id
             title (页面标题)
             urls(页面地址)
             statues
             updated_time
             created_time
        5、角色权限关系(role_access)
            id
            role_id
            access_id
            created_time
