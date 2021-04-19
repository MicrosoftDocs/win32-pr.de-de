---
description: Konfigurieren der Video Decodierung
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: Konfigurieren der Video Decodierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386e3dbb39d6296756f2fe8eec1b94c5533bff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343210"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a><span data-ttu-id="d2ea7-103">Konfigurieren der Video Decodierung (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-103">Configuring Video Decoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="d2ea7-104">Die Decodierung ist im Grunde das Gegenteil der Codierung in Bezug auf die Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-104">Decoding is essentially the opposite of encoding in terms of configuration.</span></span> <span data-ttu-id="d2ea7-105">Der Decoder unterstützt nur sehr wenige Eigenschaften, und keine davon ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-105">The decoder supports very few properties, and none of them is required.</span></span> <span data-ttu-id="d2ea7-106">Legen Sie den Eingabetyp auf den Typ fest, der für die decoderausgabe verwendet wird (einschließlich der privaten Codec-Daten)</span><span class="sxs-lookup"><span data-stu-id="d2ea7-106">Set the input type to the type used for the decoder output (including the codec private data).</span></span> <span data-ttu-id="d2ea7-107">Legen Sie dann die Ausgabe auf das gewünschte nicht komprimierte Format fest, legen Sie die [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur auf die richtige Frame Größe fest, und beginnen Sie mit der Verarbeitung von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-107">Then set the output to the desired uncompressed format, set the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure to reflect the proper frame size, and start processing samples.</span></span>

<span data-ttu-id="d2ea7-108">Sie müssen den Decoder mit einem Medientyp bereitstellen, der die privaten Codec-Daten enthält, die unmittelbar nach der [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -Struktur positioniert sind.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-108">You must supply the decoder with a media type that includes the codec private data positioned immediately after the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span> <span data-ttu-id="d2ea7-109">Der Decoder kann den Inhalt ohne diese Daten nicht decodieren.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-109">The decoder cannot decode the content without this data.</span></span> <span data-ttu-id="d2ea7-110">Die vom Decoder ausgeführte Format Validierung überprüft nicht die privaten Daten.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-110">The format validation performed by the decoder does not validate the private data.</span></span> <span data-ttu-id="d2ea7-111">Wenn die privaten Codec-Daten fehlen oder falsch sind, antwortet der Decoder so, als ob der Bitstream beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="d2ea7-111">If the codec private data is missing or incorrect, the decoder responds as if the bit stream is corrupted.</span></span> <span data-ttu-id="d2ea7-112">Weitere Informationen finden Sie unter [Verwenden von privaten Videocodec-Daten](usingvideocodecprivatedata.md).</span><span class="sxs-lookup"><span data-stu-id="d2ea7-112">For more information, see [Using Video Codec Private Data](usingvideocodecprivatedata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2ea7-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d2ea7-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2ea7-114">Verwenden von privaten Videocodec-Daten</span><span class="sxs-lookup"><span data-stu-id="d2ea7-114">Using Video Codec Private Data</span></span>](usingvideocodecprivatedata.md)
</dt> <dt>

[<span data-ttu-id="d2ea7-115">Arbeiten mit Videos</span><span class="sxs-lookup"><span data-stu-id="d2ea7-115">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 
