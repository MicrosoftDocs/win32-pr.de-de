---
description: Assert-und breakpointmakros
ms.assetid: c34db182-1f65-4a2f-9534-268638c2502d
title: Assert-und breakpointmakros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4771fb7e302ec9e1093fca82d7842212e0b68e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125348"
---
# <a name="assert-and-breakpoint-macros"></a><span data-ttu-id="64536-103">Assert-und breakpointmakros</span><span class="sxs-lookup"><span data-stu-id="64536-103">Assert and Breakpoint Macros</span></span>

<span data-ttu-id="64536-104">Die [DirectShow-Basisklassen](directshow-base-classes.md) stellen mehrere Makros bereit, die Assertionen ausführen oder Breakpoints verursachen.</span><span class="sxs-lookup"><span data-stu-id="64536-104">The [DirectShow Base Classes](directshow-base-classes.md) provide several macros that perform asserts or cause breakpoints.</span></span>



| <span data-ttu-id="64536-105">Makro</span><span class="sxs-lookup"><span data-stu-id="64536-105">Macro</span></span>                                        | <span data-ttu-id="64536-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64536-106">Description</span></span>                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64536-107">**Machung**</span><span class="sxs-lookup"><span data-stu-id="64536-107">**ASSERT**</span></span>](assert.md)                     | <span data-ttu-id="64536-108">Wertet einen Ausdruck aus und zeigt eine Diagnose Meldung an, wenn der Ausdruck **false** ist.</span><span class="sxs-lookup"><span data-stu-id="64536-108">Evaluates an expression, and displays a diagnostic message if the expression is **FALSE**.</span></span>                                         |
| [<span data-ttu-id="64536-109">**Dbgassertaligned**</span><span class="sxs-lookup"><span data-stu-id="64536-109">**DbgAssertAligned**</span></span>](dbgassertaligned.md) | <span data-ttu-id="64536-110">Testet, ob ein Zeiger an einer angegebenen Grenze ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="64536-110">Tests whether a pointer is aligned to a specified boundary.</span></span>                                                                        |
| [<span data-ttu-id="64536-111">**Dbgbreak**</span><span class="sxs-lookup"><span data-stu-id="64536-111">**DbgBreak**</span></span>](dbgbreak.md)                 | <span data-ttu-id="64536-112">Zeigt ein Meldungs Feld mit der angegebenen Zeichenfolge, dem Namen der Quelldatei und der Zeilennummer an.</span><span class="sxs-lookup"><span data-stu-id="64536-112">Displays a message box with the specified string, the name of the source file, and the line number.</span></span>                                |
| [<span data-ttu-id="64536-113">**\_Assert ausführen**</span><span class="sxs-lookup"><span data-stu-id="64536-113">**EXECUTE\_ASSERT**</span></span>](execute-assert.md)    | <span data-ttu-id="64536-114">Wertet einen Ausdruck in Debug-und Retail-Builds aus.</span><span class="sxs-lookup"><span data-stu-id="64536-114">Evaluates an expression in debug and retail builds.</span></span> <span data-ttu-id="64536-115">In Debugbuilds zeigt eine Diagnose Meldung an, wenn der Ausdruck **false** ist.</span><span class="sxs-lookup"><span data-stu-id="64536-115">In debug builds, displays a diagnostic message if the expression is **FALSE**.</span></span> |
| [<span data-ttu-id="64536-116">**Kassert**</span><span class="sxs-lookup"><span data-stu-id="64536-116">**KASSERT**</span></span>](kassert.md)                   | <span data-ttu-id="64536-117">Wertet einen Ausdruck aus und verursacht eine breakpointausnahme, wenn der Ausdruck **false** ist.</span><span class="sxs-lookup"><span data-stu-id="64536-117">Evaluates an expression, and causes a breakpoint exception if the expression is **FALSE**.</span></span>                                         |
| [<span data-ttu-id="64536-118">**Kdbgbreak**</span><span class="sxs-lookup"><span data-stu-id="64536-118">**KDbgBreak**</span></span>](kdbgbreak.md)               | <span data-ttu-id="64536-119">Verursacht eine breakpointausnahme und protokolliert die angegebene Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="64536-119">Causes a breakpoint exception, and logs the specified string.</span></span>                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="64536-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64536-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64536-121">Debugging-Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="64536-121">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



