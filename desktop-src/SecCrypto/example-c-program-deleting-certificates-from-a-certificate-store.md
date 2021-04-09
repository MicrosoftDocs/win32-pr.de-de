---
description: Im folgenden Beispiel werden die Zertifikate in einem Systemzertifikat Speicher aufgelistet. dabei wird der Name des Antragstellers der einzelnen Zertifikate angezeigt, und der Benutzer kann auswählen, ob Zertifikate aus dem Speicher gelöscht werden sollen.
ms.assetid: 52a0287b-7d2a-483e-8bbc-43621c4b7103
title: 'Beispiel-C-Programm: Löschen von Zertifikaten aus einem Zertifikat Speicher'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f29f55d27bf2a85d82e4ab96e51fe5368c9de935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864780"
---
# <a name="example-c-program-deleting-certificates-from-a-certificate-store"></a>Beispiel-C-Programm: Löschen von Zertifikaten aus einem Zertifikat Speicher

Im folgenden Beispiel werden die Zertifikate in einem System [*Zertifikat Speicher*](../secgloss/c-gly.md)aufgelistet. dabei wird der Name des Antragstellers der einzelnen Zertifikate angezeigt, und der Benutzer kann auswählen, ob Zertifikate aus dem Speicher gelöscht werden sollen. Im Beispiel wird der Name des Zertifikat Speicher des Benutzers abgerufen und kann daher verwendet werden, um den Inhalt eines beliebigen Systemzertifikat Speicher zu verwalten.

In diesem Beispiel werden die folgenden Aufgaben und [*kryptoapi*](../secgloss/c-gly.md) -Funktionen veranschaulicht:

-   Öffnen eines Systemzertifikat Speicher mithilfe von " [**certopdsystemstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea)".
-   Auflisten der Zertifikate in einem Zertifikat Speicher mithilfe von [**certenrecertifikatesinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore).
-   Der Name des Subjekts eines Zertifikats mit [**certgetnamestring wird abgerufen**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).
-   Vergleichen des Namens des Antragstellers des Zertifikats mit dem Namen des Ausstellers des Zertifikats unter Verwendung von [**certcomparecertifikatename**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificatename).
-   Es wird überprüft, ob der öffentliche Schlüssel des aktuellen Zertifikats mit dem öffentlichen Schlüssel eines vorherigen Zertifikats mit [**certcomparepublickeyinfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparepublickeyinfo)übereinstimmt.
-   Duplizieren eines Zeigers auf einen [*Zertifikat Kontext*](../secgloss/c-gly.md) mithilfe von [**certduplikatecertifiertifikatecontext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext).
-   Vergleichen der [**CERT \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) -Mitglieder der einzelnen Zertifikate mithilfe von " [**certcomparecertificate**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificate)".
-   Löschen eines Zertifikats aus einem Speicher mithilfe von " [**certdeletecertifikatefromstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)".
-   Schließen eines Zertifikat Speicher mithilfe von " [**certclosestore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)".

In diesem Beispiel wird der Name eines Systemzertifikat Speicher vom Benutzer abgerufen, der Speicher geöffnet und die Zertifikate in diesem Speicher durchlaufen. Für jedes Zertifikat wird der Name des Antragstellers des Zertifikats angezeigt, und der Benutzer erhält die Möglichkeit, das Zertifikat zu löschen.


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Declare and initialize variables.

HANDLE          hStoreHandle;
PCCERT_CONTEXT  pCertContext=NULL;   
PCCERT_CONTEXT  pDupCertContext; 
PCERT_PUBLIC_KEY_INFO pOldPubKey = NULL;
PCERT_PUBLIC_KEY_INFO pNewPubKey; 
char pszStoreName[256];
char pszNameString[256];
char fResponse ='n';  
char x;

//-------------------------------------------------------------------
// Get the name of the certificate store to open. 
printf("This program maintains the contents of a certificate\n");
printf("store by allowing you to delete any excess certificates\n");
printf("from a store. \n\n");
printf("Please enter the name of the system store to maintain:");
fgets(pszStoreName, 255, stdin);
if (pszStoreName[strlen(pszStoreName) - 1] =='\n')
   pszStoreName[strlen(pszStoreName) - 1] = '\0';
