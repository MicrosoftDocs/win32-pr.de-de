---
description: Die gettitleparser-Methode ruft die Jugend Verwaltungsebenen für den angegebenen Titel ab.
ms.assetid: 076808d7-6cb6-4d81-b26d-c7945db298f2
title: Gettitleparser-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6db82ca21c2fdd023aa472e4c3428260464a8612
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392622"
---
# <a name="gettitleparentallevels-method"></a><span data-ttu-id="38deb-103">Gettitleparser-Methode</span><span class="sxs-lookup"><span data-stu-id="38deb-103">GetTitleParentalLevels Method</span></span>

> [!Note]  
> <span data-ttu-id="38deb-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="38deb-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="38deb-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="38deb-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="38deb-106">Die- `GetTitleParentalLevels` Methode ruft die Jugend Verwaltungsebenen für den angegebenen Titel ab.</span><span class="sxs-lookup"><span data-stu-id="38deb-106">The `GetTitleParentalLevels` method retrieves the parental management levels for the specified title.</span></span>

``` syntax
[ iLevels = ] MSWebDVD.GetTitleParentalLevels(iTitle)
```

## <a name="parameters"></a><span data-ttu-id="38deb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="38deb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38deb-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*ititle*</span><span class="sxs-lookup"><span data-stu-id="38deb-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="38deb-109">Gibt den Titel als Ganzzahl an.</span><span class="sxs-lookup"><span data-stu-id="38deb-109">Specifies the title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38deb-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38deb-110">Return Value</span></span>

<span data-ttu-id="38deb-111">Gibt einen ganzzahligen Wert zurück, dessen einzelne Bits angeben, welche Personen Verwaltungsebenen (PML) im angegebenen Titel festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="38deb-111">Returns an integer value whose individual bits indicate which parental management levels (PML) are set in the specified title.</span></span>

## <a name="remarks"></a><span data-ttu-id="38deb-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38deb-112">Remarks</span></span>

<span data-ttu-id="38deb-113">Ein Titel kann über Kapitel oder sogar kurze Segmente verfügen, deren PML von der Gesamt-PML für den Titel abweicht.</span><span class="sxs-lookup"><span data-stu-id="38deb-113">A title may have chapters or even short segments that have a PML different from the overall PML for the title.</span></span> <span data-ttu-id="38deb-114">Verwenden Sie diese Methode, um alle PMLs zu ermitteln, die bei der Wiedergabe eines bestimmten Titels gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="38deb-114">Use this method to determine all the PMLs that will be encountered when playing a specified title.</span></span> <span data-ttu-id="38deb-115">Die zurückgegebene Ganzzahl ist ein Satz von Bitflags, die wie in der folgenden Tabelle dargestellt definiert werden.</span><span class="sxs-lookup"><span data-stu-id="38deb-115">The returned integer is a set of bit flags that are defined as shown in the table below.</span></span> <span data-ttu-id="38deb-116">Führt eine bitweise AND-Operation auf *ilevels* und jedem möglichen Wert aus.</span><span class="sxs-lookup"><span data-stu-id="38deb-116">Perform a bitwise AND operation on *iLevels* and each possible value.</span></span> <span data-ttu-id="38deb-117">Wenn der Vorgang **true** zurückgibt, bedeutet dies, dass an einem bestimmten Punkt in diesem Titel PML angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="38deb-117">If the operation returns **true**, it means that PML will be encountered at some point in this title.</span></span>



| <span data-ttu-id="38deb-118">Wert</span><span class="sxs-lookup"><span data-stu-id="38deb-118">Value</span></span>  | <span data-ttu-id="38deb-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38deb-119">Description</span></span>          |
|--------|----------------------|
| <span data-ttu-id="38deb-120">0x100</span><span class="sxs-lookup"><span data-stu-id="38deb-120">0x100</span></span>  | <span data-ttu-id="38deb-121">DVD-Jugend Stufe 1</span><span class="sxs-lookup"><span data-stu-id="38deb-121">DVD Parental Level 1</span></span> |
| <span data-ttu-id="38deb-122">0x200</span><span class="sxs-lookup"><span data-stu-id="38deb-122">0x200</span></span>  | <span data-ttu-id="38deb-123">DVD-Jugend Stufe 2</span><span class="sxs-lookup"><span data-stu-id="38deb-123">DVD Parental Level 2</span></span> |
| <span data-ttu-id="38deb-124">0x400</span><span class="sxs-lookup"><span data-stu-id="38deb-124">0x400</span></span>  | <span data-ttu-id="38deb-125">DVD-elternebene 3</span><span class="sxs-lookup"><span data-stu-id="38deb-125">DVD Parental Level 3</span></span> |
| <span data-ttu-id="38deb-126">0x800</span><span class="sxs-lookup"><span data-stu-id="38deb-126">0x800</span></span>  | <span data-ttu-id="38deb-127">DVD-elternebene 4</span><span class="sxs-lookup"><span data-stu-id="38deb-127">DVD Parental Level 4</span></span> |
| <span data-ttu-id="38deb-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="38deb-128">0x1000</span></span> | <span data-ttu-id="38deb-129">DVD-Jugend Stufe 5</span><span class="sxs-lookup"><span data-stu-id="38deb-129">DVD Parental Level 5</span></span> |
| <span data-ttu-id="38deb-130">0x2000</span><span class="sxs-lookup"><span data-stu-id="38deb-130">0x2000</span></span> | <span data-ttu-id="38deb-131">DVD-elternebene 6</span><span class="sxs-lookup"><span data-stu-id="38deb-131">DVD Parental Level 6</span></span> |
| <span data-ttu-id="38deb-132">0x4000</span><span class="sxs-lookup"><span data-stu-id="38deb-132">0x4000</span></span> | <span data-ttu-id="38deb-133">DVD-Jugend Stufe 7</span><span class="sxs-lookup"><span data-stu-id="38deb-133">DVD Parental Level 7</span></span> |
| <span data-ttu-id="38deb-134">0x8000</span><span class="sxs-lookup"><span data-stu-id="38deb-134">0x8000</span></span> | <span data-ttu-id="38deb-135">DVD-elternebene 8</span><span class="sxs-lookup"><span data-stu-id="38deb-135">DVD Parental Level 8</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="38deb-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38deb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38deb-137">**Selectparser-allevel**</span><span class="sxs-lookup"><span data-stu-id="38deb-137">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="38deb-138">**Getplayerparameentalcountry**</span><span class="sxs-lookup"><span data-stu-id="38deb-138">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="38deb-139">**Getplayerparser**</span><span class="sxs-lookup"><span data-stu-id="38deb-139">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="38deb-140">**Selectpartalcountry**</span><span class="sxs-lookup"><span data-stu-id="38deb-140">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> </dl>

 

 



