---
description: Warum lehnt der Video Encoder ein Ausgabeformat ab, das ich festgelegt habe, wenn ich das Format aus demselben Objekt abgerufen habe?
ms.assetid: f0747450-d224-423a-a9f1-04580df8a17e
title: Warum lehnt der Video Encoder ein Ausgabeformat ab, das ich festgelegt habe, wenn ich das Format aus demselben Objekt abgerufen habe?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680908ec814fe322585c1ac97d3bb79deddaf034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042037"
---
# <a name="why-does-the-video-encoder-reject-an-output-format-that-i-try-to-set-when-i-retrieved-the-format-from-the-same-object"></a><span data-ttu-id="22190-103">Warum lehnt der Video Encoder ein Ausgabeformat ab, das ich festgelegt habe, wenn ich das Format aus demselben Objekt abgerufen habe?</span><span class="sxs-lookup"><span data-stu-id="22190-103">Why does the video encoder reject an output format that I try to set, when I retrieved the format from the same object?</span></span>

<span data-ttu-id="22190-104">Im Unterschied zu audioencoderausgabetypen werden die von den Video Encodern aufgelisteten unterstützten Ausgaben nicht als zugestellt vervollständigt.</span><span class="sxs-lookup"><span data-stu-id="22190-104">Unlike audio encoder output types, the supported outputs enumerated by the video encoders are not complete as delivered.</span></span> <span data-ttu-id="22190-105">Sie müssen die Bitrate des Streams im **dwbitrate** -Member der **videoinfoheader** -Struktur auf den Wert festlegen, der für die Eigenschaft " [mfpkey \_ Ravg](mfpkey-ravgproperty.md) " festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="22190-105">You must set the bit rate of the stream in the **dwBitrate** member of the **VIDEOINFOHEADER** structure to match the value set for the [MFPKEY\_RAVG](mfpkey-ravgproperty.md) property.</span></span>

<span data-ttu-id="22190-106">Nachdem alle Optionen auf die gewünschte Weise festgelegt wurden, müssen Sie die privaten Codec-Daten abrufen und Sie an die **videoinfoheader** -Struktur anfügen.</span><span class="sxs-lookup"><span data-stu-id="22190-106">After all of the options are set the way that you want them, you must retrieve the codec private data and append it to the **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="22190-107">Weitere Informationen finden Sie unter [Verwenden von privaten Videocodec-Daten](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="22190-107">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="22190-108">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22190-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22190-109">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="22190-109">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



