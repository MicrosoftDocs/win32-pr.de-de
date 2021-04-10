---
description: Initiieren einer COPP-Sitzung
ms.assetid: c84a83b4-51b2-4b46-860f-d740b42323fa
title: Initiieren einer COPP-Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d64ef848874aee95d3f928a5b8bb637323a92a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125084"
---
# <a name="initiating-a-copp-session"></a>Initiieren einer COPP-Sitzung

Zum Initiieren einer zertifizierten COPP-Sitzung (Output Protection Protocol) müssen Sie eine *Signatur* vorbereiten. Hierbei handelt es sich um ein Array, das die Verkettung der folgenden Zahlen enthält:

-   Die vom Treiber zurückgegebene 128-Bit-Zufallszahl. (Dieser Wert wird bei [der Beschaffung der Zertifikat Kette des Treibers](obtaining-the-drivers-certificate-chain.md)als *guidrandom* angezeigt.)
-   Ein symmetrischer 128-Bit-AES-Schlüssel.
-   Eine 32-Bit-Startsequenz Nummer für Status Anforderungen.
-   Eine 32-Bit-Startsequenz Nummer für COPP-Befehle.

Generieren Sie einen symmetrischen AES-Schlüssel wie folgt:


```C++
DWORD dwFlag = 0x80;         // Bit length: 128-bit AES.
dwFlag <<= 16;               // Move this value to the upper 16 bits.
dwFlag |= CRYPT_EXPORTABLE;  // We want to export the key.
CryptGenKey(
    hCSP,           // Handle to the CSP.
    CALG_AES_128,   // Use 128-bit AES block encryption algorithm.
    dwFlag,
    &m_hAESKey      // Receives a handle to the AES key.
);
```



Die **CryptGenKey** -Funktion erstellt den symmetrischen Schlüssel, der Schlüssel ist jedoch weiterhin im CSP gespeichert. Um den Schlüssel in ein Bytearray zu exportieren, verwenden Sie die **CryptExportKey** -Funktion. Dies ist der Grund für die Verwendung des \_ exportierbaren Crypt-Flags beim Aufrufen von **CryptGenKey**. Der folgende Code exportiert den Schlüssel und kopiert ihn in das


```
pData
```



Array.


```C++
DWORD cbData = 0; 
BYTE *pData = NULL;
// Get the size of the blob.
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, NULL, &cbData);  

// Allocate the array and call again.
pData = new BYTE[cbData];
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, pData, &cbData);  
```



Die in zurückgegebenen Daten


```
pData
```



hat das folgende Layout:


```C++
BLOBHEADER header
DWORD      cbSize
BYTE       key[]
```



Allerdings wird keine mit diesem Layout übereinstimmende Struktur in den CryptoAPI-Headern definiert. Sie können entweder einen definieren oder eine Zeigerarithmetik ausführen. Um z. b. die Größe des Schlüssels zu überprüfen:


```C++
DWORD *pcbKey = (DWORD*)(pData + sizeof(BLOBHEADER));
if (*pcbKey != 16)
{
    // Wrong size! Should be 16 bytes (128 bits).
}
```



So erhalten Sie den Zeiger auf den Schlüssel selbst:


```C++
BYTE *pKey = pData + sizeof(BLOBHEADER) + sizeof(DWORD);
```



Generieren Sie als nächstes eine 32-Bit-Zufallszahl, die als Startsequenz für COPP-Status Anforderungen verwendet werden soll. Die empfohlene Vorgehensweise zum Erstellen einer Zufallszahl ist das Aufrufen der Funktion **cryptgenrandom** . Verwenden Sie die **Rand** -Funktion nicht in der C-Lauf Zeit Bibliothek, da Sie nicht wirklich zufällig ist. Generieren Sie eine zweite 32-Bit-Zufallszahl, die als Startsequenz für COPP-Befehle verwendet werden soll.


```C++
UINT uStatusSeq;     // Status sequence number.
UINT uCommandSeq;    // Command sequence number.
CryptGenRandom(hCSP, sizeof(UINT), &uStatusSeq);
CryptGenRandom(hCSP, sizeof(UINT), &uCommandSeq);
```



Nun können Sie die COPP-Signatur vorbereiten. Dies ist ein 256-Byte-Array, das als [**amcoppsignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) -Struktur definiert ist. Initialisieren Sie den Inhalt des Arrays mit 0 (null). Kopieren Sie dann die vier Zahlen in das Array – die Zufallszahl des Treibers, den AES-Schlüssel, die Status Sequenznummer und die Befehlssequenz Nummer in dieser Reihenfolge. Tauschen Sie schließlich die Byte Reihenfolge des gesamten Arrays aus.

Gemäß der Dokumentation für **CryptEncrypt**:

<dl> "Die Länge von Klartext-Daten, die mit einem" **CryptEncrypt** "-Rückruf mit einem RSA-Schlüssel verschlüsselt werden können, ist die Länge des Schlüsselmodulus minus elf bytes. Die elf Bytes werden als Minimalwert für die Auffüll Dauer von PKCS \# 1 ausgewählt. "  
</dl>

In diesem Fall ist der Modulo 256 Bytes, daher beträgt die maximale Nachrichten Länge 245 bytes (256 – 11). Die **amcoppsignature** -Struktur ist 256 Byte, aber die aussagekräftigen Daten in der Signatur sind nur 40 Bytes. Mit dem folgenden Code wird die Signatur verschlüsselt und das Ergebnis in bereitstellt.


```
CoppSig
```



.


```C++
AMCOPPSignature CoppSig;
ZeroMemory(&CoppSig, sizeof(CoppSig));
// Copy the signature data into CoppSig. (Not shown.)

// Encrypt the signature:
const DWORD RSA_PADDING = 11;    // 11-byte padding.
DWORD cbDataOut = sizeof(AMCOPPSignature);
DWORD cbDataIn = cbDataOut - RSA_PADDING;
CryptEncrypt(
    hRSAKey, 
    NULL,     // No hash object.
    TRUE,     // Final block to encrypt.
    0,        // Reserved.
    &CoppSig, // COPP signature.
    &cbDataOut, 
    cbDataIn
);
```



Übergeben Sie nun das verschlüsselte Array an [**iamcertifiedoutputprotection:: sessionsequencestart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):


```C++
hr = pCOPP->SessionSequenceStart(&CoppSig);
if (SUCCEEDED(hr))
{
    // Ready to send COPP commands and status requests.
}
```



Wenn diese Methode erfolgreich ausgeführt wird, können Sie COPP-Befehle und-Status Anforderungen an den Treiber senden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Certified Output Protection-Protokolls (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



