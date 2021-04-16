---
description: Im folgenden Beispiel wird ein Hashwert für einige Daten erstellt und dieser Hash signiert. In einer zweiten Phase werden der Hash und seine Signatur überprüft. Der Hash wird mit dem privaten Schlüssel des Benutzers signiert, und der öffentliche Schlüssel des Signatur Gebers wird exportiert, sodass die Signatur überprüft werden kann.
ms.assetid: 72f5d30a-efd5-4bf5-8057-cb73e5aa0514
title: 'Beispiel-C-Programm: Signieren eines Hashs und Überprüfen der Hash Signatur'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000db2504b6a7046d040f6519f78de55e5b98c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393349"
---
# <a name="example-c-program-signing-a-hash-and-verifying-the-hash-signature"></a>Beispiel-C-Programm: Signieren eines Hashs und Überprüfen der Hash Signatur

Im [*folgenden Beispiel wird*](../secgloss/h-gly.md) ein Hashwert für einige Daten erstellt und dieser Hash signiert. In einer zweiten Phase werden der Hash und seine Signatur überprüft. Der Hash wird mit dem [*privaten Schlüssel*](../secgloss/p-gly.md)des Benutzers signiert, und der [*öffentliche Schlüssel*](../secgloss/p-gly.md) des Signatur Gebers wird exportiert, sodass die Signatur überprüft werden kann.

In diesem Beispiel werden die folgenden Aufgaben und [*kryptoapi*](../secgloss/c-gly.md) -Funktionen veranschaulicht:

-   Erwerben eines CSP mithilfe von [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).
-   Das Schlüsselpaar des Benutzers bei der Signatur wird mithilfe von " \_ [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey)" erhalten.
-   Erstellen eines PublicKeyBlob mit dem öffentlichen Schlüssel des Signatur Gebers, der im Signatur Überprüfungsprozess mithilfe von [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)verwendet werden soll.
-   Erstellen eines Hash Objekts mithilfe von " [**cryptkreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)".
-   Hashwert für die Daten mithilfe von [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata).
-   Signieren des Hashs mithilfe von " [**cryptsignhash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha)".
-   Zerstören des ursprünglichen Hash Objekts mithilfe von " [**cryptdestroyhash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash)".
-   Der öffentliche Schlüssel, der zum Überprüfen des verfügbaren Hashwerts mithilfe von [**cryptimportkey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)benötigt wird.
-   Erneutes Erstellen des Hash Objekts mithilfe von " [**cryptkreatehash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) " und " [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata)".
-   Überprüfen der Signatur für den Hash mithilfe von [**cryptverifysignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea).
-   Normale Bereinigung wird durchgeführt.


