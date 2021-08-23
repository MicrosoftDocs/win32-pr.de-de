---
description: Das folgende Beispiel listet die Zertifikate in einem Systemzertifikatspeicher auf, zeigt den Namen des Betreffs jedes Zertifikats an und ermöglicht es dem Benutzer, alle Zertifikate aus dem Speicher zu löschen.
ms.assetid: 52a0287b-7d2a-483e-8bbc-43621c4b7103
title: 'Beispiel C-Programm: Löschen von Zertifikaten aus einem Store'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 065a7e0e46f3072d69014e294610ec7ae546d05c98816f809b9b2de92949db62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007853"
---
# <a name="example-c-program-deleting-certificates-from-a-certificate-store"></a>Beispiel C-Programm: Löschen von Zertifikaten aus einem Store

Das folgende Beispiel listet die Zertifikate in einem Systemzertifikatspeicher [*auf,*](../secgloss/c-gly.md)zeigt den Namen des Betreffs jedes Zertifikats an und ermöglicht es dem Benutzer, alle Zertifikate aus dem Speicher zu löschen. Das Beispiel ruft den Namen des Zertifikatspeichers vom Benutzer ab und kann daher verwendet werden, um den Inhalt eines beliebigen Systemzertifikatspeichers zu verwalten.

Dieses Beispiel veranschaulicht die folgenden Aufgaben und [*CryptoAPI-Funktionen:*](../secgloss/c-gly.md)

-   Öffnen eines Systemzertifikatspeichers [**mithilfe von CertOpenSystemStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea)
-   Auflisten der Zertifikate in einem Zertifikatspeicher [**mithilfe von CertEnumCertificatesInStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore)
-   Abrufen des Namens des Betreffs eines Zertifikats [**mithilfe von CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).
-   Vergleicht den Namen des Zertifikatssubjekts mit dem Namen des Zertifikatausstellers mithilfe von [**CertCompareCertificateName.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificatename)
-   Überprüfen, ob der öffentliche Schlüssel des aktuellen Zertifikats mit dem öffentlichen Schlüssel eines vorherigen Zertifikats mithilfe von [**CertComparePublicKeyInfo entspricht.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparepublickeyinfo)
-   Duplizieren eines Zeigers auf einen [*Zertifikatkontext mithilfe*](../secgloss/c-gly.md) [**von CertDuplicateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext).
-   Vergleichen der [**CERT \_ INFO-Member**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_info) jedes Zertifikats [**mithilfe von CertCompareCertificate**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificate).
-   Löschen eines Zertifikats aus einem Speicher [**mithilfe von CertDeleteCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore).
-   Schließen eines Zertifikatspeichers [**mithilfe von CertCloseStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)

Dieses Beispiel ruft den Namen eines Systemzertifikatspeichers vom Benutzer ab, öffnet diesen Speicher und durchläuft die Zertifikate in diesem Speicher. Für jedes Zertifikat wird der Name des Zertifikatssubjekts angezeigt, und der Benutzer erhält die Möglichkeit, dieses Zertifikat zu löschen.


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



 

 
