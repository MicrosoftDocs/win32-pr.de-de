---
description: Im folgenden Beispiel wird eine Nachricht mit dem privaten Schlüssel eines Absenders signiert und die signierte Nachricht mithilfe des öffentlichen Schlüssels eines Empfängers verschlüsselt.
ms.assetid: f2863e4a-d22a-4ff0-91d8-052eeaade14e
title: 'Beispiel-C-Programm: senden und Empfangen einer signierten und verschlüsselten Nachricht'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c2ce7c5ba04d6fb57afbb0c15e32c115dcbd5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866979"
---
# <a name="example-c-program-sending-and-receiving-a-signed-and-encrypted-message"></a><span data-ttu-id="91057-103">Beispiel-C-Programm: senden und Empfangen einer signierten und verschlüsselten Nachricht</span><span class="sxs-lookup"><span data-stu-id="91057-103">Example C Program: Sending and Receiving a Signed and Encrypted Message</span></span>

<span data-ttu-id="91057-104">Im folgenden Beispiel wird eine Nachricht mit dem [*privaten Schlüssel*](../secgloss/p-gly.md) eines Absenders signiert und die signierte Nachricht mithilfe des [*öffentlichen Schlüssels*](../secgloss/p-gly.md)eines Empfängers verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="91057-104">The following example signs a message using a sender's [*private key*](../secgloss/p-gly.md) and encrypts the signed message using a receiver's [*public key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="91057-105">Im Beispiel wird dann die Nachricht mit dem privaten Schlüssel des Empfängers entschlüsselt und die Signatur mit dem öffentlichen Schlüssel des Absenders überprüft.</span><span class="sxs-lookup"><span data-stu-id="91057-105">The example then decrypts the message using the receiver's private key and verifies the signature using the sender's public key.</span></span> <span data-ttu-id="91057-106">Das Zertifikat des Absenders, das den erforderlichen öffentlichen Schlüssel enthält, ist in der verschlüsselten Nachricht enthalten.</span><span class="sxs-lookup"><span data-stu-id="91057-106">The sender's certificate containing the needed public key is included in the encrypted message.</span></span> <span data-ttu-id="91057-107">In diesem Beispiel wird auch die signierte und verschlüsselte Nachricht in eine Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="91057-107">This example also writes the signed and encrypted message to a file.</span></span> <span data-ttu-id="91057-108">Weitere Informationen finden Sie unter [Beispiel C-Programm: Empfangen einer signierten und verschlüsselten Nachricht](example-c-program-receiving-a-signed-and-encrypted-message.md).</span><span class="sxs-lookup"><span data-stu-id="91057-108">For more information, see [Example C Program: Receiving a Signed and Encrypted Message](example-c-program-receiving-a-signed-and-encrypted-message.md).</span></span>

<span data-ttu-id="91057-109">Zum Signieren der Nachricht müssen der private Schlüssel des Signatur Gebers und das Zertifikat des Signatur Gebers verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="91057-109">To sign the message, the signer's private key and the signer's certificate must be available.</span></span> <span data-ttu-id="91057-110">Zum Verschlüsseln der signierten Nachricht muss das Zertifikat eines Empfängers, einschließlich des öffentlichen Schlüssels des Empfängers, verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="91057-110">To encrypt the signed message, a receiver's certificate including the receiver's public key must be available.</span></span>

<span data-ttu-id="91057-111">Der private Schlüssel des Empfängers muss verfügbar sein, damit die Nachricht entschlüsselt werden kann.</span><span class="sxs-lookup"><span data-stu-id="91057-111">To decrypt the message, the receiver's private key must be available.</span></span> <span data-ttu-id="91057-112">Nachdem die Nachricht entschlüsselt wurde, wird die Signatur mithilfe des öffentlichen Schlüssels aus dem Zertifikat überprüft, das in der verschlüsselten Nachricht enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="91057-112">After the message is decrypted, the signature is verified using the public key from the certificate included in the encrypted message.</span></span>

> [!Note]  
> <span data-ttu-id="91057-113">Nicht alle Zertifikate in einem [*Zertifikat Speicher*](../secgloss/c-gly.md) ermöglichen den Zugriff auf den [*privaten Schlüssel*](../secgloss/p-gly.md) , der diesem Zertifikat zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="91057-113">Not all of the certificates in a [*certificate store*](../secgloss/c-gly.md) provide access to the [*private key*](../secgloss/p-gly.md) associated with that certificate.</span></span> <span data-ttu-id="91057-114">Wenn die Nachricht signiert und verschlüsselt ist, muss ein Zertifikat verwendet werden, das zum Signatur Geber mit Zugriff auf den privaten Schlüssel dieses Signatur Gebers gehört.</span><span class="sxs-lookup"><span data-stu-id="91057-114">When the message is signed and encrypted, a certificate belonging to the signer with access to the private key of that signer must be used.</span></span> <span data-ttu-id="91057-115">Außerdem muss der Empfänger der Nachricht Zugriff auf den privaten Schlüssel haben, der dem öffentlichen Schlüssel zugeordnet ist, der zum Verschlüsseln der Nachricht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="91057-115">In addition, the receiver of the message must have access to the private key associated with the public key used to encrypt the message.</span></span>

 

<span data-ttu-id="91057-116">In diesem Beispiel werden die folgenden Aufgaben veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="91057-116">This example illustrates the following tasks:</span></span>

-   <span data-ttu-id="91057-117">Systemzertifikat Speicher werden geöffnet und geschlossen.</span><span class="sxs-lookup"><span data-stu-id="91057-117">Opening and closing system certificate stores.</span></span>
-   <span data-ttu-id="91057-118">Suchen von Zertifikaten für einen Nachrichten Absender und Nachrichtenempfänger im geöffneten Zertifikat Speicher.</span><span class="sxs-lookup"><span data-stu-id="91057-118">Finding certificates for a message sender and message receiver in the open certificate stores.</span></span>
-   <span data-ttu-id="91057-119">Suchen und Drucken des Antragsteller namens aus Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="91057-119">Finding and printing the subject name from certificates.</span></span>
-   <span data-ttu-id="91057-120">Initialisieren von Datenstrukturen, die zum Signieren, verschlüsseln, entschlüsseln und Überprüfen einer Nachricht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="91057-120">Initializing data structures needed to sign, encrypt, decrypt, and verify a message.</span></span>
-   <span data-ttu-id="91057-121">Aufrufen einer CryptoAPI-Funktion, um die erforderliche Größe eines Puffers zu ermitteln, den Puffer der erforderlichen Größe zuzuweisen und die CryptoAPI-Funktion erneut aufzurufende, um den Puffer zu füllen.</span><span class="sxs-lookup"><span data-stu-id="91057-121">Calling a CryptoAPI function to find the required size of a buffer, allocating the buffer of the required size, and calling the CryptoAPI function again to fill the buffer.</span></span> <span data-ttu-id="91057-122">Weitere Informationen finden Sie unter [Abrufen von Daten mit unbekannter Länge](retrieving-data-of-unknown-length.md).</span><span class="sxs-lookup"><span data-stu-id="91057-122">For more information, see [Retrieving Data of Unknown Length](retrieving-data-of-unknown-length.md).</span></span>
-   <span data-ttu-id="91057-123">Anzeigen einiger der verschlüsselten Inhalte eines Puffers.</span><span class="sxs-lookup"><span data-stu-id="91057-123">Displaying some of the encrypted contents of a buffer.</span></span> <span data-ttu-id="91057-124">Die enthaltene lokale Funktion " **showbytes**" zeigt Zeichen im Puffer mit Werten zwischen "0" und "z" an.</span><span class="sxs-lookup"><span data-stu-id="91057-124">The included local function, **ShowBytes**, displays characters in the buffer with values between '0' and 'z'.</span></span> <span data-ttu-id="91057-125">Alle anderen Zeichen werden als "-" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="91057-125">All other characters are displayed as the '-' character.</span></span>

<span data-ttu-id="91057-126">In diesem Beispiel werden die folgenden CryptoAPI-Funktionen verwendet:</span><span class="sxs-lookup"><span data-stu-id="91057-126">This example uses the following CryptoAPI functions:</span></span>

-   [<span data-ttu-id="91057-127">**CertOpenStore übergebene**</span><span class="sxs-lookup"><span data-stu-id="91057-127">**CertOpenStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)
-   [<span data-ttu-id="91057-128">**Certfindcertifi. Store**</span><span class="sxs-lookup"><span data-stu-id="91057-128">**CertFindCertificateInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
-   [<span data-ttu-id="91057-129">**Certgetnamestring**</span><span class="sxs-lookup"><span data-stu-id="91057-129">**CertGetNameString**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)
-   [<span data-ttu-id="91057-130">**CryptAcquireCertificatePrivateKey**</span><span class="sxs-lookup"><span data-stu-id="91057-130">**CryptAcquireCertificatePrivateKey**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecertificateprivatekey)
-   [<span data-ttu-id="91057-131">**Cryptsignandverschlüsseltmessage**</span><span class="sxs-lookup"><span data-stu-id="91057-131">**CryptSignAndEncryptMessage**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencryptmessage)
-   [<span data-ttu-id="91057-132">**Cryptdecryptandveriatymessagesignature**</span><span class="sxs-lookup"><span data-stu-id="91057-132">**CryptDecryptAndVerifyMessageSignature**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature)
-   [<span data-ttu-id="91057-133">**Certfreecertififeecontext**</span><span class="sxs-lookup"><span data-stu-id="91057-133">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext)
-   [<span data-ttu-id="91057-134">**Certclosestore**</span><span class="sxs-lookup"><span data-stu-id="91057-134">**CertCloseStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)

<span data-ttu-id="91057-135">In diesem Beispiel werden separate Funktionen verwendet, um den Signatur-/Verschlüsselungsprozess und den Entschlüsselungs-/Signatur Überprüfungsprozess anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="91057-135">This example uses separate functions to show the signing/encryption process and the decryption/signature-verification process.</span></span> <span data-ttu-id="91057-136">Außerdem wird [**mylenker Error**](myhandleerror.md) verwendet, um das Programm im Falle eines Fehlers ordnungsgemäß zu beenden.</span><span class="sxs-lookup"><span data-stu-id="91057-136">It also uses [**MyHandleError**](myhandleerror.md) to exit the program gracefully in case of any failure.</span></span> <span data-ttu-id="91057-137">Der Code **myhanderror** ist im Beispiel enthalten und kann auch zusammen mit anderen Hilfsfunktionen unter [universell Funktionen](general-purpose-functions.md)gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="91057-137">The code **MyHandleError** is included with the example and can also be found along with other auxiliary functions under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
//-------------------------------------------------------------------
// Example C Program: 
// Signs a message by using a sender's private key and encrypts the
// signed message by using a receiver's public key.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <Wincrypt.h>

#define MY_ENCODING_TYPE (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
#define MAX_NAME  128

//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// SIGNER_NAME is used with the CertFindCertificateInStore  
// function to retrieve the certificate of the message signer.
// Replace the Unicode string below with the certificate subject 
// name of the message signer.

#define SIGNER_NAME L"DUMMY_SIGNER_NAME"

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the standard  
//  error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
    exit(1);
} // End of MyHandleError.

//-------------------------------------------------------------------
// The local function ShowBytes is declared here and defined after 
// main.

void ShowBytes(BYTE *s, DWORD len);

//-------------------------------------------------------------------
// Declare local functions SignAndEncrypt, DecryptAndVerify, and 
// WriteSignedAndEncryptedBlob.
// These functions are defined after main.

BYTE* SignAndEncrypt(
     const BYTE     *pbToBeSignedAndEncrypted,
     DWORD          cbToBeSignedAndEncrypted,
     DWORD          *pcbSignedAndEncryptedBlob);

BYTE* DecryptAndVerify(
     BYTE  *pbSignedAndEncryptedBlob,
     DWORD  cbSignedAndEncryptedBlob);

void WriteSignedAndEncryptedBlob(
     DWORD  cbBlob,
     BYTE   *pbBlob);

void main (void)
{
    //---------------------------------------------------------------
    // Declare and initialize local variables.

    //---------------------------------------------------------------
    //  pbToBeSignedAndEncrypted is the message to be 
    //  encrypted and signed.

    const BYTE *pbToBeSignedAndEncrypted =
            (const unsigned char *)"Insert the message to be signed "
            "here";
    //---------------------------------------------------------------
    // This is the length of the message to be
    // encrypted and signed. Note that it is one
    // more that the length returned by strlen()
    // to include the terminating null character.

    DWORD cbToBeSignedAndEncrypted = 
        lstrlenA((const char *)pbToBeSignedAndEncrypted) + 1;

    //---------------------------------------------------------------
    // Pointer to a buffer that will hold the
    // encrypted and signed message.

    BYTE *pbSignedAndEncryptedBlob;

    //---------------------------------------------------------------
    // A DWORD to hold the length of the signed 
    // and encrypted message.

    DWORD cbSignedAndEncryptedBlob;
    BYTE *pReturnMessage;

    //---------------------------------------------------------------
    // Call the local function SignAndEncrypt.
    // This function returns a pointer to the 
    // signed and encrypted BLOB and also returns
    // the length of that BLOB.

    pbSignedAndEncryptedBlob = SignAndEncrypt(
        pbToBeSignedAndEncrypted,
        cbToBeSignedAndEncrypted,
        &cbSignedAndEncryptedBlob);

    _tprintf(TEXT("The following is the signed and encrypted ")
        TEXT("message.\n"));
    ShowBytes(pbSignedAndEncryptedBlob,cbSignedAndEncryptedBlob/4);

    // Open a file and write the signed and 
    // encrypted message to the file.

    WriteSignedAndEncryptedBlob(
        cbSignedAndEncryptedBlob,
        pbSignedAndEncryptedBlob);

    //---------------------------------------------------------------
    // Call the local function DecryptAndVerify.
    // This function decrypts and displays the 
    // encrypted message and also verifies the 
    // message's signature.
       
    if(pReturnMessage = DecryptAndVerify(
        pbSignedAndEncryptedBlob,
        cbSignedAndEncryptedBlob))
    {
        _tprintf(TEXT(" The returned, verified message is ->\n%s\n"),
            pReturnMessage);
        _tprintf(TEXT(" The program executed without error.\n"));
    }
    else
    {
        _tprintf(TEXT("Verification failed.\n"));
    }

} // End Main.

//-------------------------------------------------------------------
// Begin definition of the SignAndEncrypt function.

BYTE* SignAndEncrypt(
     const BYTE *pbToBeSignedAndEncrypted,
     DWORD cbToBeSignedAndEncrypted,
     DWORD *pcbSignedAndEncryptedBlob)
{
    //---------------------------------------------------------------
    // Declare and initialize local variables.

    FILE *hToSave;
    HCERTSTORE hCertStore;

    //---------------------------------------------------------------
    // pSignerCertContext will be the certificate of 
    // the message signer.

    PCCERT_CONTEXT pSignerCertContext ;

    //---------------------------------------------------------------
    // pReceiverCertContext will be the certificate of the 
    // message receiver.

    PCCERT_CONTEXT pReceiverCertContext;

    TCHAR pszNameString[256];
    CRYPT_SIGN_MESSAGE_PARA SignPara;
    CRYPT_ENCRYPT_MESSAGE_PARA EncryptPara;
    DWORD cRecipientCert;
    PCCERT_CONTEXT rgpRecipientCert[5];
    BYTE *pbSignedAndEncryptedBlob = NULL;
    CERT_NAME_BLOB Subject_Blob;
    BYTE *pbDataIn;
    DWORD dwKeySpec;
    HCRYPTPROV hCryptProv;

    //---------------------------------------------------------------
    // Open the MY certificate store. 
    // For more information, see the CertOpenStore function 
    // PSDK reference page. 
    // Note: Case is not significant in certificate store names.

    if ( !( hCertStore = CertOpenStore(
        CERT_STORE_PROV_SYSTEM,
        0,
        NULL,
        CERT_SYSTEM_STORE_CURRENT_USER,
        L"my")))
    {
        MyHandleError(TEXT("The MY store could not be opened."));
    }

    //---------------------------------------------------------------
    // Get the certificate for the signer.

    if(!(pSignerCertContext = CertFindCertificateInStore(
        hCertStore,
        MY_ENCODING_TYPE,
        0,
        CERT_FIND_SUBJECT_STR,
        SIGNER_NAME,
        NULL)))
    {
        MyHandleError(TEXT("Cert not found.\n"));
    }

    //---------------------------------------------------------------
    // Get and print the name of the message signer.
    // The following two calls to CertGetNameString with different
    // values for the second parameter get two different forms of 
    // the certificate subject's name.

    if(CertGetNameString(
        pSignerCertContext ,
        CERT_NAME_SIMPLE_DISPLAY_TYPE,
        0,
        NULL,
        pszNameString,
        MAX_NAME) > 1)
    {
        _tprintf(
            TEXT("The SIMPLE_DISPLAY_TYPE message signer's name is ")
            TEXT("%s \n"),
            pszNameString);
    }
    else
    {
        MyHandleError(
            TEXT("Getting the name of the signer failed.\n"));
    }

    if(CertGetNameString(
        pSignerCertContext,
        CERT_NAME_RDN_TYPE,
        0,
        NULL,
        pszNameString,
        MAX_NAME) > 1)
    {
        _tprintf(
            TEXT("The RDM_TYPE message signer's name is %s \n"),
            pszNameString);
    }
    else
    {
        MyHandleError(
            TEXT("Getting the name of the signer failed.\n"));
    }

    if(!( CryptAcquireCertificatePrivateKey(
        pSignerCertContext,
        0,
        NULL,
        &hCryptProv,
        &dwKeySpec,
        NULL)))
    {
        MyHandleError(TEXT("CryptAcquireCertificatePrivateKey.\n"));
    }

    //---------------------------------------------------------------
    // Get the certificate for the receiver. In this case,  
    // a BLOB with the name of the receiver is saved in a file.

    // Note: To decrypt the message signed and encrypted here,
    // this program must use the certificate of the intended
    // receiver. The signed and encrypted message can only be
    // decrypted and verified by the owner of the recipient
    // certificate. That user must have access to the private key
    // associated with the public key of the recipient's certificate.

    // To run this sample, the file contains information that allows 
    // the program to find one of the current user's certificates. 
    // The current user should have access to the private key of the
    // certificate and thus can test the verification and decryption. 

    // In normal use, the file would contain information used to find
    // the certificate of an intended receiver of the message. 
    // The signed and encrypted message would be written
    // to a file or otherwise sent to the intended receiver.

    //---------------------------------------------------------------
    // Open a file and read in the receiver name
    // BLOB.


    if( !(hToSave= fopen("s.txt","rb")))
    {
        MyHandleError(TEXT("Source file was not opened.\n"));
    }

    fread(
        &(Subject_Blob.cbData),
        sizeof(DWORD),
        1,
        hToSave);

    if(ferror(hToSave))
    {
        MyHandleError(TEXT("The size of the BLOB was not read.\n"));
    }

    if(!(pbDataIn = (BYTE *) malloc(Subject_Blob.cbData)))
    {
        MyHandleError(TEXT("Memory allocation error."));
    }

    fread(
        pbDataIn,
        Subject_Blob.cbData,
        1,
        hToSave);

    if(ferror(hToSave))
    {
        MyHandleError(TEXT("BLOB not read."));
    }

    fclose(hToSave);

    Subject_Blob.pbData = pbDataIn;

    //---------------------------------------------------------------
    // Use the BLOB just read in from the file to find its associated
    // certificate in the MY store.
    // This call to CertFindCertificateInStore uses the
    // CERT_FIND_SUBJECT_NAME dwFindType.

    if(!(pReceiverCertContext = CertFindCertificateInStore(
        hCertStore,
        MY_ENCODING_TYPE,
        0,
        CERT_FIND_SUBJECT_NAME,
        &Subject_Blob,
        NULL)))
    {
        MyHandleError(TEXT("Receiver certificate not found."));
    }

    //---------------------------------------------------------------
    // Get and print the subject name from the receiver's
    // certificate.

    if(CertGetNameString(
        pReceiverCertContext ,
        CERT_NAME_SIMPLE_DISPLAY_TYPE,
        0,
        NULL,
        pszNameString,
        MAX_NAME) > 1)
    {
        _tprintf(TEXT("The message receiver is  %s \n"), 
            pszNameString);
    }
    else
    {
        MyHandleError(
            TEXT("Getting the name of the receiver failed.\n"));
    }

    //---------------------------------------------------------------
    // Initialize variables and data structures
    // for the call to CryptSignAndEncryptMessage.

    SignPara.cbSize = sizeof(CRYPT_SIGN_MESSAGE_PARA);
    SignPara.dwMsgEncodingType = MY_ENCODING_TYPE;
    SignPara.pSigningCert = pSignerCertContext ;
    SignPara.HashAlgorithm.pszObjId = szOID_RSA_MD2;
    SignPara.HashAlgorithm.Parameters.cbData = 0;
    SignPara.pvHashAuxInfo = NULL;
    SignPara.cMsgCert = 1;
    SignPara.rgpMsgCert = &pSignerCertContext ;
    SignPara.cMsgCrl = 0;
    SignPara.rgpMsgCrl = NULL;
    SignPara.cAuthAttr = 0;
    SignPara.rgAuthAttr = NULL;
    SignPara.cUnauthAttr = 0;
    SignPara.rgUnauthAttr = NULL;
    SignPara.dwFlags = 0;
    SignPara.dwInnerContentType = 0;

    EncryptPara.cbSize = sizeof(CRYPT_ENCRYPT_MESSAGE_PARA);
    EncryptPara.dwMsgEncodingType = MY_ENCODING_TYPE;
    EncryptPara.hCryptProv = 0;
    EncryptPara.ContentEncryptionAlgorithm.pszObjId = szOID_RSA_RC4;
    EncryptPara.ContentEncryptionAlgorithm.Parameters.cbData = 0;
    EncryptPara.pvEncryptionAuxInfo = NULL;
    EncryptPara.dwFlags = 0;
    EncryptPara.dwInnerContentType = 0;

    cRecipientCert = 1;
    rgpRecipientCert[0] = pReceiverCertContext;
    *pcbSignedAndEncryptedBlob = 0;
    pbSignedAndEncryptedBlob = NULL;

    if( CryptSignAndEncryptMessage(
        &SignPara,
        &EncryptPara,
        cRecipientCert,
        rgpRecipientCert,
        pbToBeSignedAndEncrypted,
        cbToBeSignedAndEncrypted,
        NULL, // the pbSignedAndEncryptedBlob
        pcbSignedAndEncryptedBlob))
    {
        _tprintf(TEXT("%d bytes for the buffer .\n"),
            *pcbSignedAndEncryptedBlob);
    }
    else
    {
        MyHandleError(TEXT("Getting the buffer length failed."));
    }

    //---------------------------------------------------------------
    // Allocate memory for the buffer.

    if(!(pbSignedAndEncryptedBlob = 
        (unsigned char *)malloc(*pcbSignedAndEncryptedBlob)))
    {
        MyHandleError(TEXT("Memory allocation failed."));
    }

    //---------------------------------------------------------------
    // Call the function a second time to copy the signed and 
    // encrypted message into the buffer.

    if( CryptSignAndEncryptMessage(
        &SignPara,
        &EncryptPara,
        cRecipientCert,
        rgpRecipientCert,
        pbToBeSignedAndEncrypted,
        cbToBeSignedAndEncrypted,
        pbSignedAndEncryptedBlob,
        pcbSignedAndEncryptedBlob))
    {
        _tprintf(TEXT("The message is signed and encrypted.\n"));
    }
    else
    {
        MyHandleError(
            TEXT("The message failed to sign and encrypt."));
    }

    //---------------------------------------------------------------
    // Clean up.

    if(pSignerCertContext )
    {
        CertFreeCertificateContext(pSignerCertContext);
    }
    
    if(pReceiverCertContext )
    {
        CertFreeCertificateContext(pReceiverCertContext);
    }
    
    CertCloseStore(hCertStore, 0);

    //---------------------------------------------------------------
    // Return the signed and encrypted message.

    return pbSignedAndEncryptedBlob;

}  // End SignAndEncrypt.

//-------------------------------------------------------------------
// Define the DecryptAndVerify function.

BYTE* DecryptAndVerify(
     BYTE  *pbSignedAndEncryptedBlob,
     DWORD  cbSignedAndEncryptedBlob)
{
    //---------------------------------------------------------------
    // Declare and initialize local variables.

    HCERTSTORE hCertStore;
    CRYPT_DECRYPT_MESSAGE_PARA DecryptPara;
    CRYPT_VERIFY_MESSAGE_PARA VerifyPara;
    DWORD dwSignerIndex = 0;
    BYTE *pbDecrypted;
    DWORD cbDecrypted;

    //---------------------------------------------------------------
    // Open the certificate store.

    if ( !( hCertStore = CertOpenStore(
        CERT_STORE_PROV_SYSTEM,
        0,
        NULL,
        CERT_SYSTEM_STORE_CURRENT_USER,
        L"my")))
    {
        MyHandleError(TEXT("The MY store could not be opened."));
    }

    //---------------------------------------------------------------
    // Initialize the needed data structures.

    DecryptPara.cbSize = sizeof(CRYPT_DECRYPT_MESSAGE_PARA);
    DecryptPara.dwMsgAndCertEncodingType = MY_ENCODING_TYPE;
    DecryptPara.cCertStore = 1;
    DecryptPara.rghCertStore = &hCertStore;

    VerifyPara.cbSize = sizeof(CRYPT_VERIFY_MESSAGE_PARA);
    VerifyPara.dwMsgAndCertEncodingType = MY_ENCODING_TYPE;
    VerifyPara.hCryptProv = 0;
    VerifyPara.pfnGetSignerCertificate = NULL;
    VerifyPara.pvGetArg = NULL;
    pbDecrypted = NULL;
    cbDecrypted = 0;

    //---------------------------------------------------------------
    // Call CryptDecryptAndVerifyMessageSignature a first time
    // to determine the needed size of the buffer to hold the 
    // decrypted message.

    if(!(CryptDecryptAndVerifyMessageSignature(
        &DecryptPara,
        &VerifyPara,
        dwSignerIndex,
        pbSignedAndEncryptedBlob,
        cbSignedAndEncryptedBlob,
        NULL,           // pbDecrypted
        &cbDecrypted,
        NULL,
        NULL)))
    {
        MyHandleError(TEXT("Failed getting size."));
    }

    //---------------------------------------------------------------
    // Allocate memory for the buffer to hold the decrypted
    // message.

    if(!(pbDecrypted = (BYTE *)malloc(cbDecrypted)))
    {
        MyHandleError(TEXT("Memory allocation failed."));
    }

    if(!(CryptDecryptAndVerifyMessageSignature(
        &DecryptPara,
        &VerifyPara,
        dwSignerIndex,
        pbSignedAndEncryptedBlob,
        cbSignedAndEncryptedBlob,
        pbDecrypted,
        &cbDecrypted,
        NULL,
        NULL)))
    {
        pbDecrypted = NULL;
    }

    //---------------------------------------------------------------
    // Close the certificate store.

    CertCloseStore(
        hCertStore,
        0);

    //---------------------------------------------------------------
    // Return the decrypted string or NULL.

    return pbDecrypted;

} // End of DecryptandVerify.

//-------------------------------------------------------------------
// Define the MyHandleError function.

void WriteSignedAndEncryptedBlob(
     DWORD cbBlob,
     BYTE *pbBlob)
{
    // Open an output file, write the file, and close the file.
    // This function would be used to save the signed and encrypted 
    // message to a file that would be sent to the intended receiver.
    // Note: The only receiver able to decrypt and verify this
    // message will have access to the private key associated 
    // with the public key from the certificate used when 
    // the message was encrypted.

    FILE *hOutputFile;

    if( !(hOutputFile = _tfopen(TEXT("sandvout.txt"), TEXT("wb"))))
    {
        MyHandleError(TEXT("Output file was not opened.\n"));
    }

    fwrite(
        &cbBlob,
        sizeof(DWORD),
        1,
        hOutputFile);

    if(ferror(hOutputFile))
    {
        MyHandleError(
            TEXT("The size of the BLOB was not written.\n"));
    }

    fwrite(
        pbBlob,
        cbBlob,
        1,
        hOutputFile);

    if(ferror(hOutputFile))
    {
        MyHandleError(
            TEXT("The bytes of the BLOB were not written.\n"));
    }
    else
    {
        _tprintf(TEXT("The BLOB has been written to the file.\n"));
    }
    
    fclose(hOutputFile);
}  // End of WriteSignedAndEcryptedBlob.


//-------------------------------------------------------------------
// Define the ShowBytes function.
// This function displays the contents of a BYTE buffer. Characters
// less than '0' or greater than 'z' are all displayed as '-'.

void ShowBytes(BYTE *s, DWORD len)
{
    DWORD TotalChars = 0;
    DWORD ThisLine = 0;

    while(TotalChars < len)
    {
        if(ThisLine > 70)
        {
            ThisLine = 0;
            _tprintf(TEXT("\n"));
        }
        if( s[TotalChars] < '0' || s[TotalChars] > 'z')
        {
            _tprintf(TEXT("-"));
        }
        else
        {
            _tprintf(TEXT("%c"), s[TotalChars]);
        }

        TotalChars++;
        ThisLine++;
    }

    _tprintf(TEXT("\n"));
} // End of ShowBytes.

```



 

 
