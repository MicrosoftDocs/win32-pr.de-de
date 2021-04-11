---
description: Das mstoppt-Attribut gibt die Endzeit eines Clips relativ zur ursprünglichen Mediendatei an.
ms.assetid: 01559d29-9c7b-4842-a1f7-16552adbda43
title: mstoppt-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a63f52a1b912392165293e008074cf64a03b9751
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123469"
---
# <a name="mstop-attribute"></a><span data-ttu-id="6242c-103">mstoppt-Attribut</span><span class="sxs-lookup"><span data-stu-id="6242c-103">mstop Attribute</span></span>

> [!Note]  
> <span data-ttu-id="6242c-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="6242c-104">\[Deprecated.</span></span> <span data-ttu-id="6242c-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="6242c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6242c-106">Das- `mstop` Attribut gibt die Endzeit eines Clips relativ zur ursprünglichen Mediendatei an.</span><span class="sxs-lookup"><span data-stu-id="6242c-106">The `mstop` attribute specifies the stop time of a clip, relative to the original media file.</span></span>

## <a name="applies-to"></a><span data-ttu-id="6242c-107">Gilt für</span><span class="sxs-lookup"><span data-stu-id="6242c-107">Applies To</span></span>

[<span data-ttu-id="6242c-108">**Techno**</span><span class="sxs-lookup"><span data-stu-id="6242c-108">**clip**</span></span>](clip-element.md)

## <a name="possible-values"></a><span data-ttu-id="6242c-109">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="6242c-109">Possible Values</span></span>

<span data-ttu-id="6242c-110">Muss eine Zeichenfolge im Format " *hh: mm: SS. FF* " sein, wobei " *HH* = Hours, *mm* = Minutes, *SS* = seconds" und " *FF* = Sekundenbruchteile" sein muss.</span><span class="sxs-lookup"><span data-stu-id="6242c-110">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="6242c-111">Beispiel: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="6242c-111">Example: 1:04:30.512.</span></span> <span data-ttu-id="6242c-112">Führende Einheiten können ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="6242c-112">Leading units can be omitted.</span></span> <span data-ttu-id="6242c-113">Beispielsweise sind 3:00 (drei Minuten) und 45 (45 Sekunden) beide gültig.</span><span class="sxs-lookup"><span data-stu-id="6242c-113">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="see-also"></a><span data-ttu-id="6242c-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6242c-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6242c-115">XTL-Attribute</span><span class="sxs-lookup"><span data-stu-id="6242c-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="6242c-116">**Iamtimelinesrc:: setmediatimes**</span><span class="sxs-lookup"><span data-stu-id="6242c-116">**IAMTimelineSrc::SetMediaTimes**</span></span>](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



