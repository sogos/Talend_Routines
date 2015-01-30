package routines;

import  java.io.FileInputStream;
import  java.io.FileOutputStream;
import  java.io.IOException;
import  java.util.zip.GZIPInputStream;


public class GzipUncompress {

    /**
     * unCompress: not return value, only print "hello" + message.
     * 
     * 
     * {talendTypes} String
     * 
     * {Category} User Defined
     * 
     * {param} string("input") input: The file to decompress
     * {param} string("output") output: The file uncompress destination
     * 
     * {example} unCompress("file", "target") (No output)
     */
    public static void unCompress(String input, String output)  {
    	
      byte[] buffer = new byte[1024];
      try {


        GZIPInputStream in = new GZIPInputStream(new FileInputStream(input));
        FileOutputStream out = new FileOutputStream(output);

        int len;
        while ((len = in.read(buffer)) > 0) {
          out.write(buffer, 0, len);
        }

        in.close();
        out.close();

      } catch (IOException e) {
       throw new RuntimeException("Error while uncompressing .." + e.getMessage());
     }
     
   }

 }
