---
description: Das folgende Beispiel veranschaulicht das Serialisieren eines Zertifikatkontexts und seiner Eigenschaften in ein Formular, das in einer Datei gespeichert, mit einer E-Mail gesendet oder anderweitig an einen anderen Benutzer übertragen werden kann.
ms.assetid: cda7fa68-debe-40e6-8c4a-536dacccc2d1
title: 'C-Beispielprogramm: Serialisieren von Zertifikaten'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8931c0d45a8117257d3af4e9430c60e990a50646529f5bcb43a8d3349e35a0e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007518"
---
# <a name="example-c-program-serializing-certificates"></a>C-Beispielprogramm: Serialisieren von Zertifikaten

Das folgende Beispiel veranschaulicht das Serialisieren eines [*Zertifikatkontexts*](../secgloss/c-gly.md) und seiner Eigenschaften in ein Formular, das in einer Datei gespeichert, mit einer E-Mail gesendet oder anderweitig an einen anderen Benutzer übertragen werden kann. Das Beispiel zeigt auch, wie das serialisierte Zertifikat wieder in ein Zertifikat geändert und einem Zertifikatspeicher hinzugefügt werden kann. Der gleiche Prozess funktioniert auch mit [*CRLs*](../secgloss/c-gly.md) und [*CTLs,*](../secgloss/c-gly.md) die [**CertSerializeCRLStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecrlstoreelement) und [**CertSerializeCTLStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializectlstoreelement)verwenden.

In diesem Beispiel werden die folgenden Aufgaben und CryptoAPI-Funktionen veranschaulicht:

-   Öffnen eines Systemzertifikatspeichers mit [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea).
-   Öffnen eines Zertifikatspeichers mit [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).
-   Abrufen eines Zertifikats aus einem Speicher mithilfe von [**CertEnumCertificatesInStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore)
-   Abrufen des Namens des Antragstellers des Zertifikats mithilfe von [**CertGetNameString.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)
-   Erstellen einer serialisierten Form eines [*Zertifikatkontexts*](../secgloss/c-gly.md) und seiner Eigenschaften mithilfe von [**CertSerializeCertificateStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecertificatestoreelement).
-   Erstellen eines neuen Zertifikats aus einer serialisierten Zeichenfolge und Hinzufügen in einen Zertifikatspeicher mithilfe von [**CertAddSerializedElementToStore.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore)
-   Verwenden von [**CertAddEncodedCertificateToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore) zum Erstellen eines neuen Zertifikats aus dem codierten Teil eines vorhandenen Zertifikats.
-   Verwenden von [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) zum Schließen eines Zertifikatspeichers.


