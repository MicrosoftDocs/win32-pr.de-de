---
description: Abrufen der Treiber Zertifikat Kette
ms.assetid: bc7b346c-3382-4f2b-90b6-03f6a1a5a9ce
title: Abrufen der Treiber Zertifikat Kette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3f46e395550ca4bcb02396fe09126c1232f2c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859981"
---
# <a name="obtaining-the-drivers-certificate-chain"></a>Abrufen der Treiber Zertifikat Kette

Zur Verwendung des Certified Output Protection Protocol (COPP) muss die Anwendung zuerst ein DirectShow-Diagramm erstellen, das den Video Mischungs Filter (VMR-7 oder VMR-9) enthält. Der ältere Videorendererfilter unterstützt COPP nicht. Vor dem Aufrufen von COPP-Methoden muss die Anwendung ein Videowiedergabe Diagramm erstellen und den Decoder mit der Eingabe-PIN des VMR-Filters verbinden. Die Videodatei muss nicht abgespielt werden.

Fragen Sie nach der Erstellung des Diagramms den VMR nach der [**iamcertifiedoutputprotection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) -Schnittstelle ab, und nennen Sie dann [**iamcertifiedoutputprotection:: keyexchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange). Diese Methode gibt eine als GUID typisierte 128-Bit-Zufallszahl zusammen mit einem Zeiger auf ein Bytearray zurück, das die XML-Zertifikat Kette des Treibers im UTF-8-Format enthält. Der folgende Code zeigt, wie Sie die Zertifikat Kette erhalten.


```C++
GUID guidRandom;
BYTE *pbCertificateChain = NULL;
DWORD cbCertificateChainLen;   // Size of the certificate chain, in bytes.
hr = pCOPP->KeyExchange(&guidRandom, &pbCertificateChain,
         &cbCertificateChainLen);
if (SUCCEEDED(hr))
{
    // TODO: Validate the certificate chain and get the driver's
    // public key. 

    // When you are done, free the buffer that contains the 
    // certificate chain.
    CoTaskMemFree(pbCertificateChain);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Certified Output Protection-Protokolls (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



