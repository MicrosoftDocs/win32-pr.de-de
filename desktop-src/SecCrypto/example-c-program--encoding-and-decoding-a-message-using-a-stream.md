---
description: Veranschaulicht die Verwendung der Funktionen cryptmsgopentoencode, cryptmsgopentodecode und cryptmsgupdate mit der CMSG-Daten \_ Strom \_ Informationsstruktur zum Codieren und Decodieren einer Nachricht mithilfe der Streamingfunktionen dieser Funktionen.
ms.assetid: 6c9c0509-1ad9-42cd-9589-e77752df6739
title: 'Beispiel-C-Programm: Codieren und Decodieren einer Nachricht mithilfe eines Streams'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 962420bfba05caabb272419e305ee01f76d39c63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754177"
---
# <a name="example-c-program-encoding-and-decoding-a-message-using-a-stream"></a>Beispiel-C-Programm: Codieren und Decodieren einer Nachricht mithilfe eines Streams

Im folgenden Beispiel wird veranschaulicht, wie die Funktionen [**cryptmsgopentoencode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode), [**cryptmsgopentodecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)und [**cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) mit der [**CMSG-Daten \_ Strom \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_stream_info) Struktur zum Codieren und Decodieren einer Nachricht mithilfe der Streamingfunktionen dieser Funktionen verwendet werden.

Das Signieren und Codieren einer Nachricht gewährleistet nicht den Datenschutz für diese Nachricht. Stattdessen wird die Authentizität der Nachricht sichergestellt. Da die Nachricht mit dem privaten Schlüssel des Absenders signiert ist und der Empfänger der Nachricht die Signatur mit dem [*öffentlichen Schlüssel*](../secgloss/p-gly.md) des Absenders entschlüsselt (verfügbar über das Zertifikat, das zusammen mit der Nachricht gesendet wird), kann der Empfänger sicher sein, dass die Nachricht von der Person oder Entität gesendet wurde, die dem Zertifikat zugeordnet ist, und dass die Nachricht nach der Signierung nicht geändert wurde.

Dieser Teil der Codierungs Signierung dieses Beispiels veranschaulicht die folgenden Aufgaben und kryptoapi-Funktionen:

-   Öffnen eines Zertifikat Speicher mithilfe von " [**certopendstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)".
-   Abrufen eines Zertifikats mit einem bestimmten Antragsteller Namen mithilfe von " [**certfindcertifikateinstore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)".
-   Der Antragsteller Name eines Zertifikats wird mithilfe von [**certgetnamestring**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)abgerufen und gedruckt.
-   Das Handle für einen Kryptografieanbieter, der einen privaten Schlüssel mit der [**CryptAcquireCertificatePrivateKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecertificateprivatekey) -Funktion bereitstellen kann.
-   Initialisieren der [**CMSG- \_ signierten \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) Informationen und der [**CMSG-Daten \_ Strom \_ Info**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_stream_info) -Strukturen, die in einem Rückruf von [**cryptmsgopentoencode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)verwendet werden sollen.
-   Signieren und Codieren einer Nachricht mithilfe von [**cryptmsgopentoencode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode) und [**cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).
-   Implementieren einer streamcallback-Funktion, die eine codierte und signierte Nachricht in einem beliebigen permanenten Format speichern kann, z. b. beim Schreiben in eine Datei.

Der Decodierungs Teil dieses Beispiels veranschaulicht die folgenden Aufgaben und kryptoapi-Funktionen:

-   Initialisieren einer [**CMSG-Daten \_ Strom- \_ Informations**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_stream_info) Struktur, die in einem Rückruf von [**cryptmsgopentodecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)verwendet werden soll.
-   Implementieren einer streamcallback-Funktion, die eine decodierte Nachricht in einem beliebigen permanenten Format speichern kann, z. b. beim Drucken auf dem Bildschirm.
-   Lesen einer codierten Nachricht aus einer Datei und Decodieren der Nachricht mithilfe von [**cryptmsgupdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).

