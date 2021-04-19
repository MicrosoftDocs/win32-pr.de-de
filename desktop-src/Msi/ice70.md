---
description: ICE70 überprüft, ob ganzzahlige Werte für Registrierungseinträge ordnungsgemäß angegeben werden.
ms.assetid: f8493622-867b-42e1-9fda-a7c3229bbb4e
title: ICE70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616592a772dec6f95d81b92f03f0bffea6ce7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353623"
---
# <a name="ice70"></a><span data-ttu-id="cb015-103">ICE70</span><span class="sxs-lookup"><span data-stu-id="cb015-103">ICE70</span></span>

<span data-ttu-id="cb015-104">ICE70 überprüft, ob ganzzahlige Werte für Registrierungseinträge ordnungsgemäß angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cb015-104">ICE70 verifies that integer values for registry entries are specified correctly.</span></span> <span data-ttu-id="cb015-105">Werte der Form \# \# Str, \# % unexpanded Str, werden nicht überprüft.</span><span class="sxs-lookup"><span data-stu-id="cb015-105">Values of the form \#\#str, \#%unexpanded str are not validated.</span></span> <span data-ttu-id="cb015-106">Werte der Form \# xhex, \# xhex, \# Integer und \# \[ Property \] werden überprüft.</span><span class="sxs-lookup"><span data-stu-id="cb015-106">Values of the form \#xhex, \#Xhex, \#integer, and \#\[property\] are validated.</span></span> <span data-ttu-id="cb015-107">In der folgenden Tabelle finden Sie eine kurze Übersicht.</span><span class="sxs-lookup"><span data-stu-id="cb015-107">The following table provides a brief overview.</span></span>



| <span data-ttu-id="cb015-108">Wert</span><span class="sxs-lookup"><span data-stu-id="cb015-108">Value</span></span>                 | <span data-ttu-id="cb015-109">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="cb015-109">Validation</span></span>                                                                    |
|-----------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="cb015-110">\#\#SRT</span><span class="sxs-lookup"><span data-stu-id="cb015-110">\#\#str</span></span>               | <span data-ttu-id="cb015-111">gültigen</span><span class="sxs-lookup"><span data-stu-id="cb015-111">valid</span></span>                                                                         |
| <span data-ttu-id="cb015-112">\#% nicht erweitert Str</span><span class="sxs-lookup"><span data-stu-id="cb015-112">\#%unexpanded str</span></span>     | <span data-ttu-id="cb015-113">gültigen</span><span class="sxs-lookup"><span data-stu-id="cb015-113">valid</span></span>                                                                         |
| <span data-ttu-id="cb015-114">\#xhex, \# xhex</span><span class="sxs-lookup"><span data-stu-id="cb015-114">\#xHex,\#XHex</span></span>         | <span data-ttu-id="cb015-115">Überprüfen Sie auf gültige hexadezimale Zeichen (0-9, a-f, a-f).</span><span class="sxs-lookup"><span data-stu-id="cb015-115">Validate for valid hex characters (0-9,a-f,A-F).</span></span> <span data-ttu-id="cb015-116">Eigenschaften sind hier zulässig.</span><span class="sxs-lookup"><span data-stu-id="cb015-116">Properties are allowed here.</span></span> |
| <span data-ttu-id="cb015-117">\#+ int, \# -int, \# int</span><span class="sxs-lookup"><span data-stu-id="cb015-117">\#+int, \#-int, \#int</span></span> | <span data-ttu-id="cb015-118">Validieren Sie auf gültige numerische Zeichen (0-9).</span><span class="sxs-lookup"><span data-stu-id="cb015-118">Validate for valid numeric characters (0-9).</span></span> <span data-ttu-id="cb015-119">Eigenschaften sind hier zulässig.</span><span class="sxs-lookup"><span data-stu-id="cb015-119">Properties are allowed here.</span></span>     |



 

<span data-ttu-id="cb015-120">Die Syntax für einen ganzzahligen Wert, der in die Registrierung eingegeben werden soll, ist \# Integer, wobei Integer numerisch ist.</span><span class="sxs-lookup"><span data-stu-id="cb015-120">The syntax for an integer value to be entered into the registry is \#integer where integer is numerical.</span></span>

## <a name="result"></a><span data-ttu-id="cb015-121">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="cb015-121">Result</span></span>

<span data-ttu-id="cb015-122">ICE70 meldet einen Fehler, wenn ganzzahlige Werte für Registrierungseinträge nicht ordnungsgemäß angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="cb015-122">ICE70 reports an error if integer values for registry entries are not specified correctly.</span></span>

## <a name="example"></a><span data-ttu-id="cb015-123">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cb015-123">Example</span></span>

<span data-ttu-id="cb015-124">ICE70 meldet die folgenden Fehler für das angegebene Beispiel.</span><span class="sxs-lookup"><span data-stu-id="cb015-124">ICE70 reports the following errors for the given example.</span></span>