```C++
//--------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Example of signing a hash and 
// verifying the hash signature.
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

HCRYPTPROV hProv;
BYTE *pbBuffer= (BYTE *)"The data that is to be hashed and signed.";
DWORD dwBufferLen = strlen((char *)pbBuffer)+1;
HCRYPTHASH hHash;
HCRYPTKEY hKey;
HCRYPTKEY hPubKey;
BYTE *pbKeyBlob;        
BYTE *pbSignature;
DWORD dwSigLen;
DWORD dwBlobLen;

//-------------------------------------------------------------------
// Acquire a cryptographic provider context handle.

if(CryptAcquireContext(
   &hProv, 
   NULL, 
   NULL, 
   PROV_RSA_FULL, 
   0)) 
{
     printf("CSP context acquired.\n");
}
else
{
     MyHandleError("Error during CryptAcquireContext.");
}
//-------------------------------------------------------------------
// Get the public at signature key. This is the public key
// that will be used by the receiver of the hash to verify
// the signature. In situations where the receiver could obtain the
// sender's public key from a certificate, this step would not be
// needed.

if(CryptGetUserKey(   
   hProv,    
   AT_SIGNATURE,    
   &hKey)) 
{
    printf("The signature key has been acquired. \n");
}
else
{
    MyHandleError("Error during CryptGetUserKey for signkey.");
}
//-------------------------------------------------------------------
// Export the public key. Here the public key is exported to a 
// PUBLICKEYBOLB so that the receiver of the signed hash can
// verify the signature. This BLOB could be written to a file and
// sent to another user.

if(CryptExportKey(   
   hKey,    
   NULL,    
   PUBLICKEYBLOB,
   0,    
   NULL, 
   &dwBlobLen)) 
{
     printf("Size of the BLOB for the public key determined. \n");
}
else
{
     MyHandleError("Error computing BLOB length.");
}
//-------------------------------------------------------------------
// Allocate memory for the pbKeyBlob.

if(pbKeyBlob = (BYTE*)malloc(dwBlobLen)) 
{
    printf("Memory has been allocated for the BLOB. \n");
}
else
{
    MyHandleError("Out of memory. \n");
}
//-------------------------------------------------------------------
// Do the actual exporting into the key BLOB.

if(CryptExportKey(   
   hKey, 
   NULL,    
   PUBLICKEYBLOB,    
   0,    
   pbKeyBlob,    
   &dwBlobLen))
{
     printf("Contents have been written to the BLOB. \n");
}
else
{
    MyHandleError("Error during CryptExportKey.");
}
//-------------------------------------------------------------------
// Create the hash object.

if(CryptCreateHash(
   hProv, 
   CALG_MD5, 
   0, 
   0, 
   &hHash)) 
{
     printf("Hash object created. \n");
}
else
{
    MyHandleError("Error during CryptCreateHash.");
}
//-------------------------------------------------------------------
// Compute the cryptographic hash of the buffer.

if(CryptHashData(
   hHash, 
   pbBuffer, 
   dwBufferLen, 
   0)) 
{
     printf("The data buffer has been hashed.\n");
}
else
{
     MyHandleError("Error during CryptHashData.");
}
//-------------------------------------------------------------------
// Determine the size of the signature and allocate memory.

dwSigLen= 0;
if(CryptSignHash(
   hHash, 
   AT_SIGNATURE, 
   NULL, 
   0, 
   NULL, 
   &dwSigLen)) 
{
     printf("Signature length %d found.\n",dwSigLen);
}
else
{
     MyHandleError("Error during CryptSignHash.");
}
//-------------------------------------------------------------------
// Allocate memory for the signature buffer.

if(pbSignature = (BYTE *)malloc(dwSigLen))
{
     printf("Memory allocated for the signature.\n");
}
else
{
     MyHandleError("Out of memory.");
}
//-------------------------------------------------------------------
// Sign the hash object.

if(CryptSignHash(
   hHash, 
   AT_SIGNATURE, 
   NULL, 
   0, 
   pbSignature, 
   &dwSigLen)) 
{
     printf("pbSignature is the hash signature.\n");
}
else
{
     MyHandleError("Error during CryptSignHash.");
}
//-------------------------------------------------------------------
// Destroy the hash object.

if(hHash) 
  CryptDestroyHash(hHash);

printf("The hash object has been destroyed.\n");
printf("The signing phase of this program is completed.\n\n");

//-------------------------------------------------------------------
// In the second phase, the hash signature is verified.
// This would most often be done by a different user in a
// separate program. The hash, signature, and the PUBLICKEYBLOB
// would be read from a file, an email message, 
// or some other source.

// Here, the original pbBuffer, pbSignature, szDescription. 
// pbKeyBlob, and their lengths are used.

// The contents of the pbBuffer must be the same data 
// that was originally signed.

//-------------------------------------------------------------------
// Get the public key of the user who created the digital signature 
// and import it into the CSP by using CryptImportKey. This returns
// a handle to the public key in hPubKey.

if(CryptImportKey(
   hProv,
   pbKeyBlob,
   dwBlobLen,
   0,
   0,
   &hPubKey))
{
     printf("The key has been imported.\n");
}
else
{
     MyHandleError("Public key import failed.");
}
//-------------------------------------------------------------------
// Create a new hash object.

if(CryptCreateHash(
   hProv, 
   CALG_MD5, 
   0, 
   0, 
   &hHash)) 
{
     printf("The hash object has been recreated. \n");
}
else
{
     MyHandleError("Error during CryptCreateHash.");
}
//-------------------------------------------------------------------
// Compute the cryptographic hash of the buffer.

if(CryptHashData(
   hHash, 
   pbBuffer, 
   dwBufferLen, 
   0)) 
{
     printf("The new hash has been created.\n");
}
else
{
     MyHandleError("Error during CryptHashData.");
}
//-------------------------------------------------------------------
// Validate the digital signature.

if(CryptVerifySignature(
   hHash, 
   pbSignature, 
   dwSigLen, 
   hPubKey,
   NULL, 
   0)) 
{
     printf("The signature has been verified.\n");
}
else
{
     printf("Signature not validated!\n");
}
//-------------------------------------------------------------------
// Free memory to be used to store signature.

if(pbSignature)
  free(pbSignature);

//-------------------------------------------------------------------
// Destroy the hash object.

if(hHash) 
  CryptDestroyHash(hHash);

//-------------------------------------------------------------------
// Release the provider handle.

if(hProv) 
   CryptReleaseContext(hProv, 0);
} //  End of main

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the  
//  standard error (stderr) file and exit the program. 
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



 

 
