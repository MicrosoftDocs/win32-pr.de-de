---
description: Das mstart-Attribut gibt die Startzeit eines Clips relativ zur ursprünglichen Mediendatei an.
ms.assetid: ed63f448-8ca3-4733-afc0-2d743f82bebe
title: mstart-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb637dd0c5f924a593370ceb0fb205adf5d589ea
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480758"
---
# <a name="mstart-attribute"></a><span data-ttu-id="ee61e-103">mstart-Attribut</span><span class="sxs-lookup"><span data-stu-id="ee61e-103">mstart Attribute</span></span>

> [!Note]  
> <span data-ttu-id="ee61e-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ee61e-104">\[Deprecated.</span></span> <span data-ttu-id="ee61e-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="ee61e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ee61e-106">Das- `mstart` Attribut gibt die Startzeit eines Clips relativ zur ursprünglichen Mediendatei an.</span><span class="sxs-lookup"><span data-stu-id="ee61e-106">The `mstart` attribute specifies the start time of a clip, relative to the original media file.</span></span>

## <a name="applies-to"></a><span data-ttu-id="ee61e-107">Gilt für</span><span class="sxs-lookup"><span data-stu-id="ee61e-107">Applies To</span></span>

[<span data-ttu-id="ee61e-108">**Techno**</span><span class="sxs-lookup"><span data-stu-id="ee61e-108">**clip**</span></span>](clip-element.md)

## <a name="possible-values"></a><span data-ttu-id="ee61e-109">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="ee61e-109">Possible Values</span></span>

<span data-ttu-id="ee61e-110">Muss eine Zeichenfolge im Format " *hh: mm: SS. FF* " sein, wobei " *HH* = Hours, *mm* = Minutes, *SS* = seconds" und " *FF* = Sekundenbruchteile" sein muss.</span><span class="sxs-lookup"><span data-stu-id="ee61e-110">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="ee61e-111">Beispiel: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="ee61e-111">Example: 1:04:30.512.</span></span> <span data-ttu-id="ee61e-112">Führende Einheiten können ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="ee61e-112">Leading units can be omitted.</span></span> <span data-ttu-id="ee61e-113">Beispielsweise sind 3:00 (drei Minuten) und 45 (45 Sekunden) beide gültig.</span><span class="sxs-lookup"><span data-stu-id="ee61e-113">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee61e-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee61e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee61e-115">XTL-Attribute</span><span class="sxs-lookup"><span data-stu-id="ee61e-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="ee61e-116">**Iamtimelinesrc:: setmediatimes**</span><span class="sxs-lookup"><span data-stu-id="ee61e-116">**IAMTimelineSrc::SetMediaTimes**</span></span>](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