printf("Certificates will be deleted from "
       "the %s store.\n",pszStoreName);

//-------------------------------------------------------------------
// Open a system certificate store.

if ( hStoreHandle = CertOpenSystemStore(
     NULL,     
     pszStoreName))
{
     printf("The %s store has been opened. \n", pszStoreName);
}
else
{
     MyHandleError("The store was not opened.");
}
//-------------------------------------------------------------------
// Find the certificates in the system store. 

while(pCertContext= CertEnumCertificatesInStore(
    hStoreHandle,
    pCertContext)) // on the first call to the function,
                   //  this parameter is NULL
                   // on all subsequent
                   //  calls, it is the last pointer returned by 
                   //  the function
{
//-------------------------------------------------------------------
// Get and display the name of the subject of the certificate.

if(CertGetNameString(   
   pCertContext,   
   CERT_NAME_SIMPLE_DISPLAY_TYPE,   
   0,
   NULL,   
   pszNameString,   
   128))
{
   printf("\nCertificate for %s \n",pszNameString);
}
else
{
   MyHandleError("CertGetName failed.");
}
//-------------------------------------------------------------------
// Check to determine whether the issuer 
// and the subject are the same.

if(CertCompareCertificateName(
   MY_ENCODING_TYPE,
   &(pCertContext->pCertInfo->Issuer),
   &(pCertContext->pCertInfo->Subject)))
{
     printf("The certificate subject and issuer are the same.\n");
}
else
{
     printf("The certificate subject and issuer "
         "are not the same.\n");
}
//--------------------------------------------------------------------
// Determine whether this certificate's public key matches 
// the public key of the last certificate.

pNewPubKey = &(pCertContext->pCertInfo->SubjectPublicKeyInfo);
if(pOldPubKey)
   if(CertComparePublicKeyInfo(
       MY_ENCODING_TYPE,
       pOldPubKey,
       pNewPubKey))
   {
       printf("The public keys are the same.\n");
   }
   else
   {
       printf("This certificate has a different public key.\n");
   }
//-------------------------------------------------------------------
// Reset the old key.

pOldPubKey = pNewPubKey;

//-------------------------------------------------------------------
// Determine whether this certificate is to be deleted. 

printf("Would you like to delete this certificate? (y/n) ");
fResponse = getchar();
if(fResponse == 'y')
{
   //----------------------------------------------------------------
   // Create a duplicate pointer to the certificate to be 
   // deleted. In this way, the original pointer is not freed 
   // when the certificate is deleted from the store 
   // and the enumeration of the certificates in the store can
   // continue. If the original pointer is used, after the 
   // certificate is deleted, the enumeration loop stops.

   if(pDupCertContext = CertDuplicateCertificateContext(
      pCertContext))
   {
       printf("A duplicate pointer was created. Continue. \n");
   }
   else
   {
        MyHandleError("Duplication of the certificate "
            "pointer failed.");
   }

//-------------------------------------------------------------------
// Compare the pCertInfo members of the two certificates 
// to determine whether they are identical.

if(CertCompareCertificate(
      X509_ASN_ENCODING,
      pDupCertContext->pCertInfo, 
      pCertContext->pCertInfo))
{
     printf("The two certificates are identical. \n");
}
else
{
     printf("The two certificates are not identical. \n");
}
//-------------------------------------------------------------------
// Delete the certificate.
   if(CertDeleteCertificateFromStore(
     pDupCertContext))   
   {
       printf("The certificate has been deleted. Continue. \n");
   }
   else
   {
      printf("The deletion of the certificate failed.\n");
   }
} // end if

//-------------------------------------------------------------------
// Clear the input buffer.

x = getchar();

} // end while

//-------------------------------------------------------------------
// Clean up.

CertCloseStore(
   hStoreHandle,
   0);
printf("The program ran to completion successfully. \n");
} // end main

//-------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function to print an error message and exit 
// the program. 
// For most applications, replace this function with one 
// that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // end MyHandleError
```



 

 
