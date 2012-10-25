xcode
=====- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions
{
    self.window = [[UIWindow alloc] initWithFrame:[[UIScreen mainScreen] bounds]];
    // Override point for customization after application launch.
    
    UIViewController *viewController1 = [[PaperTrailFirstViewController alloc] initWithNibName:@"PaperTrailFirstViewController" bundle:nil];
    UIViewController *viewController2 = [[PaperTrailSecondViewController alloc] initWithNibName:@"PaperTrailSecondViewController" bundle:nil];   
    UIViewController *viewController3 = [[PaperTrailThirdViewController alloc] initWithNibName:@"PaperTrailThirdViewController" bundle:nil]; 
    UIViewController *viewController4 = [[PaperTrailFourthViewController alloc] initWithNibName:@"PaperTrailFourthViewController" bundle:nil];
    UIViewController *viewController5 = [[PaperTrailFifthViewController alloc] initWithNibName:@"PaperTrailFifthViewController" bundle:nil];    
    self.tabBarController = [[UITabBarController alloc] init];
    self.tabBarController.viewControllers = [NSArray arrayWithObjects:viewController1,viewController2,viewController3,viewController4,viewController5, nil];
       
      self.window.rootViewController = self.tabBarController;  
    [window addSubview:self.navBarController.view];
    [self.window makeKeyAndVisible];
    return YES;
}