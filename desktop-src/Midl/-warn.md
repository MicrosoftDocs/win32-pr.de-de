---
title: /Warn-Schalter
description: Der/Warn-Schalter gibt die Warnstufe des Mittell-Compilers an.
ms.assetid: b1e26e67-8c47-40a2-8f34-22273ddfaa1d
keywords:
- /Warn-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /warn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb2effd65175bf7bf54cb74cb63a56af0278784
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718198"
---
# <a name="warn-switch"></a><span data-ttu-id="0019f-104">/Warn-Schalter</span><span class="sxs-lookup"><span data-stu-id="0019f-104">/warn switch</span></span>

<span data-ttu-id="0019f-105">Der **/Warn** -Schalter gibt die Warnstufe des Mittell-Compilers an.</span><span class="sxs-lookup"><span data-stu-id="0019f-105">The **/warn** switch specifies the warning level of the MIDL compiler.</span></span>

``` syntax
midl /warn level
```

## <a name="switch-options"></a><span data-ttu-id="0019f-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="0019f-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="0019f-107">*level*</span><span class="sxs-lookup"><span data-stu-id="0019f-107">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="0019f-108">Gibt die Warnstufe an, eine ganze Zahl im Bereich von 0 bis 4.</span><span class="sxs-lookup"><span data-stu-id="0019f-108">Specifies the warning level, an integer in the range 0 through 4.</span></span> <span data-ttu-id="0019f-109">Zwischen dem Schalter **/Warn** und der Ziffer, die den Wert für die Warnstufe angibt, besteht kein Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="0019f-109">There is no space between the **/warn** switch and the digit indicating the warning-level value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0019f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0019f-110">Remarks</span></span>

<span data-ttu-id="0019f-111">Die Warnstufe zeigt den Schweregrad der Warnung an.</span><span class="sxs-lookup"><span data-stu-id="0019f-111">The warning level indicates the severity of the warning.</span></span> <span data-ttu-id="0019f-112">Die Warnungs Stufen liegen zwischen 1 und 4. der Wert 0 bedeutet, dass keine Warn Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0019f-112">Warning levels range from 1 to 4, with a value of zero meaning to display no warning information.</span></span> <span data-ttu-id="0019f-113">Die Warnung mit dem höchsten Schweregrad ist Ebene 1.</span><span class="sxs-lookup"><span data-stu-id="0019f-113">The highest severity warning is level 1.</span></span> <span data-ttu-id="0019f-114">In der folgenden Tabelle werden die Warnungen für die einzelnen Warn Stufen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0019f-114">The following table describes the warnings for each warning level.</span></span>



| <span data-ttu-id="0019f-115">Warnstufe</span><span class="sxs-lookup"><span data-stu-id="0019f-115">Warning level</span></span> | <span data-ttu-id="0019f-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0019f-116">Description</span></span>                                             | <span data-ttu-id="0019f-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0019f-117">Example</span></span>                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="0019f-118">0</span><span class="sxs-lookup"><span data-stu-id="0019f-118">0</span></span>             | <span data-ttu-id="0019f-119">Keine Warnungen.</span><span class="sxs-lookup"><span data-stu-id="0019f-119">No warnings.</span></span>                                            |                                                                           |
| <span data-ttu-id="0019f-120">1</span><span class="sxs-lookup"><span data-stu-id="0019f-120">1</span></span>             | <span data-ttu-id="0019f-121">Schwerwiegende Warnungen, die zu Anwendungsfehlern führen können.</span><span class="sxs-lookup"><span data-stu-id="0019f-121">Severe warnings that can cause application errors.</span></span>      | <span data-ttu-id="0019f-122">Es wurde kein Bindungs handle angegeben, nicht attributierte Zeiger, widersprüchliche Switches.</span><span class="sxs-lookup"><span data-stu-id="0019f-122">No binding handle specified, unattributed pointers, conflicting switches.</span></span> |
| <span data-ttu-id="0019f-123">2</span><span class="sxs-lookup"><span data-stu-id="0019f-123">2</span></span>             | <span data-ttu-id="0019f-124">Kann zu Problemen in der Betriebsumgebung des Benutzers führen.</span><span class="sxs-lookup"><span data-stu-id="0019f-124">May cause problems in the user's operating environment.</span></span> | <span data-ttu-id="0019f-125">Die Bezeichnerlänge überschreitet 31 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="0019f-125">Identifier length exceeds 31 characters.</span></span> <span data-ttu-id="0019f-126">Es wurde kein Standard-Union-Arm angegeben.</span><span class="sxs-lookup"><span data-stu-id="0019f-126">No default union arm specified.</span></span>  |
| <span data-ttu-id="0019f-127">3</span><span class="sxs-lookup"><span data-stu-id="0019f-127">3</span></span>             | <span data-ttu-id="0019f-128">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="0019f-128">Reserved.</span></span>                                               |                                                                           |
| <span data-ttu-id="0019f-129">4</span><span class="sxs-lookup"><span data-stu-id="0019f-129">4</span></span>             | <span data-ttu-id="0019f-130">Niedrigste Warnstufe.</span><span class="sxs-lookup"><span data-stu-id="0019f-130">Lowest warning level.</span></span>                                   | <span data-ttu-id="0019f-131">Nicht-ANSI-C-Konstrukte.</span><span class="sxs-lookup"><span data-stu-id="0019f-131">Non-ANSI C constructs.</span></span>                                                    |



 

<span data-ttu-id="0019f-132">Warnungen unterscheiden sich von Fehlern.</span><span class="sxs-lookup"><span data-stu-id="0019f-132">Warnings are different from errors.</span></span> <span data-ttu-id="0019f-133">Fehler bewirken, dass der Mittell-Compiler die Verarbeitung der IDL-Datei stoppt.</span><span class="sxs-lookup"><span data-stu-id="0019f-133">Errors cause the MIDL compiler to halt processing of the IDL file.</span></span> <span data-ttu-id="0019f-134">Warnungen bewirken, dass der Mittell-Compiler eine Informations Meldung ausgibt und die Verarbeitung der IDL-Datei fortsetzt.</span><span class="sxs-lookup"><span data-stu-id="0019f-134">Warnings cause the MIDL compiler to emit an informational message and continue processing the IDL file.</span></span>

<span data-ttu-id="0019f-135">Die Warnstufe, die durch den Schalter " **/Warn** " festgelegt wird, kann mit dem [**WX**](-wx.md) -Schalter verwendet werden, damit der Mittell-Compiler die Verarbeitung der IDL-Datei stoppt.</span><span class="sxs-lookup"><span data-stu-id="0019f-135">The warning level set by the **/warn** switch can be used with the [**WX**](-wx.md) switch to cause the MIDL compiler to halt processing of the IDL file.</span></span>

<span data-ttu-id="0019f-136">Der **/Warn** -Schalter verhält sich wie der [**/W**](-w.md) -Schalter.</span><span class="sxs-lookup"><span data-stu-id="0019f-136">The **/warn** switch behaves the same as the [**/W**](-w.md) switch.</span></span>

## <a name="examples"></a><span data-ttu-id="0019f-137">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0019f-137">Examples</span></span>

<span data-ttu-id="0019f-138">**Mittel l/warn2 Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="0019f-138">**midl /warn2 filename.idl**</span></span>

<span data-ttu-id="0019f-139">**Mittel l/warn4 Leiste. idl**</span><span class="sxs-lookup"><span data-stu-id="0019f-139">**midl /warn4 bar.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="0019f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0019f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0019f-141">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="0019f-141">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