```C++
//------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Example that uses CertSerializeCertificateStoreElement to
// serialize the data from a certificate, 
// and CertAddSerializedElementToStore to add that data as a new
// certificate to a store.
// CertAddEncodeCertificateToStore is also demonstrated.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//-------------------------------------------------------------------
// Declare and initialize variables.

HCERTSTORE         hSystemStore;
HCERTSTORE         hFileStore;
PCCERT_CONTEXT     pCertContext = NULL;
char               pszNameString[256]; 
BYTE*              pbElement;
DWORD              cbElement;

//-------------------------------------------------------------------
// Open a system certificate store.

if(hSystemStore = CertOpenSystemStore(
    0,
    "CA"))
{
  printf("The CA system store is open. Continue.\n");
}
else
{
  MyHandleError("The first system store did not open.");
}
//-------------------------------------------------------------------
// Open a second store.
// In order to work, a file-based certificate store named 
// teststor.sto must be available in the working directory.

if(hFileStore = CertOpenStore(
   CERT_STORE_PROV_FILENAME,
   MY_ENCODING_TYPE,
   NULL,
   0,
   L"testStor.sto" ))
{
     printf("The file store is open. Continue.\n");
}
else
{
     MyHandleError("The file store did not open.");
}
//-------------------------------------------------------------------
// Retrieve the first certificate from the Root store.
// CertFindCertificateInStore could be used here to find
// a certificate with a specific property.

if(pCertContext=CertEnumCertificatesInStore(
    hSystemStore,
    pCertContext))
{
printf("A certificate is available. Continue.\n");
}
else
{
     MyHandleError("No certificate available. "
         "The store may be empty.");
}
//-------------------------------------------------------------------
//  Find and print the name of the subject of the certificate 
//  just retrieved.

if(CertGetNameString(   
   pCertContext,   
   CERT_NAME_SIMPLE_DISPLAY_TYPE,   
   0,
   NULL,   
   pszNameString,   
   128))
{
     printf("Certificate for %s has been retrieved.\n",
         pszNameString);
}
else
{
     printf("CertGetName failed. \n");
}
//-------------------------------------------------------------------
// Find out how much memory to allocate for the serialized element.

if(CertSerializeCertificateStoreElement(
    pCertContext,      // The existing certificate.
    0,                 // Accept default for dwFlags, 
    NULL,              // NULL for the first function call.
    &cbElement))       // Address where the length of the 
                       // serialized element will be placed.
{
     printf("The length of the serialized string is %d.\n",
         cbElement);
}
else
{
     MyHandleError("Finding the length of the serialized "
         "element failed.");
}
//-------------------------------------------------------------------
// Allocate memory for the serialized element.

if(pbElement = (BYTE*)malloc(cbElement))
{
     printf("Memory has been allocated. Continue.\n");
}
else
{
     MyHandleError("The allocation of memory failed.");
}
//-------------------------------------------------------------------
// Create the serialized element from a certificate context.

if(CertSerializeCertificateStoreElement(
    pCertContext,        // The certificate context source for the 
                         // serialized element.
    0,                   // dwFlags. Accept the default.
    pbElement,           // A pointer to where the new element will
                         // be stored.
    &cbElement))         // The length of the serialized element,
{
     printf("The encoded element has been serialized. \n");
}
else
{
     MyHandleError("The element could not be serialized.");
}
//-------------------------------------------------------------------
//  pbElement could be written to a file or be sent by email
//  to another user. 
//  The following process uses the serialized 
//  pbElement and its length, cbElement, to 
//  add a new certificate to a store.

if(CertAddSerializedElementToStore(
    hFileStore,          // Store where certificate is to be added.
    pbElement,           // The serialized element for another
                         // certificate. 
    cbElement,           // The length of pbElement.  
    CERT_STORE_ADD_REPLACE_EXISTING,
                         // Flag to indicate what to do if a matching
                         // certificate is already in the store.
    0,                   // dwFlags. Accept the default.
    CERT_STORE_CERTIFICATE_CONTEXT_FLAG, 
    NULL,
    NULL
    ))
{
     printf("The new certificate is added to the second store.\n");
}
else
{
     MyHandleError("The new element was not added to a store.");
}
//-------------------------------------------------------------------
//  Next, another certificate will be retrieved from the system store
//  and its encoded part, pCertContext->pbCertEncoded, will be
//  used to create a new certificate to be added to the file store.

if(pCertContext=CertEnumCertificatesInStore(
    hSystemStore,
    pCertContext))
{
printf("Another certificate is available. Continue.\n");
}
else
{
     MyHandleError("No certificate is available. "
         "The store may be empty.");
}

//-------------------------------------------------------------------
//  Find and print the name of the subject of the certificate 
//  just retrieved.

if(CertGetNameString(   
   pCertContext,   
   CERT_NAME_SIMPLE_DISPLAY_TYPE,   
   0,
   NULL,   
   pszNameString,   
   128))
{
     printf("Certificate for %s has been retrieved.\n",
         pszNameString);
}
else
{
     printf("CertGetName failed. \n");
}
//-------------------------------------------------------------------
//  Create a new certificate from the encoded portion of pCertContext
//  and add it to the file-based store.

if(CertAddEncodedCertificateToStore(
     hFileStore,
     MY_ENCODING_TYPE,
     pCertContext->pbCertEncoded,
     pCertContext->cbCertEncoded,
     CERT_STORE_ADD_USE_EXISTING,
     NULL))
{
     printf("Another certificate is added to the file store.\n");
}
else
{
     MyHandleError("The new certificate was not added to the "
         "file store.");
}
//-------------------------------------------------------------------
// Free memory.

free(pbElement);
CertCloseStore(hSystemStore,0);
CertCloseStore(hFileStore,0); 
printf("The program ran without error to the end.\n");

} // End of main

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the standard  
//  error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // End of MyHandleError
```



 

 
