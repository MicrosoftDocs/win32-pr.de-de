---
description: Importieren des öffentlichen Schlüssels für Treiber
ms.assetid: 9bab0e43-6e9f-4cdb-bfd0-cdafcc12d526
title: Importieren des öffentlichen Schlüssels für Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222b9c62bd9babe0a01a0e6a9b3a50747ab3b039
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860357"
---
# <a name="importing-the-drivers-public-key"></a><span data-ttu-id="5299b-103">Importieren des öffentlichen Schlüssels für Treiber</span><span class="sxs-lookup"><span data-stu-id="5299b-103">Importing the Drivers Public Key</span></span>

<span data-ttu-id="5299b-104">Der öffentliche RSA-Schlüssel des Treibers ist in den "Modulus"-und "Exponent"-Tags des Blatt Knotens des Zertifikats enthalten.</span><span class="sxs-lookup"><span data-stu-id="5299b-104">The driver's RSA public key is contained in the Modulus and Exponent tags of the certificate's leaf node.</span></span> <span data-ttu-id="5299b-105">Beide Werte sind Base64-codiert und müssen decodiert werden.</span><span class="sxs-lookup"><span data-stu-id="5299b-105">Both values are base64-encoded and must be decoded.</span></span> <span data-ttu-id="5299b-106">Wenn Sie CryptoAPI von Microsoft verwenden, müssen Sie den Schlüssel in einen Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) importieren, bei dem es sich um das Modul handelt, das die kryptografischen Algorithmen implementiert.</span><span class="sxs-lookup"><span data-stu-id="5299b-106">If you are using Microsoft's CryptoAPI, you must import the key into a cryptographic service provider (CSP), which is the module that implements the cryptographic algorithms.</span></span>

<span data-ttu-id="5299b-107">Um den Modulo und die Exponenten von der Base64-Codierung in binäre Arrays zu konvertieren, verwenden Sie die Funktion " **cryptstringdebinary** ", wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="5299b-107">To convert the modulus and exponents from base64 encoding to binary arrays, use the **CryptStringToBinary** function, as shown in the following code.</span></span> <span data-ttu-id="5299b-108">Ruft die-Funktion einmal auf, um die Größe des Bytearrays abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5299b-108">Call the function once to get the size of the byte array.</span></span> <span data-ttu-id="5299b-109">Weisen Sie dann den Puffer zu, und nennen Sie die Funktion erneut.</span><span class="sxs-lookup"><span data-stu-id="5299b-109">Then allocate the buffer and call the function again.</span></span>


```C++
DWORD cbLen = 0, dwSkip = 0, dwFlags = 0;
::CryptStringToBinary(
   pszModulus,  // String that contains the Base64-encoded modulus.
   cchModulus,  // Length of the string, not including the trailing NULL.
   CRYPT_STRING_BASE64,  // Base64 encoding.
   NULL,     // Do not convert yet. Just calculate the length.
   &cbLen,   // Receives the length of the buffer that is required.
   &dwSkip,  // Receives the number of skipped characters.
   &dwFlags  // Receives flags.
);

// Allocate a new buffer.
BYTE *pbBuffer = new BYTE [cbLen];
::CryptStringToBinary(pszModulus, cchModulus, CRYPT_STRING_BASE64, 
    pbBuffer, &cbLen, &dwSkip, &dwFlags);

// (Repeat these steps for the exponent.)
```



