# Cocos2d-x-ipa

需手动编译
#参考命令

#source ~/.bash_profile || true
axmol new -p dev.chenx.hellolua -d lua-tests -l lua --portrait lua-tests
cd lua-tests/lua-tests/
axmol build -p ios -a arm64 -c

cd build_ios_arm64/


 xcodebuild \
    -project lua-tests.xcodeproj \
    -scheme lua-tests \
    -configuration Debug \
    -sdk iphoneos \
    build \
    CODE_SIGNING_ALLOWED=NO \
    CODE_SIGNING_REQUIRED=NO
