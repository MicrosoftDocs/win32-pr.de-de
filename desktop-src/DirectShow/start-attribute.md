---
description: Das Start-Attribut gibt die Startzeit eines Objekts relativ zum übergeordneten Objekt an.
ms.assetid: 971de88e-c1ee-4e07-bf8e-3153e4fd11f3
title: Start Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b377d0d83c86b981400a784904cf0423f0cca20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359451"
---
# <a name="start-attribute"></a><span data-ttu-id="faff1-103">Start Attribut</span><span class="sxs-lookup"><span data-stu-id="faff1-103">start Attribute</span></span>

> [!Note]  
> <span data-ttu-id="faff1-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="faff1-104">\[Deprecated.</span></span> <span data-ttu-id="faff1-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="faff1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="faff1-106">Das- `start` Attribut gibt die Startzeit eines Objekts relativ zum übergeordneten Objekt an.</span><span class="sxs-lookup"><span data-stu-id="faff1-106">The `start` attribute specifies the start time of an object, relative to the parent object.</span></span>

## <a name="possible-values"></a><span data-ttu-id="faff1-107">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="faff1-107">Possible Values</span></span>

<span data-ttu-id="faff1-108">Muss eine Zeichenfolge im Format " *hh: mm: SS. FF* " sein, wobei " *HH* = Hours, *mm* = Minutes, *SS* = seconds" und " *FF* = Sekundenbruchteile" sein muss.</span><span class="sxs-lookup"><span data-stu-id="faff1-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="faff1-109">Beispiel: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="faff1-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="faff1-110">Führende Einheiten können ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="faff1-110">Leading units can be omitted.</span></span> <span data-ttu-id="faff1-111">Beispielsweise sind 3:00 (drei Minuten) und 45 (45 Sekunden) beide gültig.</span><span class="sxs-lookup"><span data-stu-id="faff1-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="faff1-112">Gilt für</span><span class="sxs-lookup"><span data-stu-id="faff1-112">Applies To</span></span>

<span data-ttu-id="faff1-113">[**Clip**](clip-element.md), [**Effekt**](effect-element.md), [**Übergang**](transition-element.md)</span><span class="sxs-lookup"><span data-stu-id="faff1-113">[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="faff1-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="faff1-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faff1-115">XTL-Attribute</span><span class="sxs-lookup"><span data-stu-id="faff1-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="faff1-116">**Iamtimelineobj:: setstartstation**</span><span class="sxs-lookup"><span data-stu-id="faff1-116">**IAMTimelineObj::SetStartStop**</span></span>](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



