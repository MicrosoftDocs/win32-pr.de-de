---
description: Das Attribut "beenden" gibt die Endzeit eines Objekts relativ zum übergeordneten Objekt an.
ms.assetid: 1bda3472-abda-4672-9b82-311163e56fe0
title: Attribut "Ende"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6deb3f2a422cb8100da32c0427caf6436e72fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359449"
---
# <a name="stop-attribute"></a><span data-ttu-id="caced-103">Attribut "Ende"</span><span class="sxs-lookup"><span data-stu-id="caced-103">stop Attribute</span></span>

> [!Note]  
> <span data-ttu-id="caced-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="caced-104">\[Deprecated.</span></span> <span data-ttu-id="caced-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="caced-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="caced-106">Das- `stop` Attribut gibt die Endzeit eines Objekts relativ zum übergeordneten Objekt an.</span><span class="sxs-lookup"><span data-stu-id="caced-106">The `stop` attribute specifies the stop time of an object, relative to the parent object.</span></span>

## <a name="possible-values"></a><span data-ttu-id="caced-107">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="caced-107">Possible Values</span></span>

<span data-ttu-id="caced-108">Muss eine Zeichenfolge im Format " *hh: mm: SS. FF* " sein, wobei " *HH* = Hours, *mm* = Minutes, *SS* = seconds" und " *FF* = Sekundenbruchteile" sein muss.</span><span class="sxs-lookup"><span data-stu-id="caced-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="caced-109">Beispiel: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="caced-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="caced-110">Führende Einheiten können ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="caced-110">Leading units can be omitted.</span></span> <span data-ttu-id="caced-111">Beispielsweise sind 3:00 (drei Minuten) und 45 (45 Sekunden) beide gültig.</span><span class="sxs-lookup"><span data-stu-id="caced-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="caced-112">Gilt für</span><span class="sxs-lookup"><span data-stu-id="caced-112">Applies To</span></span>

<span data-ttu-id="caced-113">[**Clip**](clip-element.md), [**Effekt**](effect-element.md), [**Übergang**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="caced-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="caced-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="caced-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="caced-115">XTL-Attribute</span><span class="sxs-lookup"><span data-stu-id="caced-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="caced-116">**Iamtimelineobj:: setstartstation**</span><span class="sxs-lookup"><span data-stu-id="caced-116">**IAMTimelineObj::SetStartStop**</span></span>](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