<span data-ttu-id="5299b-110">Das Base64-codierte Array ist in Big-Endian-Reihenfolge, während die CryptoAPI die Zahl in Little-Endian-Reihenfolge erwartet, daher müssen Sie die Byte Reihenfolge des Arrays austauschen, das von " **cryptstringesbinary**" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5299b-110">The base64-encoded array is in big-endian order, whereas the CryptoAPI expects the number in little-endian order, so you need to swap the byte order of the array that is returned from **CryptStringToBinary**.</span></span> <span data-ttu-id="5299b-111">Der Modulo beträgt 256 Bytes, das decodierte Bytearray kann jedoch weniger als 256 Byte betragen.</span><span class="sxs-lookup"><span data-stu-id="5299b-111">The modulus is 256 bytes, but the decoded byte array might be less than 256 bytes.</span></span> <span data-ttu-id="5299b-112">Wenn dies der Fall ist, müssen Sie ein neues Array mit einer Größe von 256 Bytes zuordnen, die Daten in das neue Array kopieren und die Vorderseite des Arrays mit Nullen auffüllen.</span><span class="sxs-lookup"><span data-stu-id="5299b-112">If so, you will need to allocate a new array that is 256 bytes, copy the data into the new array, and pad the front of the array with zeros.</span></span> <span data-ttu-id="5299b-113">Der Exponent ist ein DWORD-Wert (4 Byte).</span><span class="sxs-lookup"><span data-stu-id="5299b-113">The exponent is a DWORD (4-byte) value.</span></span>

<span data-ttu-id="5299b-114">Nachdem Sie die Werte Modulo und Exponent angegeben haben, können Sie den Schlüssel in den Standard-Kryptografiedienstanbieter (CSP) importieren, wie im folgenden Code gezeigt:</span><span class="sxs-lookup"><span data-stu-id="5299b-114">After you have the modulus and exponent values, you can import the key into the default cryptographic service provider (CSP), as shown in the following code:</span></span>


```C++
// Assume the following values exist:
BYTE *pModulus;     // Byte array that contains the modulus.
DWORD cbModulus;    // Size of the modulus in bytes.
DWORD dwExponent;   // Exponent.

// Create a new key container to hold the key. 
::CryptAcquireContext(
    &hCSP,         // Receives a handle to the CSP.
    NULL,          // Use the default key container.
    NULL,          // Use the default CSP.
    PROV_RSA_AES,  // Use the AES provider (public-key algorithm).
    CRYPT_SILENT | CRYPT_NEWKEYSET 
);

// Move the key into the key container. 
// The data format is: PUBLICKEYSTRUC + RSAPUBKEY + key
DWORD cbKeyBlob = cbModulus + sizeof(PUBLICKEYSTRUC) + sizeof(RSAPUBKEY)
BYTE *pBlob = new BYTE[cbKeyBlob];

// Fill in the data.
PUBLICKEYSTRUC *pPublicKey = (PUBLICKEYSTRUC*)pBlob;
pPublicKey->bType = PUBLICKEYBLOB; 
pPublicKey->bVersion = CUR_BLOB_VERSION;  // Always use this value.
pPublicKey->reserved = 0;                 // Must be zero.
pPublicKey->aiKeyAlg = CALG_RSA_KEYX;     // RSA public-key key exchange. 

// The next block of data is the RSAPUBKEY structure.
RSAPUBKEY *pRsaPubKey = (RSAPUBKEY*)(pBlob + sizeof(PUBLICKEYSTRUC));
pRsaPubKey->magic = RSA1;            // Public key.
pRsaPubKey->bitlen = cbModulus * 8;  // Number of bits in the modulus.
pRsaPubKey->pubexp = dwExponent;     // Exponent.

// Copy the modulus into the blob. Put the modulus directly after the
// RSAPUBKEY structure in the blob.
BYTE *pKey = (BYTE*)(pRsaPubkey + sizeof(RSAPUBKEY));
CopyMemory(pKey, pModulus, cbModulus);

// Now import the key.
HCRYPTKEY hRSAKey;  // Receives a handle to the key.
CryptImportKey(hCSP, pBlob, cbKeyBlob, 0, 0, &hRSAKey) 
```



<span data-ttu-id="5299b-115">Nun können Sie die CryptoAPI verwenden, um Befehle und Status Anforderungen mit dem öffentlichen Schlüssel des Treibers zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="5299b-115">Now you can use the CryptoAPI to encrypt commands and status requests with the driver's public key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5299b-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5299b-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5299b-117">Verwenden des Certified Output Protection-Protokolls (COPP)</span><span class="sxs-lookup"><span data-stu-id="5299b-117">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



