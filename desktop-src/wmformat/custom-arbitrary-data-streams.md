---
title: Benutzerdefinierte beliebige Datenströme
description: Benutzerdefinierte beliebige Datenströme
ms.assetid: 23e93b5d-719f-47dc-9f3b-7bef14161b90
keywords:
- Windows Media-Format-SDK, benutzerdefinierte beliebige Datenströme
- Advanced Systems Format (ASF), benutzerdefinierte beliebige Datenströme
- ASF (Advanced Systems Format), benutzerdefinierte beliebige Datenströme
- Windows Media-Format-SDK, Streams
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- benutzerdefinierte beliebige Datenströme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c031e6d02864cae326a9cadb48577e1ea76c0e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341681"
---
# <a name="custom-arbitrary-data-streams"></a><span data-ttu-id="15b89-110">Benutzerdefinierte beliebige Datenströme</span><span class="sxs-lookup"><span data-stu-id="15b89-110">Custom Arbitrary Data Streams</span></span>

<span data-ttu-id="15b89-111">Sie können einen Stream in einer ASF-Datei erstellen, die beliebige Daten enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="15b89-111">You can create a stream in an ASF file to contain any sort of data.</span></span> <span data-ttu-id="15b89-112">Wenn keiner der unterstützten Streamtypen Ihren Anforderungen entspricht, müssen Sie einen beliebigen Datenstrom verwenden.</span><span class="sxs-lookup"><span data-stu-id="15b89-112">If none of the supported stream types suits your needs, you must use an arbitrary data stream.</span></span> <span data-ttu-id="15b89-113">Das Writer-Objekt verarbeitet einen beliebigen Datenstrom genauso wie alle nicht komprimierten Datenströme. die Beispiele werden packetisiert und mit den Beispielen aus anderen Streams im Daten Abschnitt der Datei kombiniert.</span><span class="sxs-lookup"><span data-stu-id="15b89-113">The writer object handles an arbitrary data stream just as it does any uncompressed stream; the samples are packetized and combined with the samples from other streams in the data section of the file.</span></span> <span data-ttu-id="15b89-114">Natürlich kann nur eine Leseanwendung, die speziell für den Umgang mit Ihrem beliebigen Typ programmiert wurde, die Daten verarbeiten, nachdem Sie vom Lese Objekt bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="15b89-114">Of course, only a reading application that has been specifically programmed to deal with your arbitrary type will be able to handle the data after it is delivered by the reading object.</span></span>

<span data-ttu-id="15b89-115">Eine häufige Verwendung beliebiger Datenströme ist für Mediendaten vorgesehen, die mit einem Drittanbieter-Codec codiert werden.</span><span class="sxs-lookup"><span data-stu-id="15b89-115">One common use of arbitrary data streams is for media data encoded by using a third-party codec.</span></span> <span data-ttu-id="15b89-116">Da die Objekte dieses SDK nicht direkt mit Codecs von Drittanbietern interagieren, muss die Schreib Anwendung die Beispiele mit dem Codierungs Teil des Codecs verarbeiten und die komprimierten Beispiele an den Writer übergeben.</span><span class="sxs-lookup"><span data-stu-id="15b89-116">Because the objects of this SDK do not interact directly with third-party codecs, your writing application must process the samples with the encoding portion of the codec and pass the compressed samples to the writer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15b89-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="15b89-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15b89-118">**Beliebige Streams**</span><span class="sxs-lookup"><span data-stu-id="15b89-118">**Arbitrary Streams**</span></span>](arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="15b89-119">**Konfigurieren von benutzerdefinierten beliebigen Streams**</span><span class="sxs-lookup"><span data-stu-id="15b89-119">**Configuring Custom Arbitrary Streams**</span></span>](configuring-custom-arbitrary-streams.md)
</dt> </dl>

 

 




