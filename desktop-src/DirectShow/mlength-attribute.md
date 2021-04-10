---
description: Das mlength-Attribut gibt die Dauer einer Quelldatei an. Dieser Wert muss die tatsächliche Dauer sein, oder es können Renderingfehler auftreten.
ms.assetid: f33ce85c-df61-4248-8dea-677162fa1a07
title: mlength-Attribut
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eadc288e29d99df0e6af7f06e1404d86f6a938
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957696"
---
# <a name="mlength-attribute"></a><span data-ttu-id="a7e18-104">mlength-Attribut</span><span class="sxs-lookup"><span data-stu-id="a7e18-104">mlength Attribute</span></span>

> [!Note]  
> <span data-ttu-id="a7e18-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="a7e18-105">\[Deprecated.</span></span> <span data-ttu-id="a7e18-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="a7e18-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a7e18-107">Das- `mlength` Attribut gibt die Dauer einer Quelldatei an.</span><span class="sxs-lookup"><span data-stu-id="a7e18-107">The `mlength` attribute specifies the duration of a source file.</span></span> <span data-ttu-id="a7e18-108">Dieser Wert muss die tatsächliche Dauer sein, oder es können Renderingfehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="a7e18-108">This value must be the actual duration, or rendering errors may occur.</span></span>

## <a name="applies-to"></a><span data-ttu-id="a7e18-109">Gilt für</span><span class="sxs-lookup"><span data-stu-id="a7e18-109">Applies To</span></span>

[<span data-ttu-id="a7e18-110">**Techno**</span><span class="sxs-lookup"><span data-stu-id="a7e18-110">**clip**</span></span>](clip-element.md)

## <a name="possible-values"></a><span data-ttu-id="a7e18-111">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="a7e18-111">Possible Values</span></span>

<span data-ttu-id="a7e18-112">Muss eine Zeichenfolge im Format " *hh: mm: SS. FF* " sein, wobei " *HH* = Hours, *mm* = Minutes, *SS* = seconds" und " *FF* = Sekundenbruchteile" sein muss.</span><span class="sxs-lookup"><span data-stu-id="a7e18-112">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="a7e18-113">Beispiel: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="a7e18-113">Example: 1:04:30.512.</span></span> <span data-ttu-id="a7e18-114">Führende Einheiten können ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="a7e18-114">Leading units can be omitted.</span></span> <span data-ttu-id="a7e18-115">Beispielsweise sind 3:00 (drei Minuten) und 45 (45 Sekunden) beide gültig.</span><span class="sxs-lookup"><span data-stu-id="a7e18-115">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7e18-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7e18-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7e18-117">XTL-Attribute</span><span class="sxs-lookup"><span data-stu-id="a7e18-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="a7e18-118">**Iamtimelinesrc:: setmedialength**</span><span class="sxs-lookup"><span data-stu-id="a7e18-118">**IAMTimelineSrc::SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)
</dt> </dl>

 

 



