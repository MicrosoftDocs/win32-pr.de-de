---
description: Abrufen der Treiberzertifikatkette
ms.assetid: bc7b346c-3382-4f2b-90b6-03f6a1a5a9ce
title: Abrufen der Treiberzertifikatkette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2641c27c3d24ab45a87b16e8c805228c316d9f89428cd29abbaff347b5aae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684560"
---
# <a name="obtaining-the-drivers-certificate-chain"></a>Abrufen der Treiberzertifikatkette

Zur Verwendung des Certified Output Protection Protocol (COPP) muss die Anwendung zunächst ein DirectShow-Diagramm erstellen, das den Filter "Rendern von Videos mischen" (VMR-7 oder VMR-9) enthält. Der ältere Videorendererfilter unterstützt COPP nicht. Vor dem Aufrufen von COPP-Methoden muss die Anwendung ein Videowiedergabediagramm erstellen und den Decoder mit dem Eingabepin des VMR-Filters verbinden. Die Videodatei muss nicht wieder verwendet werden.

Fragen Sie nach dem Erstellen des Graphen die VMR nach der [**IAMCertifiedOutputProtection-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) ab, und rufen Sie [**dann IAMCertifiedOutputProtection::KeyExchange auf.**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange) Diese Methode gibt eine als GUID typisierte 128-Bit-Zufallszahl sowie einen Zeiger auf ein Bytearray zurück, das die XML-Zertifikatkette des Treibers im UTF-8-Format enthält. Der folgende Code zeigt, wie die Zertifikatkette erhalten wird.


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

 

 



