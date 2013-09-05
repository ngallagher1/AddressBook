GeneralContact
===========
import java.io.*;
import java.util.*;
import java.lang.*;
import java.text.*;

public class GeneralContact<E>
{
	private ArrayList<E> contacts;
	private String firstName;
	private String lastName;
	private int phoneNumber;
	private String address;

	public GeneralContact()
	{
		contacts = new ArrayList<E>();
		firstName = "";
		lastName = "";
		phoneNumber = 0;
		address = "";
	}

	public GeneralContact(String first, String last, int phone, String a)
	{
		firstName = first;
		lastName = last;
		phoneNumber = phone;
		address = a;
	}

    public boolean equals(Object otherObject)
    {
  	  if(otherObject == null)
  	     return false;
  	  if(otherObject == this)
  	     return true;
  	  if(this.getClass() != otherObject.getClass())
  	     return false;
  	  GeneralContact otherContact = (GeneralContact)otherObject;
  	  return phoneNumber == otherContact.phoneNumber;
    }

	public boolean isEmpty()
	{ return contacts.size() == 0; }

    public int size()
    { return contacts.size(); }

}
