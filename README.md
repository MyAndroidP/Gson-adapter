# Gson-adapter
Gson 容错解析器
使用的方法：
1.将上面的3个java文件下载下来，放置同一包下
2.配置Retrofit时，通过addConverterFactory(BaseConverterFactory.create())来添加使用
//配合Retrofit

      Retrofit retrofit = new Retrofit.Builder()
 
                  //  .client(okHttpClientBuilder.build()) 自配置的okhttpclient
                  
                  //.baseUrl(url) 基地址
                  
                    .addCallAdapterFactory(RxJavaCallAdapterFactory.create())
                    
                  //  .addConverterFactory(ScalarsConverterFactory.create())
                  
                    .addConverterFactory(BaseConverterFactory.create())
                    
                    .build();
