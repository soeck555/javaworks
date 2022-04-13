# javaworks
package com.callor.arrays.service;

import com.callor.arrays.utils.Line;

/*
 * makeScore()
 * printScore()
 * sumScore()
 * 등의 method 를 선언하고
 * 
 * 임의 성적을 생성하여 intKor 에 저장
 * 성적일람표 출력
 * 총점계산
 * 
 */
public class ScoreServiceV6 {
	
	private int[] intKor;
	
	
	public ScoreServiceV6() {
		intKor = new int[100];
		
	}
	public void makeScore() {
		for( int index = 0 ; index < intKor.length ; index++) {
			intKor[index] = (int)(Math.random() *100) +1;
		}
	}
	public void printScore() {
		System.out.println( Line.dLine);
		System.out.println("영어성적일람표");
		System.out.println( Line.sLine);
		for(int index = 0; index < intKor.length ; index ++) {
			System.out.printf("%d번:%d\t\t", (index+1),intKor[index]);
			if( (index + 1) % 5 == 0) {
				System.out.println();
			}
		}
	}
	public void sumScore() {
		int intsum = 0 ;
		for(int index = 0 ; index < intKor.length ; index ++) {
			intsum = intsum + intKor[index];
			System.out.println("총점 : " + intsum);{
				if((index + 1) % intKor.length == 0 ) {
					System.out.println();
				}
			}
		}
	}
}
