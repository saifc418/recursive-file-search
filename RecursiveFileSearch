package recursivefilesearch;

import java.io.File;

public class RecursiveFileSearch {

	// Method to count the number of .txt files in a folder and its subfolders
	public static int countTextFiles(File folder) {
		int count = 0; // DO NOT create extra variables or counters
		
		File[] files = folder.listFiles(); // List all files and subfolders
		
		// If the folder is empty, run this
		if (files == null) {
			
			System.out.println("Empty folder");
			return 0;
		}
		
		// Loop for each file in the array
		for (File file: files) {
			
			// Run this block if it is a directory (like a folder)
			if (file.isDirectory()) {
	
				// Print out the folder name
				System.out.print(file.getName() + ": ");
				
				// Accumulate count variable and recursively call method
				count += countTextFiles(file);
			}
			
			// Run this block if it is a file
			if (file.isFile()) {
				
				// Run this block if the file ends with ".txt"
				if (file.getName().endsWith(".txt")) {
					
					// Print out the file name
					System.out.print(file.getName() + " ");
					
					// Accumulate count
					count += 1;
				}
			}
		}
		
		// Print new line
		System.out.println();
		
		// Return count
		return count;
	}


	
	public static void main(String[] args) {
		
		File folder = new File("mainFolder"); // Main folder
		int txtFileCount = countTextFiles(folder);
		System.out.println("Total number of .txt files: " + txtFileCount);
	}
}
