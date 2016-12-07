# Gson-adapter
Gson 容错解析器
使用的方法：

 Retrofit retrofit = new Retrofit.Builder()
                  //  .client(okHttpClientBuilder.build()) 自配置的okhttpclient
                  //.baseUrl(url) 基地址
                    .addCallAdapterFactory(RxJavaCallAdapterFactory.create())
                  //  .addConverterFactory(ScalarsConverterFactory.create())
                    .addConverterFactory(BaseConverterFactory.create())
                    .build();
