---
description: Die Methode "Accept-Parser-allevelchange" akzeptiert oder lehnt die neue temporäre Jugend Verwaltungsebene ab.
ms.assetid: b3d58069-16dc-4598-90ea-6136c2f62ac7
title: Akzeptparser-allevelchange-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b2e81d1d82c4ede14580ed65d88566738dac1b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346829"
---
# <a name="acceptparentallevelchange-method"></a><span data-ttu-id="e7ccf-103">Akzeptparser-allevelchange-Methode</span><span class="sxs-lookup"><span data-stu-id="e7ccf-103">AcceptParentalLevelChange Method</span></span>

> [!Note]  
> <span data-ttu-id="e7ccf-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e7ccf-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e7ccf-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="e7ccf-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e7ccf-106">Die Methode "Accept-Parser-allevelchange" akzeptiert oder lehnt die neue temporäre Jugend Verwaltungsebene ab.</span><span class="sxs-lookup"><span data-stu-id="e7ccf-106">The AcceptParentalLevelChange method accepts or rejects the new temporary parental management level.</span></span>

``` syntax
        MSWebDVD.AcceptParentalLevelChange(bAccept)
```

## <a name="parameters"></a><span data-ttu-id="e7ccf-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7ccf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7ccf-108"><span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*baccept*</span><span class="sxs-lookup"><span data-stu-id="e7ccf-108"><span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*</span></span>
</dt> <dd>

<span data-ttu-id="e7ccf-109">Gibt die neue elternebene als booleschen Wert an.</span><span class="sxs-lookup"><span data-stu-id="e7ccf-109">Specifies the new parental level as a Boolean value.</span></span>



| <span data-ttu-id="e7ccf-110">Wert</span><span class="sxs-lookup"><span data-stu-id="e7ccf-110">Value</span></span> | <span data-ttu-id="e7ccf-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7ccf-111">Description</span></span>                               |
|-------|-------------------------------------------|
| <span data-ttu-id="e7ccf-112">true</span><span class="sxs-lookup"><span data-stu-id="e7ccf-112">true</span></span>  | <span data-ttu-id="e7ccf-113">Akzeptieren Sie die neue Jugend Verwaltungsebene.</span><span class="sxs-lookup"><span data-stu-id="e7ccf-113">Accept the new parental management level.</span></span> |
| <span data-ttu-id="e7ccf-114">false</span><span class="sxs-lookup"><span data-stu-id="e7ccf-114">false</span></span> | <span data-ttu-id="e7ccf-115">Lehnen Sie die neue Jugend Verwaltungsebene ab.</span><span class="sxs-lookup"><span data-stu-id="e7ccf-115">Reject the new parental management level.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7ccf-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7ccf-116">Return Value</span></span>

<span data-ttu-id="e7ccf-117">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="e7ccf-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7ccf-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7ccf-118">Remarks</span></span>

<span data-ttu-id="e7ccf-119">Geben Sie diese Methode als Reaktion auf eine Änderung des Änderungs Ereignisses für eine EC- \_ DVD an \_ \_ \_ , um anzugeben, ob der DVD-Navigator den Inhalt mit der neuen Jugendebene wiedergeben soll.</span><span class="sxs-lookup"><span data-stu-id="e7ccf-119">Call this method in response to an EC\_DVD\_PARENTAL\_LEVEL\_CHANGE event notification to specify whether the DVD Navigator should play the content with the new parental level, or branch to where the disc specifies if the new level is rejected.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7ccf-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7ccf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7ccf-121">Erzwingen von Eltern Verwaltungsebenen</span><span class="sxs-lookup"><span data-stu-id="e7ccf-121">Enforcing Parental Management Levels</span></span>](enforcing-parental-management-levels.md)
</dt> <dt>

[<span data-ttu-id="e7ccf-122">**Getplayerparameentalcountry**</span><span class="sxs-lookup"><span data-stu-id="e7ccf-122">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="e7ccf-123">**Getplayerparser**</span><span class="sxs-lookup"><span data-stu-id="e7ccf-123">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="e7ccf-124">**Gettitleparamevels**</span><span class="sxs-lookup"><span data-stu-id="e7ccf-124">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="e7ccf-125">**Notifyparametriallevelchange**</span><span class="sxs-lookup"><span data-stu-id="e7ccf-125">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="e7ccf-126">**Selectpartalcountry**</span><span class="sxs-lookup"><span data-stu-id="e7ccf-126">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="e7ccf-127">**Selectparser-allevel**</span><span class="sxs-lookup"><span data-stu-id="e7ccf-127">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> </dl>

 

 



