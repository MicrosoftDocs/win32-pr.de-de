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
# <a name="importing-the-drivers-public-key"></a>Importieren des öffentlichen Schlüssels für Treiber

Der öffentliche RSA-Schlüssel des Treibers ist in den "Modulus"-und "Exponent"-Tags des Blatt Knotens des Zertifikats enthalten. Beide Werte sind Base64-codiert und müssen decodiert werden. Wenn Sie CryptoAPI von Microsoft verwenden, müssen Sie den Schlüssel in einen Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) importieren, bei dem es sich um das Modul handelt, das die kryptografischen Algorithmen implementiert.

Um den Modulo und die Exponenten von der Base64-Codierung in binäre Arrays zu konvertieren, verwenden Sie die Funktion " **cryptstringdebinary** ", wie im folgenden Code gezeigt. Ruft die-Funktion einmal auf, um die Größe des Bytearrays abzurufen. Weisen Sie dann den Puffer zu, und nennen Sie die Funktion erneut.


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



Das Base64-codierte Array ist in Big-Endian-Reihenfolge, während die CryptoAPI die Zahl in Little-Endian-Reihenfolge erwartet, daher müssen Sie die Byte Reihenfolge des Arrays austauschen, das von " **cryptstringesbinary**" zurückgegeben wird. Der Modulo beträgt 256 Bytes, das decodierte Bytearray kann jedoch weniger als 256 Byte betragen. Wenn dies der Fall ist, müssen Sie ein neues Array mit einer Größe von 256 Bytes zuordnen, die Daten in das neue Array kopieren und die Vorderseite des Arrays mit Nullen auffüllen. Der Exponent ist ein DWORD-Wert (4 Byte).

Nachdem Sie die Werte Modulo und Exponent angegeben haben, können Sie den Schlüssel in den Standard-Kryptografiedienstanbieter (CSP) importieren, wie im folgenden Code gezeigt:


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



Nun können Sie die CryptoAPI verwenden, um Befehle und Status Anforderungen mit dem öffentlichen Schlüssel des Treibers zu verschlüsseln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Certified Output Protection-Protokolls (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



