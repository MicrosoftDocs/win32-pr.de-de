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
# <a name="initiating-a-copp-session"></a><span data-ttu-id="0f1ef-103">Initiieren einer COPP-Sitzung</span><span class="sxs-lookup"><span data-stu-id="0f1ef-103">Initiating a COPP Session</span></span>

<span data-ttu-id="0f1ef-104">Zum Initiieren einer zertifizierten COPP-Sitzung (Output Protection Protocol) müssen Sie eine *Signatur* vorbereiten. Hierbei handelt es sich um ein Array, das die Verkettung der folgenden Zahlen enthält:</span><span class="sxs-lookup"><span data-stu-id="0f1ef-104">To initiate a Certified Output Protection Protocol (COPP) session, you must prepare a *signature*, which is an array that contains the concatenation of the following numbers:</span></span>

-   <span data-ttu-id="0f1ef-105">Die vom Treiber zurückgegebene 128-Bit-Zufallszahl.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-105">The 128-bit random number returned by the driver.</span></span> <span data-ttu-id="0f1ef-106">(Dieser Wert wird bei [der Beschaffung der Zertifikat Kette des Treibers](obtaining-the-drivers-certificate-chain.md)als *guidrandom* angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="0f1ef-106">(This value is shown as *guidRandom* in [Obtaining the Driver's Certificate Chain](obtaining-the-drivers-certificate-chain.md).)</span></span>
-   <span data-ttu-id="0f1ef-107">Ein symmetrischer 128-Bit-AES-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-107">A 128-bit symmetric AES key.</span></span>
-   <span data-ttu-id="0f1ef-108">Eine 32-Bit-Startsequenz Nummer für Status Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-108">A 32-bit starting sequence number for status requests.</span></span>
-   <span data-ttu-id="0f1ef-109">Eine 32-Bit-Startsequenz Nummer für COPP-Befehle.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-109">A 32-bit starting sequence number for COPP commands.</span></span>

<span data-ttu-id="0f1ef-110">Generieren Sie einen symmetrischen AES-Schlüssel wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0f1ef-110">Generate a symmetric AES key as follows:</span></span>


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



<span data-ttu-id="0f1ef-111">Die **CryptGenKey** -Funktion erstellt den symmetrischen Schlüssel, der Schlüssel ist jedoch weiterhin im CSP gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-111">The **CryptGenKey** function creates the symmetric key, but the key is still held in the CSP.</span></span> <span data-ttu-id="0f1ef-112">Um den Schlüssel in ein Bytearray zu exportieren, verwenden Sie die **CryptExportKey** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-112">To export the key into a byte array, use the **CryptExportKey** function.</span></span> <span data-ttu-id="0f1ef-113">Dies ist der Grund für die Verwendung des \_ exportierbaren Crypt-Flags beim Aufrufen von **CryptGenKey**.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-113">This is the reason for using the CRYPT\_EXPORTABLE flag when calling **CryptGenKey**.</span></span> <span data-ttu-id="0f1ef-114">Der folgende Code exportiert den Schlüssel und kopiert ihn in das</span><span class="sxs-lookup"><span data-stu-id="0f1ef-114">The following code exports the key and copies it into the</span></span>


```
pData
```



<span data-ttu-id="0f1ef-115">Array.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-115">array.</span></span>


```C++
DWORD cbData = 0; 
BYTE *pData = NULL;
// Get the size of the blob.
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, NULL, &cbData);  

// Allocate the array and call again.
pData = new BYTE[cbData];
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, pData, &cbData);  
```



<span data-ttu-id="0f1ef-116">Die in zurückgegebenen Daten</span><span class="sxs-lookup"><span data-stu-id="0f1ef-116">The data returned in</span></span>


```
pData
```



<span data-ttu-id="0f1ef-117">hat das folgende Layout:</span><span class="sxs-lookup"><span data-stu-id="0f1ef-117">has the following layout:</span></span>


```C++
BLOBHEADER header
DWORD      cbSize
BYTE       key[]
```



<span data-ttu-id="0f1ef-118">Allerdings wird keine mit diesem Layout übereinstimmende Struktur in den CryptoAPI-Headern definiert.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-118">However, no structure that matches this layout is defined in the CryptoAPI headers.</span></span> <span data-ttu-id="0f1ef-119">Sie können entweder einen definieren oder eine Zeigerarithmetik ausführen.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-119">You can either define one or do some pointer arithmetic.</span></span> <span data-ttu-id="0f1ef-120">Um z. b. die Größe des Schlüssels zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="0f1ef-120">For example, to verify the size of the key:</span></span>


```C++
DWORD *pcbKey = (DWORD*)(pData + sizeof(BLOBHEADER));
if (*pcbKey != 16)
{
    // Wrong size! Should be 16 bytes (128 bits).
}
```



<span data-ttu-id="0f1ef-121">So erhalten Sie den Zeiger auf den Schlüssel selbst:</span><span class="sxs-lookup"><span data-stu-id="0f1ef-121">To get the pointer to the key itself:</span></span>


```C++
BYTE *pKey = pData + sizeof(BLOBHEADER) + sizeof(DWORD);
```



