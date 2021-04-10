---
description: Das cutpoint-Attribut gibt an, wann ein Übergang von einer Quelle zum nächsten erfolgt, wenn der Übergang als Ausschneiden gerendert wird. Der Wert ist relativ zum Anfang des Übergangs.
ms.assetid: bdb0b8cd-025f-4b56-9cd4-f71c58ee809a
title: cutpoint-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd516bd67577906a0a06d8da692ffbd7563ce32f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124597"
---
# <a name="cutpoint-attribute"></a><span data-ttu-id="ca59c-104">cutpoint-Attribut</span><span class="sxs-lookup"><span data-stu-id="ca59c-104">cutpoint Attribute</span></span>

> [!Note]  
> <span data-ttu-id="ca59c-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="ca59c-105">\[Deprecated.</span></span> <span data-ttu-id="ca59c-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="ca59c-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ca59c-107">Das- `cutpoint` Attribut gibt an, wann ein Übergang von einer Quelle zum nächsten erfolgt, wenn der Übergang als Ausschneiden gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="ca59c-107">The `cutpoint` attribute specifies when a transition cuts from one source to the next, if the transition is rendered as a cut.</span></span> <span data-ttu-id="ca59c-108">Der Wert ist relativ zum Anfang des Übergangs.</span><span class="sxs-lookup"><span data-stu-id="ca59c-108">The value is relative to the start of the transition.</span></span>

## <a name="possible-values"></a><span data-ttu-id="ca59c-109">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="ca59c-109">Possible Values</span></span>

<span data-ttu-id="ca59c-110">Muss eine Zeichenfolge im Format " *hh: mm: SS. FF* " sein, wobei " *HH* = Hours, *mm* = Minutes, *SS* = seconds" und " *FF* = Sekundenbruchteile" sein muss.</span><span class="sxs-lookup"><span data-stu-id="ca59c-110">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="ca59c-111">Beispiel: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="ca59c-111">Example: 1:04:30.512.</span></span> <span data-ttu-id="ca59c-112">Führende Einheiten können ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="ca59c-112">Leading units can be omitted.</span></span> <span data-ttu-id="ca59c-113">Beispielsweise sind 3:00 (drei Minuten) und 45 (45 Sekunden) beide gültig.</span><span class="sxs-lookup"><span data-stu-id="ca59c-113">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="ca59c-114">Gilt für</span><span class="sxs-lookup"><span data-stu-id="ca59c-114">Applies To</span></span>

[<span data-ttu-id="ca59c-115">**Übergang**</span><span class="sxs-lookup"><span data-stu-id="ca59c-115">**transition**</span></span>](transition-element.md)

## <a name="see-also"></a><span data-ttu-id="ca59c-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca59c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca59c-117">XTL-Attribute</span><span class="sxs-lookup"><span data-stu-id="ca59c-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="ca59c-118">**Iamtimelinetrans:: setcutpoint**</span><span class="sxs-lookup"><span data-stu-id="ca59c-118">**IAMTimelineTrans::SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)
</dt> </dl>

 

 



