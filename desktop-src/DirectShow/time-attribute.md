---
description: Das Time-Attribut gibt die Zeit an, zu der ein Parameter einen neuen Wert annimmt, relativ zum Anfang des Übergangs oder Effekts.
ms.assetid: bb478215-cbd5-4fea-9d88-a1f2b002f3da
title: Zeit Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15a84d40c5e38ed81f8c17cd2d931e3f85e389a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218701"
---
# <a name="time-attribute"></a><span data-ttu-id="f7f39-103">Zeit Attribut</span><span class="sxs-lookup"><span data-stu-id="f7f39-103">time Attribute</span></span>

> [!Note]  
> <span data-ttu-id="f7f39-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="f7f39-104">\[Deprecated.</span></span> <span data-ttu-id="f7f39-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="f7f39-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f7f39-106">Das- `time` Attribut gibt die Zeit an, zu der ein Parameter einen neuen Wert annimmt, relativ zum Anfang des Übergangs oder Effekts.</span><span class="sxs-lookup"><span data-stu-id="f7f39-106">The `time` attribute specifies the time at which a parameter assumes a new value, relative to the start of the transition or effect.</span></span>

## <a name="possible-values"></a><span data-ttu-id="f7f39-107">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="f7f39-107">Possible Values</span></span>

<span data-ttu-id="f7f39-108">Muss eine Zeichenfolge im Format " *hh: mm: SS. FF* " sein, wobei " *HH* = Hours, *mm* = Minutes, *SS* = seconds" und " *FF* = Sekundenbruchteile" sein muss.</span><span class="sxs-lookup"><span data-stu-id="f7f39-108">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="f7f39-109">Beispiel: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="f7f39-109">Example: 1:04:30.512.</span></span> <span data-ttu-id="f7f39-110">Führende Einheiten können ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="f7f39-110">Leading units can be omitted.</span></span> <span data-ttu-id="f7f39-111">Beispielsweise sind 3:00 (drei Minuten) und 45 (45 Sekunden) beide gültig.</span><span class="sxs-lookup"><span data-stu-id="f7f39-111">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f7f39-112">Gilt für</span><span class="sxs-lookup"><span data-stu-id="f7f39-112">Applies To</span></span>

<span data-ttu-id="f7f39-113">[**bei**](at-element.md), [ **linear**](linear-element.md)</span><span class="sxs-lookup"><span data-stu-id="f7f39-113">[**at**](at-element.md), [**linear**](linear-element.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="f7f39-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7f39-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7f39-115">XTL-Attribute</span><span class="sxs-lookup"><span data-stu-id="f7f39-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> </dl>

 

 



