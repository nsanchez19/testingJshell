# Repository for testing jshell

   3 :  String intToBinaryWithSeparator(int n, String separator) {
                String str = String.format("%032d", new java.math.BigInteg
er(Integer.toBinaryString(n)));

                String[] as = str.split("(?<=\\G........)");

                java.util.stream.Stream<String> streamIn = java.util.Array
s.stream(as);

                java.util.stream.Stream<String> streamOut = streamIn.map(s
 -> {
                        java.lang.StringBuilder sb = new java.lang.StringB
uilder(s);
                        sb.insert(4, '_');
                        return sb.toString();
                });

                return streamOut.collect(java.util.stream.Collectors.joini
ng(separator));
        }
   4 :  String intToBin(int n) {
                return intToBinaryWithSeparator(n, " , ");
        }
   5 : int n = 68;
   6 : byte b = 127;
   7 : char c = 'B';
