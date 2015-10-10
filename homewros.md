# Homeworks
package github;

import java.util.*;

public class Personne {
	Scanner clavier =new Scanner (System.in);
	private String nom,nationalite;
	//private static  int nbrami=0;
	ArrayList<Personne> amis=new ArrayList<Personne>();
	//Personne[] amis;
	
	 //constructeur  copy
public Personne (Personne autre)
{
this.nom=autre.nom;
this.nationalite=autre.nationalite;
}
//constructeur a arguments 
public Personne ( String nm,String nat){nom=nm;nationalite=nat;}
// constructeur par defaut
public Personne (){}
public String toString()
{return"NOM:"+this.nom+"\nNATIONALITE:"+this.nationalite;}

public void CréeListeAmi(Personne p)
{ 
String answer; p=new Personne ();
System.out.println("voici la liste de vos amis:");
do{
System.out.println("LE NOM:");
p.nom=clavier.next();
System.out.println("LA NATIONALITE:");
p.nationalite=clavier.next();
ajouterAmi(p);
System.out.println("y a t'il un autre ami? oui/non");
answer=clavier.next();}while(answer.equals("oui"));
}
public void ajouterAmi(Personne z)
{
	amis.add(z);
	/*amis[nbrami].nom=p.nom;
	amis[nbrami].nationalite=p.nationalite;
	nbrami++;*/
}


		
public void MalisteAmi()
{
	for(int i=0;i<amis.size();i++)
	{System.out.println(amis.get(i));
	}
}
public void amialgerien(){
	System.out.println("vos amis algeriens sont:");
	for(int i=0;i<amis.size();i++)
	{
		if(amis.get(i).nationalite.equals("algerien")){
			System.out.println(amis.get(i));}
			
	}
}
public void amiEtranger(){
	System.out.println("vos amis etrangers sont:");
	for(int i=0;i<amis.size();i++)
	{
		if(!amis.get(i).nationalite.equals("algerien"))
			System.out.println(amis.get(i));
			
	}
	}
}
