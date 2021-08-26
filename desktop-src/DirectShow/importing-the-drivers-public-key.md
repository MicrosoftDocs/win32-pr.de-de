---
description: Importieren des öffentlichen Schlüssels für Treiber
ms.assetid: 9bab0e43-6e9f-4cdb-bfd0-cdafcc12d526
title: Importieren des öffentlichen Schlüssels für Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebaa4d2d6b5de54eec5ef40070c5ecfb805494a2e937cbbc709f4e44656f55f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042845"
---
# <a name="importing-the-drivers-public-key"></a>Importieren des öffentlichen Schlüssels für Treiber

Der öffentliche RSA-Schlüssel des Treibers ist in den Tags Modulus und Exponent des Blattknotens des Zertifikats enthalten. Beide Werte sind base64-codiert und müssen decodiert werden. Wenn Sie die CryptoAPI von Microsoft verwenden, müssen Sie den Schlüssel in einen Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) importieren. Dabei handelt es sich um das Modul, das die kryptografischen Algorithmen implementiert.

Verwenden Sie die **CryptStringToBinary-Funktion,** wie im folgenden Code gezeigt, um die Modulus und Exponenten aus der Base64-Codierung in binäre Arrays zu konvertieren. Rufen Sie die Funktion einmal auf, um die Größe des Bytearrays abzurufen. Ordnen Sie dann den Puffer zu, und rufen Sie die Funktion erneut auf.


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



Das Base64-codierte Array befindet sich in Big-Endian-Reihenfolge, während die CryptoAPI die Zahl in Little-Endian-Reihenfolge erwartet. Daher müssen Sie die Bytereihenfolge des Arrays austauschen, das von **CryptStringToBinary** zurückgegeben wird. Der Modulus beträgt 256 Bytes, aber das decodierte Bytearray kann kleiner als 256 Bytes sein. Wenn ja, müssen Sie ein neues Array mit 256 Bytes zuordnen, die Daten in das neue Array kopieren und die Front des Arrays mit Nullen aufgefüllt. Der Exponent ist ein DWORD-Wert (4 Byte).

Nachdem Sie über die Modulus- und Exponentenwerte verfügen, können Sie den Schlüssel in den Standardmäßigen Kryptografiedienstanbieter (CSP) importieren, wie im folgenden Code gezeigt:


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



Jetzt können Sie die CryptoAPI verwenden, um Befehle und Statusanforderungen mit dem öffentlichen Schlüssel des Treibers zu verschlüsseln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Certified Output Protection Protocol (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