Ein Beispiel für die Ausführung dieser Vorgänge ohne Verwendung eines streamrückrufs finden Sie [unter Beispiel C-Programm: Signieren, codieren, decodieren und Überprüfen einer Nachricht](example-c-program-signing-encoding-decoding-and-verifying-a-message.md).

In diesem Beispiel wird die Funktion " [**myhanderror**](myhandleerror.md)" verwendet. Der Code für diese Funktion ist im Beispiel enthalten. Der Code für diese und andere Hilfsfunktionen wird auch unter [allgemeine \_ \_ Funktionen](general-purpose-functions.md)aufgeführt.


```C++
#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>
#pragma comment(lib, "crypt32.lib")

// Link with the Crypt32.lib file.
#pragma comment (lib, "Crypt32")

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

#define MAX_NAME 256

#define ENCODED_FILE_NAME L"testStream.p7s"

//-------------------------------------------------------------------
//  Define function MyHandleError.
void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.

//+----------------------------------------------
// Callback function used for streamed Signing. 
//-----------------------------------------------
BOOL 
WINAPI
EncodeCallback(
    const void *pvArg,
    BYTE *pbData,
    DWORD cbData,
    BOOL fFinal)
{
    DWORD dwWrittenBytes = 0;
    HANDLE hFileToWrite = INVALID_HANDLE_VALUE;
        
    hFileToWrite = *((HANDLE *)pvArg);
    if ( !WriteFile(
            hFileToWrite,
            pbData,
            cbData,
            &dwWrittenBytes,
            NULL) ||
        (dwWrittenBytes != cbData))
    {
        return FALSE;
    }

    return TRUE;
}

//+----------------------------------------------
// Callback function used for decoding streamed Signing.
//-----------------------------------------------
BOOL 
WINAPI
DecodeCallback(
    const void *pvArg,
    BYTE *pbData,
    DWORD cbData,
    BOOL fFinal)
{
    if (pbData != NULL && cbData > 0)
    {
        *(pbData+cbData) = 0;
        printf("%s", (char*)pbData);
    }

    return TRUE;
}

void EncodeMessageWithStream(LPWSTR pwszSignerName)
{
    //---------------------------------------------------------------
    // Declare and initialize variables. This includes declaring and 
    // initializing a pointer to message content to be countersigned 
    // and encoded. Usually, the message content will exist somewhere
    // and a pointer to it is passed to the application. 

    BYTE* pbContent1 = (BYTE*)"First sentence. ";
    DWORD cbContent1 = lstrlenA((char *)pbContent1);
    BYTE* pbContent2 = (BYTE*)"Second sentence. ";
    DWORD cbContent2 = lstrlenA((char *)pbContent2);

    HCRYPTPROV hCryptProv;         // CSP handle
    HCERTSTORE hStoreHandle;       // store handle
    PCCERT_CONTEXT pSignerCert;    // signer certificate
    CMSG_SIGNER_ENCODE_INFO SignerEncodeInfo;
    CMSG_SIGNER_ENCODE_INFO SignerEncodeInfoArray[1];
    CERT_BLOB SignerCertBlob;
    CERT_BLOB SignerCertBlobArray[1];
    CMSG_SIGNED_ENCODE_INFO SignedMsgEncodeInfo;
    HCRYPTMSG hMsg;
    LPWSTR pszNameString;
    DWORD dwKeySpec;

    //---------------------------------------------------------------
    // Open the My system certificate store.

    if(!(hStoreHandle = CertOpenStore(
        // The system store will be a virtual store.
        CERT_STORE_PROV_SYSTEM,
        // Encoding type not needed with this PROV.
        0,
        // Accept the default HCRYPTPROV. 
        NULL,
        CERT_SYSTEM_STORE_CURRENT_USER,
        // Set the system store location in the registry. Other 
        // predefined system stores could have been used, including 
        // trust, Ca, or root.
        L"MY")))                
    {
        MyHandleError(L"Could not open the MY system store.");
    }

    //---------------------------------------------------------------
    // Get a pointer to a signer's signature certificate.

    if(pSignerCert = CertFindCertificateInStore(
        hStoreHandle,
        MY_ENCODING_TYPE,
        0,
        CERT_FIND_SUBJECT_STR,
        pwszSignerName,
        NULL))
    {
        //-----------------------------------------------------------
        //   A certificate was found. Get and print the name of the 
        //   subject of the certificate.

        if(CertGetNameString(
            pSignerCert,
            CERT_NAME_SIMPLE_DISPLAY_TYPE,
            0,
            NULL,
            pszNameString,
            MAX_NAME) > 1)
        {
            printf("The message signer is  %s \n",pszNameString);
        }
        else
        {
            MyHandleError(L"CertGetNameString failed.\n");
        }
    }
    else
    {
        MyHandleError(L"Cert not found.\n");
    }

    //---------------------------------------------------------------
    // Initialize the CMSG_SIGNER_ENCODE_INFO structure.

    //---------------------------------------------------------------
    // Get a handle to a cryptographic provider. 
    if(!(CryptAcquireCertificatePrivateKey(
        pSignerCert,
        0,
        NULL,
        &hCryptProv,
        &dwKeySpec,
        NULL)))
    {
        DWORD dwError = GetLastError();
        if(NTE_BAD_PUBLIC_KEY == dwError)
        {
            printf("NTE_BAD_PUBLIC_KEY\n");
        }

        MyHandleError(L"CryptAcquireContext failed");
    }
     
    memset(&SignerEncodeInfo, 0, sizeof(CMSG_SIGNER_ENCODE_INFO));
    SignerEncodeInfo.cbSize = sizeof(CMSG_SIGNER_ENCODE_INFO);
    SignerEncodeInfo.pCertInfo = pSignerCert->pCertInfo;
    SignerEncodeInfo.hCryptProv = hCryptProv;
    SignerEncodeInfo.dwKeySpec = dwKeySpec;
    SignerEncodeInfo.HashAlgorithm.pszObjId = szOID_RSA_MD5;
    SignerEncodeInfo.pvHashAuxInfo = NULL;

    //---------------------------------------------------------------
    // Initialize the first element of an array of signers. 
    // Note: Currently, there is only one signer.

    SignerEncodeInfoArray[0] = SignerEncodeInfo;

    //---------------------------------------------------------------
    // Initialize the CMSG_SIGNED_ENCODE_INFO structure.

    SignerCertBlob.cbData = pSignerCert->cbCertEncoded;
    SignerCertBlob.pbData = pSignerCert->pbCertEncoded;

    //---------------------------------------------------------------
    //  Initialize the first element of an array of signer BLOBs.
    //  Note: In this program, there is only one signer BLOB used.

    SignerCertBlobArray[0] = SignerCertBlob;
    memset(&SignedMsgEncodeInfo, 0, sizeof(CMSG_SIGNED_ENCODE_INFO));
    SignedMsgEncodeInfo.cbSize = sizeof(CMSG_SIGNED_ENCODE_INFO);
    SignedMsgEncodeInfo.cSigners = 1;
    SignedMsgEncodeInfo.rgSigners = SignerEncodeInfoArray;
    SignedMsgEncodeInfo.cCertEncoded = 1;
    SignedMsgEncodeInfo.rgCertEncoded = SignerCertBlobArray;

    // Fill the CMSG_STREAM_INFO structure.
    CMSG_STREAM_INFO stStreamInfo;

    // BER_ENCODING
    stStreamInfo.cbContent = 0xffffffff;
    // DER_ENCODING 
    // stStreamInfo.cbContent = cbContent;

    stStreamInfo.pfnStreamOutput = EncodeCallback;
    HANDLE hOutMsgFile = INVALID_HANDLE_VALUE;
    hOutMsgFile = CreateFile(
            ENCODED_FILE_NAME,
            GENERIC_WRITE,
            FILE_SHARE_WRITE,
            NULL,
            CREATE_ALWAYS,
            FILE_ATTRIBUTE_NORMAL,
            NULL);
    if (INVALID_HANDLE_VALUE == hOutMsgFile)
    {
        MyHandleError(L"CreateFile (OUT MSG)");
    }

    stStreamInfo.pvArg = &hOutMsgFile; 

    //---------------------------------------------------------------
    // Open a message to encode.

    if(!(hMsg = CryptMsgOpenToEncode(
        MY_ENCODING_TYPE,      // encoding type
        0,                     // flags
        CMSG_SIGNED,           // message type
        &SignedMsgEncodeInfo,  // pointer to structure
        NULL,                  // inner content OID
        &stStreamInfo)))       // stream information
    {
        MyHandleError(L"OpenToEncode failed");
    }

    //---------------------------------------------------------------
    // Update the message with the data.

    if(!(CryptMsgUpdate(
        hMsg,        // handle to the message
        pbContent1,  // pointer to the content
        cbContent1,  // size of the content
        FALSE)))     // first call
    {
        MyHandleError(L"MsgUpdate failed");
    }

    if(!(CryptMsgUpdate(
        hMsg,        // handle to the message
        pbContent2,  // pointer to the content
        cbContent2,  // size of the content
        TRUE)))      // last call
    {
        MyHandleError(L"MsgUpdate failed");
    }

    //---------------------------------------------------------------
    // The message is signed and encoded.
    // Close the message handle and the certificate store.

    CryptMsgClose(hMsg);
    CertCloseStore(hStoreHandle, CERT_CLOSE_STORE_FORCE_FLAG);
    CryptReleaseContext(hCryptProv,0);
    CloseHandle(hOutMsgFile);
}

void DecodeMessageWithStream()
{
    //---------------------------------------------------------------
    // Open the message for decoding.

    HCRYPTMSG hMsg;

    // Fill the CMSG_STREAM_INFO structure.
    CMSG_STREAM_INFO stStreamInfo2;

    // BER_ENCODING
    stStreamInfo2.cbContent = 0xffffffff;
    stStreamInfo2.pfnStreamOutput = DecodeCallback;

    if(!(hMsg = CryptMsgOpenToDecode(
        MY_ENCODING_TYPE,   // encoding type
        0,                  // flags
        0,                  // message type (get from message)
        NULL,               // cryptographic provider
                            // use NULL for the default provider
        NULL,               // recipient information
        &stStreamInfo2)))   // stream information
    {
        MyHandleError(L"OpenToDecode failed.");
    }

    HANDLE hInMsgFile = INVALID_HANDLE_VALUE;
    hInMsgFile = CreateFile(
            ENCODED_FILE_NAME,
            GENERIC_READ,
            FILE_SHARE_READ,
            NULL,
            OPEN_EXISTING,
            FILE_ATTRIBUTE_NORMAL,
            NULL);
    if (INVALID_HANDLE_VALUE == hInMsgFile)
    {
        MyHandleError(L"CreateFile (IN MSG)");
    }

    const DWORD cbBytesToRead = 256;
    byte pbEncodedBlob[cbBytesToRead];
    DWORD cbBytesRead;
    BOOL lastCall = FALSE;

    while (ReadFile(
        hInMsgFile,
        pbEncodedBlob,
        cbBytesToRead,
        &cbBytesRead,
        NULL))
    {
        if (cbBytesRead < cbBytesToRead)
        {
            lastCall = TRUE;
        }

        if(!(CryptMsgUpdate(
            hMsg,            // handle to the message
            pbEncodedBlob,   // pointer to the encoded BLOB
            cbBytesRead,     // size of the encoded BLOB
            lastCall)))      // last call
        {
            MyHandleError(L"Decode MsgUpdate failed.");
        }

        if (lastCall)
        {
            break;
        }
    }

    CryptMsgClose(hMsg);
    CloseHandle(hInMsgFile);
}
```



 

 
