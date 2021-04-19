---
title: /W-Schalter
description: Der/W-Schalter gibt die Warnstufe des Mittell-Compilers an. Die Warnstufe zeigt den Schweregrad der Warnung an.
ms.assetid: ee894d73-cbd1-455f-9836-a6d80cfc95f9
keywords:
- /W-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /W
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b1f15ae0c28722adaca8c4b0651606681ce3af
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338420"
---
# <a name="w-switch"></a><span data-ttu-id="86e07-105">/W-Schalter</span><span class="sxs-lookup"><span data-stu-id="86e07-105">/W switch</span></span>

<span data-ttu-id="86e07-106">Der **/W** -Schalter gibt die Warnstufe des Mittell-Compilers an.</span><span class="sxs-lookup"><span data-stu-id="86e07-106">The **/W** switch specifies the warning level of the MIDL compiler.</span></span> <span data-ttu-id="86e07-107">Die Warnstufe zeigt den Schweregrad der Warnung an.</span><span class="sxs-lookup"><span data-stu-id="86e07-107">The warning level indicates the severity of the warning.</span></span>

``` syntax
midl /W level
```

## <a name="switch-options"></a><span data-ttu-id="86e07-108">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="86e07-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="86e07-109">*level*</span><span class="sxs-lookup"><span data-stu-id="86e07-109">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="86e07-110">Gibt die Warnstufe an, eine ganze Zahl im Bereich von 0 bis 4.</span><span class="sxs-lookup"><span data-stu-id="86e07-110">Specifies the warning level, an integer in the range 0 through 4.</span></span> <span data-ttu-id="86e07-111">Zwischen dem Schalter **/W** und der Ziffer, die den Wert für die Warnstufe angibt, besteht kein Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="86e07-111">There is no space between the **/W** switch and the digit indicating the warning-level value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="86e07-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86e07-112">Remarks</span></span>

<span data-ttu-id="86e07-113">Die Warnungs Stufen liegen zwischen 1 und 4. der Wert 0 bedeutet, dass keine Warn Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="86e07-113">Warning levels range from 1 to 4, with a value of zero meaning to display no warning information.</span></span> <span data-ttu-id="86e07-114">Die Warnung mit dem höchsten Schweregrad ist Ebene 1.</span><span class="sxs-lookup"><span data-stu-id="86e07-114">The highest-severity warning is level 1.</span></span> <span data-ttu-id="86e07-115">In der folgenden Tabelle werden die Warnungen für die einzelnen Warn Stufen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="86e07-115">The following table describes the warnings for each warning level.</span></span>



| <span data-ttu-id="86e07-116">Warnstufe</span><span class="sxs-lookup"><span data-stu-id="86e07-116">Warning level</span></span> | <span data-ttu-id="86e07-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86e07-117">Description</span></span>                                             | <span data-ttu-id="86e07-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="86e07-118">Example</span></span>                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="86e07-119">W0</span><span class="sxs-lookup"><span data-stu-id="86e07-119">W0</span></span>            | <span data-ttu-id="86e07-120">Keine Warnungen.</span><span class="sxs-lookup"><span data-stu-id="86e07-120">No warnings.</span></span>                                            |                                                                           |
| <span data-ttu-id="86e07-121">W1</span><span class="sxs-lookup"><span data-stu-id="86e07-121">W1</span></span>            | <span data-ttu-id="86e07-122">Schwerwiegende Warnungen, die zu Anwendungsfehlern führen können.</span><span class="sxs-lookup"><span data-stu-id="86e07-122">Severe warnings that can cause application errors.</span></span>      | <span data-ttu-id="86e07-123">Es wurde kein Bindungs handle angegeben, nicht attributierte Zeiger, widersprüchliche Switches.</span><span class="sxs-lookup"><span data-stu-id="86e07-123">No binding handle specified, unattributed pointers, conflicting switches.</span></span> |
| <span data-ttu-id="86e07-124">W2</span><span class="sxs-lookup"><span data-stu-id="86e07-124">W2</span></span>            | <span data-ttu-id="86e07-125">Kann zu Problemen in der Betriebsumgebung des Benutzers führen.</span><span class="sxs-lookup"><span data-stu-id="86e07-125">May cause problems in the user's operating environment.</span></span> | <span data-ttu-id="86e07-126">Die Bezeichnerlänge überschreitet 31 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="86e07-126">Identifier length exceeds 31 characters.</span></span> <span data-ttu-id="86e07-127">Es wurde kein Standard-Union-Arm angegeben.</span><span class="sxs-lookup"><span data-stu-id="86e07-127">No default union arm specified.</span></span>  |
| <span data-ttu-id="86e07-128">W3</span><span class="sxs-lookup"><span data-stu-id="86e07-128">W3</span></span>            | <span data-ttu-id="86e07-129">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="86e07-129">Reserved.</span></span>                                               |                                                                           |
| <span data-ttu-id="86e07-130">W4</span><span class="sxs-lookup"><span data-stu-id="86e07-130">W4</span></span>            | <span data-ttu-id="86e07-131">Niedrigste Warnstufe.</span><span class="sxs-lookup"><span data-stu-id="86e07-131">Lowest warning level.</span></span>                                   | <span data-ttu-id="86e07-132">Nicht-ANSI-C-Konstrukte.</span><span class="sxs-lookup"><span data-stu-id="86e07-132">Non-ANSI C constructs.</span></span>                                                    |



 

<span data-ttu-id="86e07-133">Warnungen unterscheiden sich von Fehlern.</span><span class="sxs-lookup"><span data-stu-id="86e07-133">Warnings are different from errors.</span></span> <span data-ttu-id="86e07-134">Fehler bewirken, dass der Mittell-Compiler die Verarbeitung der IDL-Datei stoppt.</span><span class="sxs-lookup"><span data-stu-id="86e07-134">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="86e07-135">Warnungen bewirken, dass der Mittell-Compiler eine Informations Meldung ausgibt und die Verarbeitung der IDL-Datei fortsetzt.</span><span class="sxs-lookup"><span data-stu-id="86e07-135">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="86e07-136">Die vom **/W** -Schalter festgelegte Warnstufe kann mit dem [**/WX**](-wx.md) -Schalter verwendet werden, damit der Mittell-Compiler die Verarbeitung der IDL-Datei stoppt.</span><span class="sxs-lookup"><span data-stu-id="86e07-136">The warning level set by the **/W** switch can be used with the [**/WX**](-wx.md) switch to cause the MIDL compiler to halt processing of the IDL file.</span></span>

<span data-ttu-id="86e07-137">Der **/W** -Schalter verhält sich wie der [**/Warn**](-warn.md) -Schalter.</span><span class="sxs-lookup"><span data-stu-id="86e07-137">The **/W** switch behaves the same as the [**/warn**](-warn.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="86e07-138">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86e07-138">Examples</span></span>

<span data-ttu-id="86e07-139">**Mittel l/W2 Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="86e07-139">**midl /W2 filename.idl**</span></span>

<span data-ttu-id="86e07-140">**Mittel l/W4 Leiste. idl**</span><span class="sxs-lookup"><span data-stu-id="86e07-140">**midl /W4 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="86e07-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86e07-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86e07-142">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="86e07-142">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="86e07-143">**/Warn**</span><span class="sxs-lookup"><span data-stu-id="86e07-143">**/warn**</span></span>](-warn.md)
</dt> </dl>

 

 




