platform :ios, '6.0'
pod 'DTCoreText', '~> 1.6.11'
pod 'AFNetworking', '1.3.3'
pod 'SBJson', '~> 4.0.1'
pod 'BlocksKit', '~> 2.2.0'
pod 'CocoaLumberjack', '~> 1.7.0'
pod 'VKFoundation', :git => "https://github.com/viki-org/VKFoundation.git"
pod 'CocoaHTTPServer'

target 'VKVideoPlayerTests' do
  pod 'Specta',      '~> 0.2.1'
  pod 'Expecta',     '~> 0.3.0'
  pod 'OCMock',      '~> 2.2.1'
  pod 'CocoaHTTPServer'
end

# Remove 64-bit build architecture from Pods targets
post_install do |installer|
  installer.project.targets.each do |target|
    target.build_configurations.each do |configuration|
      target.build_settings(configuration.name)['ARCHS'] = '$(ARCHS_STANDARD_32_BIT)'
    end
  end
end

