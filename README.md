# jquery.i18n
简单易用的jquery国际化插件
创建语言包 /i18n/i18n_xx.json

    $(document).ready(function () {
      /*默认语言*/
      var defaultLang = "en";
      $("[i18n]").i18n({
        defaultLang: defaultLang,
        filePath: "./i18n/",
        filePrefix: "i18n_",
        fileSuffix: "",
        forever: true,
        callback: function () {
          console.log("i18n has been completed.");
        }
      });
      /*切换为中文 - 按钮*/
      $("#chinese").click(function () {
        console.log('中文');
        $("[i18n]").i18n({
          defaultLang: "cn"
        });

      });
      /*切换为英文 - 按钮*/
      $("#english").click(function () {
        console.log('英文');
        $("[i18n]").i18n({
          defaultLang: "en",
        });
      });
      /*切换为越南 - 按钮*/
      $("#Vietnam").click(function () {
        console.log('越南');
        $("[i18n]").i18n({
          defaultLang: "vi",
        });
      });

    });
