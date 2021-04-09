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
# <a name="obtaining-the-drivers-certificate-chain"></a><span data-ttu-id="d206d-103">Abrufen der Treiber Zertifikat Kette</span><span class="sxs-lookup"><span data-stu-id="d206d-103">Obtaining the Drivers Certificate Chain</span></span>

<span data-ttu-id="d206d-104">Zur Verwendung des Certified Output Protection Protocol (COPP) muss die Anwendung zuerst ein DirectShow-Diagramm erstellen, das den Video Mischungs Filter (VMR-7 oder VMR-9) enthält.</span><span class="sxs-lookup"><span data-stu-id="d206d-104">To use Certified Output Protection Protocol (COPP), the application first must build a DirectShow graph that includes the Video Mixing Render filter (VMR-7 or VMR-9).</span></span> <span data-ttu-id="d206d-105">Der ältere Videorendererfilter unterstützt COPP nicht.</span><span class="sxs-lookup"><span data-stu-id="d206d-105">The older Video Renderer filter does not support COPP.</span></span> <span data-ttu-id="d206d-106">Vor dem Aufrufen von COPP-Methoden muss die Anwendung ein Videowiedergabe Diagramm erstellen und den Decoder mit der Eingabe-PIN des VMR-Filters verbinden.</span><span class="sxs-lookup"><span data-stu-id="d206d-106">Before calling any COPP methods, the application must build a video playback graph and connect the decoder to the VMR filter's input pin.</span></span> <span data-ttu-id="d206d-107">Die Videodatei muss nicht abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="d206d-107">It is not necessary to play the video file.</span></span>

<span data-ttu-id="d206d-108">Fragen Sie nach der Erstellung des Diagramms den VMR nach der [**iamcertifiedoutputprotection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) -Schnittstelle ab, und nennen Sie dann [**iamcertifiedoutputprotection:: keyexchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span><span class="sxs-lookup"><span data-stu-id="d206d-108">After building the graph, query the VMR for the [**IAMCertifiedOutputProtection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) interface, and then call [**IAMCertifiedOutputProtection::KeyExchange**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-keyexchange).</span></span> <span data-ttu-id="d206d-109">Diese Methode gibt eine als GUID typisierte 128-Bit-Zufallszahl zusammen mit einem Zeiger auf ein Bytearray zurück, das die XML-Zertifikat Kette des Treibers im UTF-8-Format enthält.</span><span class="sxs-lookup"><span data-stu-id="d206d-109">This method returns a 128-bit random number typed as a GUID, along with a pointer to a byte array that contains the driver's XML certificate chain in UTF-8 format.</span></span> <span data-ttu-id="d206d-110">Der folgende Code zeigt, wie Sie die Zertifikat Kette erhalten.</span><span class="sxs-lookup"><span data-stu-id="d206d-110">The following code shows how to get the certificate chain.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d206d-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d206d-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d206d-112">Verwenden des Certified Output Protection-Protokolls (COPP)</span><span class="sxs-lookup"><span data-stu-id="d206d-112">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



