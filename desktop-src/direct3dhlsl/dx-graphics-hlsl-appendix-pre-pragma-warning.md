---
title: warning-pragma-Direktive
description: Pragma-Direktive, die das Verhalten von compilerwarnungs Meldungen ändert.
ms.assetid: 69488014-36e3-4c87-8b65-6123b5e87bcb
keywords:
- warning-pragma-Direktive HLSL
topic_type:
- apiref
api_name:
- warning pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7599886b47830b33c69f11c0c341c7775c644dd3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948198"
---
# <a name="warning-pragma-directive"></a><span data-ttu-id="7f868-104">warning-pragma-Direktive</span><span class="sxs-lookup"><span data-stu-id="7f868-104">warning pragma Directive</span></span>

<span data-ttu-id="7f868-105">Pragma-Direktive, die das Verhalten von compilerwarnungs Meldungen ändert.</span><span class="sxs-lookup"><span data-stu-id="7f868-105">Pragma directive that modifies the behavior of compiler warning messages.</span></span>



| <span data-ttu-id="7f868-106">\#pragma-Warnung ( *Warning-specifier* : *Warning-Number-List* \[ ; *Warning-specifier* : *Warning-Number-List*... \] )</span><span class="sxs-lookup"><span data-stu-id="7f868-106">\#pragma warning( *warning-specifier* : *warning-number-list* \[; *warning-specifier* : *warning-number-list*...\] )</span></span> |
|----------------------------------------------------------------------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="7f868-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f868-107">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f868-108">Element</span><span class="sxs-lookup"><span data-stu-id="7f868-108">Item</span></span></th>
<th><span data-ttu-id="7f868-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f868-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7f868-110"><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>warnungsspezifizierer</em></span><span class="sxs-lookup"><span data-stu-id="7f868-110"><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>warning-specifier</em></span></span><br/></td>
<td><span data-ttu-id="7f868-111">Das für die angegebenen Warnungen festzulegende Verhalten.</span><span class="sxs-lookup"><span data-stu-id="7f868-111">Behavior to set for the specified warnings.</span></span> <span data-ttu-id="7f868-112">Dieser Parameter kann einen der in der folgenden Tabelle aufgeführten Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="7f868-112">This parameter can take one of the values listed in the following table.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7f868-113">Wert</span><span class="sxs-lookup"><span data-stu-id="7f868-113">Value</span></span></th>
<th><span data-ttu-id="7f868-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f868-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7f868-115">once</span><span class="sxs-lookup"><span data-stu-id="7f868-115">once</span></span></td>
<td><span data-ttu-id="7f868-116">Zeigt die Meldung der Warnungen mit den angegebenen Zahlen nur einmal an.</span><span class="sxs-lookup"><span data-stu-id="7f868-116">Display the message of the warnings with the specified numbers only once.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f868-117">default</span><span class="sxs-lookup"><span data-stu-id="7f868-117">default</span></span></td>
<td><span data-ttu-id="7f868-118">Setzt das Verhalten der Warnungen mit den angegebenen Zahlen auf ihren Standardwert zurück.</span><span class="sxs-lookup"><span data-stu-id="7f868-118">Reset the behavior of the warnings with the specified numbers to their default value.</span></span> <span data-ttu-id="7f868-119">Dies hat auch den Effekt, dass eine Warnung aktiviert wird, die standardmäßig deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7f868-119">This also has the effect of turning a warning on that is off by default.</span></span> <span data-ttu-id="7f868-120">Die Warnung wird auf der Standard Ebene generiert.</span><span class="sxs-lookup"><span data-stu-id="7f868-120">The warning will be generated at its default level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7f868-121">1, 2, 3, 4</span><span class="sxs-lookup"><span data-stu-id="7f868-121">1, 2, 3, 4</span></span></td>
<td><span data-ttu-id="7f868-122">Wendet die angegebene Ebene auf die Warnungen mit den angegebenen Zahlen an.</span><span class="sxs-lookup"><span data-stu-id="7f868-122">Apply the specified level to the warnings with the specified numbers.</span></span> <span data-ttu-id="7f868-123">Dies hat auch den Effekt, dass eine Warnung aktiviert wird, die standardmäßig deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7f868-123">This also has the effect of turning a warning on that is off by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7f868-124">disable</span><span class="sxs-lookup"><span data-stu-id="7f868-124">disable</span></span></td>
<td><span data-ttu-id="7f868-125">Geben Sie die Warnungen nicht mit den angegebenen Zahlen aus.</span><span class="sxs-lookup"><span data-stu-id="7f868-125">Do not issue the warnings with the specified numbers.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7f868-126">error</span><span class="sxs-lookup"><span data-stu-id="7f868-126">error</span></span></td>
<td><span data-ttu-id="7f868-127">Melden Sie die Warnungen mit den angegebenen Zahlen als Fehler.</span><span class="sxs-lookup"><span data-stu-id="7f868-127">Report the warnings with the specified numbers as errors.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f868-128"><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>Warnung-Number-List</em></span><span class="sxs-lookup"><span data-stu-id="7f868-128"><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>warning-number-list</em></span></span></p></td>
<td><p><span data-ttu-id="7f868-129">Eine durch Leerzeichen getrennte Liste mit den Zahlen der Warnungen, um das Verhalten von zu ändern.</span><span class="sxs-lookup"><span data-stu-id="7f868-129">White space-delimited list of the numbers of the warnings to modify the behavior of.</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="7f868-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f868-130">Remarks</span></span>