<span data-ttu-id="0f1ef-122">Generieren Sie als nächstes eine 32-Bit-Zufallszahl, die als Startsequenz für COPP-Status Anforderungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-122">Next, generate a 32-bit random number to use as the starting sequence for COPP status requests.</span></span> <span data-ttu-id="0f1ef-123">Die empfohlene Vorgehensweise zum Erstellen einer Zufallszahl ist das Aufrufen der Funktion **cryptgenrandom** .</span><span class="sxs-lookup"><span data-stu-id="0f1ef-123">The recommended way to create a random number is to call the **CryptGenRandom** function.</span></span> <span data-ttu-id="0f1ef-124">Verwenden Sie die **Rand** -Funktion nicht in der C-Lauf Zeit Bibliothek, da Sie nicht wirklich zufällig ist.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-124">Do not use the **rand** function in the C run-time library, because it is not truly random.</span></span> <span data-ttu-id="0f1ef-125">Generieren Sie eine zweite 32-Bit-Zufallszahl, die als Startsequenz für COPP-Befehle verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-125">Generate a second 32-bit random number to use as the starting sequence for COPP commands.</span></span>


```C++
UINT uStatusSeq;     // Status sequence number.
UINT uCommandSeq;    // Command sequence number.
CryptGenRandom(hCSP, sizeof(UINT), &uStatusSeq);
CryptGenRandom(hCSP, sizeof(UINT), &uCommandSeq);
```



<span data-ttu-id="0f1ef-126">Nun können Sie die COPP-Signatur vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-126">Now you can prepare the COPP signature.</span></span> <span data-ttu-id="0f1ef-127">Dies ist ein 256-Byte-Array, das als [**amcoppsignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) -Struktur definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-127">This is a 256-byte array, defined as the [**AMCOPPSignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) structure.</span></span> <span data-ttu-id="0f1ef-128">Initialisieren Sie den Inhalt des Arrays mit 0 (null).</span><span class="sxs-lookup"><span data-stu-id="0f1ef-128">Initialize the contents of the array to zero.</span></span> <span data-ttu-id="0f1ef-129">Kopieren Sie dann die vier Zahlen in das Array – die Zufallszahl des Treibers, den AES-Schlüssel, die Status Sequenznummer und die Befehlssequenz Nummer in dieser Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-129">Then copy the four numbers into the array—the driver's random number, the AES key, the status sequence number, and the command sequence number, in that order.</span></span> <span data-ttu-id="0f1ef-130">Tauschen Sie schließlich die Byte Reihenfolge des gesamten Arrays aus.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-130">Finally, swap the byte order of the entire array.</span></span>

<span data-ttu-id="0f1ef-131">Gemäß der Dokumentation für **CryptEncrypt**:</span><span class="sxs-lookup"><span data-stu-id="0f1ef-131">According to the documentation for **CryptEncrypt**:</span></span>

<dl> <span data-ttu-id="0f1ef-132">"Die Länge von Klartext-Daten, die mit einem" **CryptEncrypt** "-Rückruf mit einem RSA-Schlüssel verschlüsselt werden können, ist die Länge des Schlüsselmodulus minus elf bytes.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-132">"The length of plaintext data that can be encrypted with a call to **CryptEncrypt** with an RSA key is the length of the key modulus minus eleven bytes.</span></span> <span data-ttu-id="0f1ef-133">Die elf Bytes werden als Minimalwert für die Auffüll Dauer von PKCS \# 1 ausgewählt. "</span><span class="sxs-lookup"><span data-stu-id="0f1ef-133">The eleven bytes is the chosen minimum for PKCS \#1 padding."</span></span>  
</dl>

<span data-ttu-id="0f1ef-134">In diesem Fall ist der Modulo 256 Bytes, daher beträgt die maximale Nachrichten Länge 245 bytes (256 – 11).</span><span class="sxs-lookup"><span data-stu-id="0f1ef-134">In this case, the modulus is 256 bytes, so the maximum message length is 245 bytes (256 – 11).</span></span> <span data-ttu-id="0f1ef-135">Die **amcoppsignature** -Struktur ist 256 Byte, aber die aussagekräftigen Daten in der Signatur sind nur 40 Bytes.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-135">The **AMCOPPSignature** structure is 256 bytes, but the meaningful data in the signature is only 40 bytes.</span></span> <span data-ttu-id="0f1ef-136">Mit dem folgenden Code wird die Signatur verschlüsselt und das Ergebnis in bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-136">The following code encrypts the signature and provides the result in</span></span>


```
CoppSig
```



<span data-ttu-id="0f1ef-137">.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-137">.</span></span>


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



<span data-ttu-id="0f1ef-138">Übergeben Sie nun das verschlüsselte Array an [**iamcertifiedoutputprotection:: sessionsequencestart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):</span><span class="sxs-lookup"><span data-stu-id="0f1ef-138">Now pass the encrypted array to [**IAMCertifiedOutputProtection::SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):</span></span>


```C++
hr = pCOPP->SessionSequenceStart(&CoppSig);
if (SUCCEEDED(hr))
{
    // Ready to send COPP commands and status requests.
}
```



<span data-ttu-id="0f1ef-139">Wenn diese Methode erfolgreich ausgeführt wird, können Sie COPP-Befehle und-Status Anforderungen an den Treiber senden.</span><span class="sxs-lookup"><span data-stu-id="0f1ef-139">If this method succeeds, you are ready to send COPP commands and status requests to the driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f1ef-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0f1ef-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f1ef-141">Verwenden des Certified Output Protection-Protokolls (COPP)</span><span class="sxs-lookup"><span data-stu-id="0f1ef-141">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