``` syntax
The value #12xz34 is an invalid numeric value for registry entry Reg1. If you meant to use a string, then the string value entry must be preceded by ## not #.
```

<span data-ttu-id="cb015-125">So beheben Sie diesen Fehler: Wenn der Wert numerisch sein soll, ändern Sie den Wert so, dass alle numerischen Zeichen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb015-125">To fix this error: If you want the value to be numeric, change the value to use all numeric characters.</span></span> <span data-ttu-id="cb015-126">Wenn Sie möchten, dass der Wert eine Zeichenfolge ist, muss der Wert zwei ' \# ' ( \# \# ) anstelle von nur einem vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="cb015-126">If you want the value to be a string, it must be preceded by two '\#' (\#\#) instead of just one.</span></span>

``` syntax
The value #xz34 is an invalid hexadecimal value for registry entry Reg2.
```

<span data-ttu-id="cb015-127">So beheben Sie diesen Fehler: gültige hexadezimale Zeichen sind 0-9, a-f und a-f.</span><span class="sxs-lookup"><span data-stu-id="cb015-127">To fix this error: Valid hexadecimal characters are 0-9, A-F, and a-f.</span></span> <span data-ttu-id="cb015-128">Nur diese Zeichen können auf das \# x (oder \# x) folgen.</span><span class="sxs-lookup"><span data-stu-id="cb015-128">Only these characters can follow the \#x (or \#X).</span></span>

<span data-ttu-id="cb015-129">[Registrierungs Tabelle](registry-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="cb015-129">[Registry table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="cb015-130">Registrierung</span><span class="sxs-lookup"><span data-stu-id="cb015-130">Registry</span></span> | <span data-ttu-id="cb015-131">Wert</span><span class="sxs-lookup"><span data-stu-id="cb015-131">Value</span></span>    |
|----------|----------|
| <span data-ttu-id="cb015-132">Reg1</span><span class="sxs-lookup"><span data-stu-id="cb015-132">Reg1</span></span>     | <span data-ttu-id="cb015-133">\#12xz34</span><span class="sxs-lookup"><span data-stu-id="cb015-133">\#12xz34</span></span> |
| <span data-ttu-id="cb015-134">Reg2</span><span class="sxs-lookup"><span data-stu-id="cb015-134">Reg2</span></span>     | <span data-ttu-id="cb015-135">\#xz34</span><span class="sxs-lookup"><span data-stu-id="cb015-135">\#xz34</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="cb015-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb015-136">Remarks</span></span>

-   <span data-ttu-id="cb015-137">\#\[MyProperty \] ist gültig.</span><span class="sxs-lookup"><span data-stu-id="cb015-137">\#\[myproperty\] is valid.</span></span>
-   <span data-ttu-id="cb015-138">\#\[MyProperty ist ungültig (fehlende schließende Klammer).</span><span class="sxs-lookup"><span data-stu-id="cb015-138">\#\[myproperty is not valid (missing ending bracket).</span></span>
-   <span data-ttu-id="cb015-139">\#\[myProp1 \] \[ myProp2 ist gültig.</span><span class="sxs-lookup"><span data-stu-id="cb015-139">\#\[myprop1\] \[myprop2 is valid.</span></span> <span data-ttu-id="cb015-140">(Obwohl der letzte Klammer die schließende Klammer fehlt, kann myProp1 zu Str ausgewertet werden \# \# \# , sodass Str \[ myProp2 gültig ist.</span><span class="sxs-lookup"><span data-stu-id="cb015-140">(Even though the last one is missing the ending bracket, myprop1 could evaluate to \#str so you would have \#\#str \[myprop2, which is valid</span></span>
-   <span data-ttu-id="cb015-141">\#\]MyProperty \[ ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="cb015-141">\#\]myproperty\[ is not valid</span></span>
-   <span data-ttu-id="cb015-142">Alle eingebetteten Eigenschaften in einer Wert Zeichenfolge dürfen nicht in \[ $compkey- \] , \[ \# filekey- \] oder \[ ! filekey-Form vorliegen, \] da diese nicht numerisch sind.</span><span class="sxs-lookup"><span data-stu-id="cb015-142">Any embedded property in a value string cannot be in \[$compkey\], \[\#filekey\], or \[!filekey\] form because these are not numeric.</span></span> <span data-ttu-id="cb015-143">Es gibt jedoch eine Ausnahme: \# \[ MyProperty \] \[ $compkey \] (oder \[ \# filekey \] oder \[ ! filekey) ist gültig, da " \] MyProperty" wie bei der vorhergehenden \[ in "str" ausgewertet werden \] kann \# .</span><span class="sxs-lookup"><span data-stu-id="cb015-143">However, there is one exception, \#\[myproperty\] \[$compkey\] (or \[\#filekey\] or \[!filekey\]) is valid because, as with the preceding, \[myproperty\] can evaluate to \#str.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb015-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cb015-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb015-145">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="cb015-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