<span data-ttu-id="7f868-131">Sie können eine beliebige Anzahl unterschiedlicher Änderungen an einem Warnungs Verhalten innerhalb desselben Warnungs-Pragmas angeben, indem Sie die Änderungen durch Semikolons trennen.</span><span class="sxs-lookup"><span data-stu-id="7f868-131">You can specify any number of distinct warning behavior changes within the same warning pragma by separating the changes with semicolons.</span></span>

<span data-ttu-id="7f868-132">Der Compiler fügt 4000 einer beliebigen Warnungs Zahl zwischen 0 und 999 hinzu.</span><span class="sxs-lookup"><span data-stu-id="7f868-132">The compiler will add 4000 to any warning number that is between 0 and 999.</span></span> <span data-ttu-id="7f868-133">Bei Warn Zahlen, die größer als 4699 sind (die der Codegenerierung zugeordneten), hat das warning-Pragma nur Auswirkungen, wenn Sie außerhalb von Funktionsdefinitionen platziert werden.</span><span class="sxs-lookup"><span data-stu-id="7f868-133">For warning numbers greater than 4699, (those associated with code generation) the warning pragma has effect only when placed outside function definitions.</span></span> <span data-ttu-id="7f868-134">Das Pragma wird ignoriert, wenn es eine Zahl größer als 4699 angibt und innerhalb einer Funktion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7f868-134">The pragma is ignored if it specifies a number greater than 4699 and is used inside a function.</span></span>

<span data-ttu-id="7f868-135">Das HLSL Warning-Pragma unterstützt die **Push** -und **Pop** -Funktionalität des Warning-Pragmas, das im C++-Compiler enthalten ist, nicht.</span><span class="sxs-lookup"><span data-stu-id="7f868-135">The HLSL warning pragma does not support the **push** and **pop** functionality of the warning pragma included in the C++ compiler.</span></span>

## <a name="examples"></a><span data-ttu-id="7f868-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f868-136">Examples</span></span>

<span data-ttu-id="7f868-137">Im folgenden Beispiel werden die Warnungen 4507 und 4034 deaktiviert, die Warnung 4385 einmal angezeigt und die Warnung 4164 als Fehlermeldung ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="7f868-137">The following example disables warnings 4507 and 4034, displays warning 4385 once once, and reports warning 4164 as an error.</span></span>


```
#pragma warning( disable : 4507 34; once : 4385; error : 164 )
```



<span data-ttu-id="7f868-138">Das vorherige Beispiel ist funktional äquivalent zu folgendem:</span><span class="sxs-lookup"><span data-stu-id="7f868-138">The preceding example is functionally equivalent to the following:</span></span>


```
#pragma warning( disable : 4507 34 )
#pragma warning( once : 4385 )
#pragma warning( error : 164 )
```



## <a name="see-also"></a><span data-ttu-id="7f868-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7f868-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f868-140">Präprozessordirektiven (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7f868-140">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="7f868-141">\#pragma-Direktive (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7f868-141">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





