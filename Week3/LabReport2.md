    import java.io.IOException;
    import java.net.URI;
    class StringHandler implements URLHandler{
        //The stored message that will be printed on the website
        String message = "";
    
        public String handleRequest(URI url) {
            if (url.getPath().equals("/"))
                return message;
            else {
                if (url.getPath().contains("/add-message")) {
                   String[] parameters = url.getQuery().split("=");
                   if (parameters[0].equals("s")) {
                        message += parameters[1] + "\n";
                        return message;
                    }
                }
               return "404 Not Found!";
            }
        }
    }

    class StringServer {
        public static void main(String[] args) throws IOException {
            if(args.length == 0){
               System.out.println("Missing port number! Try any number between 1024 to 49151");
               return;
           }

           int port = Integer.parseInt(args[0]);

           Server.start(port, new StringHandler());
        }
    }

![Image](Capture2.PNG)

![Image](Capture3.PNG)
