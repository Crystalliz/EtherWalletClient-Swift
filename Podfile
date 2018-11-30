# Uncomment the next line to define a global platform for your project
source 'https://github.com/CocoaPods/Specs.git'
platform :ios, '12.0'

def installationSettings
    use_frameworks!
    inhibit_all_warnings!
end

def commonPods
    pod 'Fabric', '1.9.0'
    pod 'Crashlytics', '3.12.0'
    pod 'SwiftGen', '6.0.2'
    pod 'Alamofire', '4.8.0'
    pod 'KeychainAccess', '3.1.2'
    pod 'RxSwift', '4.4.0'
    pod 'RxCocoa', '4.4.0'
    pod 'Swinject', '2.5.0'
end

target 'EtherWallet' do
    installationSettings
    commonPods
end

post_install do |installer|
    installer.pods_project.targets.each do |target|
        target.build_configurations.each do |config|
            config.build_settings['SWIFT_VERSION'] = '4.0'
        end
    end

    installer.pods_project.build_configurations.each do |config|
        config.build_settings['PROVISIONING_PROFILE_SPECIFIER'] = ''
    end
end
