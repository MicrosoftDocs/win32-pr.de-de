---
description: Der Windows Media Audio Voice-Decoder decodiert Datenströme, die vom Windows Media Audio Voice-Encoder codiert wurden.
ms.assetid: 8bb5c8bd-949f-4faa-b679-8854f78076a4
title: Windows Media Audio sprach Decoder (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4565a511f2816d2914ec96f3ae89f3af5dd19016
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369647"
---
# <a name="windows-media-audio-voice-decoder"></a><span data-ttu-id="25f24-103">Windows Media Audio sprach Decoder</span><span class="sxs-lookup"><span data-stu-id="25f24-103">Windows Media Audio Voice Decoder</span></span>

<span data-ttu-id="25f24-104">Der Windows Media Audio Voice-Decoder decodiert Datenströme, die vom [**Windows Media Audio Voice-Encoder**](windowsmediaaudiovoiceencoder.md)codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="25f24-104">The Windows Media Audio Voice decoder decodes streams that were encoded by the [**Windows Media Audio Voice Encoder**](windowsmediaaudiovoiceencoder.md).</span></span>

## <a name="class-identifier"></a><span data-ttu-id="25f24-105">Klassen Bezeichner</span><span class="sxs-lookup"><span data-stu-id="25f24-105">Class Identifier</span></span>

<span data-ttu-id="25f24-106">Der Klassen Bezeichner (CLSID) für den Windows Media Audio sprach Decoder wird durch die Konstante **CLSID \_ cwmspdecmediaobject** dargestellt.</span><span class="sxs-lookup"><span data-stu-id="25f24-106">The class identifier (CLSID) for the Windows Media Audio Voice decoder is represented by the constant **CLSID\_CWMSPDecMediaObject**.</span></span> <span data-ttu-id="25f24-107">Sie können eine Instanz des sprach Decoders erstellen, indem Sie **CoCreateInstance** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="25f24-107">You can create an instance of the voice decoder by calling **CoCreateInstance**.</span></span>

## <a name="input-formats"></a><span data-ttu-id="25f24-108">Eingabeformate</span><span class="sxs-lookup"><span data-stu-id="25f24-108">Input Formats</span></span>

<span data-ttu-id="25f24-109">Windows Media Audio sprach codierter Inhalt wird durch das Format-Tag 0x00a identifiziert.</span><span class="sxs-lookup"><span data-stu-id="25f24-109">Windows Media Audio Voice encoded content is identified by the format tag 0x00A.</span></span>

## <a name="requirements"></a><span data-ttu-id="25f24-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25f24-110">Requirements</span></span>



| <span data-ttu-id="25f24-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25f24-111">Requirement</span></span> | <span data-ttu-id="25f24-112">Wert</span><span class="sxs-lookup"><span data-stu-id="25f24-112">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25f24-113">Client</span><span class="sxs-lookup"><span data-stu-id="25f24-113">Client</span></span><br/> | <span data-ttu-id="25f24-114">Windows XP, Windows Vista oder Windows 7</span><span class="sxs-lookup"><span data-stu-id="25f24-114">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="25f24-115">Header</span><span class="sxs-lookup"><span data-stu-id="25f24-115">Header</span></span><br/> | <dl> <span data-ttu-id="25f24-116"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="25f24-116"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="25f24-117">DLL</span><span class="sxs-lookup"><span data-stu-id="25f24-117">DLL</span></span><br/>    | <dl> <span data-ttu-id="25f24-118"><dt>Wmspdmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25f24-118"><dt>Wmspdmod.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25f24-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25f24-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25f24-120">Codec-Objekte</span><span class="sxs-lookup"><span data-stu-id="25f24-120">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="25f24-121">Verwenden des Windows Media Audio Voice-Codecs</span><span class="sxs-lookup"><span data-stu-id="25f24-121">Using the Windows Media Audio Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[<span data-ttu-id="25f24-122">Windows Media Audio sprach Encoder</span><span class="sxs-lookup"><span data-stu-id="25f24-122">Windows Media Audio Voice Encoder</span></span>](windowsmediaaudiovoiceencoder.md)
</dt> </dl>

 

 




