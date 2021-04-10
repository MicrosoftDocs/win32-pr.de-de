---
title: Frame Interpolation
description: Frame Interpolation
ms.assetid: 74dbe855-361c-42ba-b21b-322ccd1c91d0
keywords:
- Windows Media-Format-SDK, Frame Interpolation
- Codecs, Frame Interpolation
- Frame Interpolation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c62f95322920576eec0f10f3e4d61a279fdc4cf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038558"
---
# <a name="frame-interpolation"></a><span data-ttu-id="bbe22-106">Frame Interpolation</span><span class="sxs-lookup"><span data-stu-id="bbe22-106">Frame Interpolation</span></span>

<span data-ttu-id="bbe22-107">Die Frame Interpolation ist der Prozess der Erstellung von zwischen Video Frames auf der Grundlage der Daten in zwei aufeinander folgenden Frames codierter Videos.</span><span class="sxs-lookup"><span data-stu-id="bbe22-107">Frame interpolation is the process of creating intermediate video frames based on the data in two consecutive frames of encoded video.</span></span> <span data-ttu-id="bbe22-108">In der Tat erhöht die Frame Interpolation die [*Framerate*](wmformat-glossary.md) codierter Videos zum Zeitpunkt der Decodierung.</span><span class="sxs-lookup"><span data-stu-id="bbe22-108">In effect, frame interpolation increases the [*frame rate*](wmformat-glossary.md) of encoded video at the time of decoding.</span></span> <span data-ttu-id="bbe22-109">Mithilfe von Frame Interpolation können Sie die Glättung von Wiedergabe Möglichkeiten für Videostreams mit niedrigen Frameraten verbessern.</span><span class="sxs-lookup"><span data-stu-id="bbe22-109">You can use frame interpolation to improve the smoothness of playback for video streams with low frame rates.</span></span>

<span data-ttu-id="bbe22-110">Da es sich hierbei um eine Decodierungs Funktion handelt, sind keine speziellen Codierungsoptionen enthalten, und der Inhalt wird dadurch nicht erhöht.</span><span class="sxs-lookup"><span data-stu-id="bbe22-110">Because this is a decoding feature, it does not involve any special encoding options and adds no overhead to the content.</span></span> <span data-ttu-id="bbe22-111">Die Frame Interpolation wird als Ausgabe Einstellung im Reader-Objekt angegeben.</span><span class="sxs-lookup"><span data-stu-id="bbe22-111">Frame interpolation is specified as an output setting in the reader object.</span></span>

<span data-ttu-id="bbe22-112">Nur der Windows Media Video 9-Codec unterstützt die Frame Interpolation.</span><span class="sxs-lookup"><span data-stu-id="bbe22-112">Only the Windows Media Video 9 codec supports frame interpolation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbe22-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bbe22-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbe22-114">**Codec-Features**</span><span class="sxs-lookup"><span data-stu-id="bbe22-114">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="bbe22-115">**IWMReaderAdvanced2:: setoutputsetting**</span><span class="sxs-lookup"><span data-stu-id="bbe22-115">**IWMReaderAdvanced2::SetOutputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[<span data-ttu-id="bbe22-116">**Ausgabeeinstellungen**</span><span class="sxs-lookup"><span data-stu-id="bbe22-116">**Output Settings**</span></span>](output-settings.md)
</dt> </dl>

 

 




