# router-defined


/       Home
/product/:id    商品详情页面


/category       类别页面

/cart           购物车
/checkout       结算页面

    router.route('/payments').get(router.action('payments'))
    router.route('/new-card').get(router.action('new-card'))

/user           用户页面
/user/account   用户详情
/user/orders    用户订单
/user/addresses 用户地址列表
/user/credit-cards 用户银行卡列表

/login        登录页面
/signup       注册页面
/forget       忘记密码

    router.route('/list').get(router.action('list'))
    
    router.route('/orders/:number').get(router.action('order'))

    

    router.route('/complete/cash').get(router.action('checkout/complete').cash)
    router.route('/complete/stripe').get(router.action('checkout/complete').stripe)
    router.route('/complete/transfer').get(router.action('checkout/complete').transfer)

    router.route('/orders/:number/addresses').get(router.action('checkout/addresses'))

    /**
     * Login
     */
    router.route('/login').get(router.action('login/index'))
    router.route('/signup').get(router.action('login/signup'))
    router.route('/login/forget').get(router.action('login/forget'))

    router.route('/reset-password').get(router.action('reset-password'))

    router.route('/address/list').get(router.action('address').list)
    router.route('/address/new').get(router.action('address/new'))
    router.route('/address/:addressID/edit').get(router.action('address').edit)

    router.route('/uc').get(router.action('uc'))

    /**
     * Order
     */

    router.route('/order/:number').get(router.action('order'))

    /**
     * User
     */
    router.route('/user').get(router.action('user'))
    router.route('/user/account').get(router.action('user/account'))
    router.route('/user/orders').get(router.action('user/orders'))
    router.route('/user/addresses').get(router.action('user/addresses'))
    router.route('/user/credit-cards').get(router.action('user/credit-cards'))
