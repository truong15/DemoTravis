source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '10.0'
inhibit_all_warnings!
use_frameworks!
install! 'cocoapods', :deterministic_uuids => false

workspace 'DemoTravis.xcworkspace'

target 'DemoTravis' do
    project 'DemoTravis'
    pod 'MVVM-Swift' # MVVM Architect for iOS Application.
    pod 'IQKeyboardManagerSwift','6.2.1'
    # Data
    pod 'ObjectMapper' # Simple JSON Object mapping written in Swift. Please fix this version to 2.2.6 now.

    # Network
    pod 'Alamofire', '4.8.2' # Elegant HTTP Networking in Swift.
    pod 'AlamofireNetworkActivityIndicator', '2.3.0' # Controls the visibility of the network activity indicator on iOS using Alamofire.

    # Utils
    pod 'SwiftLint'
    pod 'SwifterSwift', '4.6.0'
    pod 'SwiftyUserDefaults'
    pod 'NVActivityIndicatorView', '4.6.1'
    pod 'AsyncSwift', '2.0.4'
    pod 'FMDB','2.7.5'
    pod 'LGSideMenuController'
    pod 'R.swift'
    pod 'LGButton'
#    pod 'SpreadButton'
#    pod 'WCLShineButton'
    pod 'CircleMenu'

    post_install do |installer|
        installer.pods_project.targets.each do |target|
            target.build_configurations.each do |config|
                if config.name == 'Release'
                    config.build_settings['SWIFT_OPTIMIZATION_LEVEL'] = '-Owholemodule'
                end
            end
        end
    end
end
