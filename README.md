package models;

public class Counter{

	public int getNumberElements(String phrase, char caracter){
		int numberCaracter = 0;
		int size = phrase.length();
		for (int i = 0; i < size; i++){
			if (caracter == phrase.charAt(i)){
				numberCaracter++;
			}
		}
		return numberCaracter;
	}

	public boolean getBinary(String number){
		int numberCaracter = 0;
		int size = number.length();
		for (int i = 0; i < size; i++){
			if (number.charAt(i) == '1' || number.charAt(i) == '0'){
				numberCaracter++;
				return true;
			} 
			return false;
		}
		return false;
	}

	public int getNumberWords(String phrase){
		int numberWords = 0;
		int size = phrase.length();
		for (int i = 0; i < size; i++){
			if (phrase.charAt(i) == ' '){
				numberWords++;
			}
		}
		return numberWords + 1;
	}


	public int getNumberSimbols(String phrase){
		char symbol = 'v';
		int numberSymbols = 0;
		int size = phrase.length();
		for (int i = 0; i < size; i++){
			if (phrase.charAt(i) == (':' + symbol)){
					numberSymbols++;
			}
		}
		return numberSymbols;
	}

	public int getAddNumber(String phrase){
		int totalAdd = 0;
		int numberCaracter = 0;
		int size = phrase.length();
		for (int i = 0; i < size; i++){
			if(phrase.charAt(i) >= '1' && phrase.charAt(i) <= '9'){
				numberCaracter++;
				return totalAdd += phrase.charAt(i);
			}
		}
		return totalAdd;
	}

	public int getMajorNumber(String phrase){
		int size = phrase.length();
		int maxNumber = 0;
		int n = 1;
		for(int i = 0; i > size; i++){
			if(phrase.charAt(i) > n){
				n++;
				return maxNumber = i;
			}else if(phrase.charAt(i) < n){
				n++;
				return maxNumber = n;
			}
		}
		return maxNumber;
	}
	
	public static void main(String [] args){
		Counters elements = new Counters();
		//System.out.println("numero de carateres solicitado en la frase: " + elements.getNumberElements("hola como estas", ' '));
		//System.out.println(elements.getBinary("10001"));
		//System.out.println(elements.getNumberWords("Hola mundo de locos"));
		System.out.println(elements.getNumberSimbols("hola :v como estas :v hola:"));
		//System.out.println(elements.getAddNumber("9125"));
		//System.out.println(elements.getMajorNumber(1, 8, 3, 2));
	}
}                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     
