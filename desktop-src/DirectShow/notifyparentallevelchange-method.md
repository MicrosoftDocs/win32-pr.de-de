---
description: Die notifyparser-allevelchange-Methode aktiviert oder deaktiviert die Ereignis Behandlung für Befehle der temporären Jugend Verwaltungsebene.
ms.assetid: c8252cc6-a83f-4cce-ba3e-7db669eeb465
title: Notifyparser-allevelchange-Methode (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc47b7d78af8cfdd32aa63361411e769c375ddf1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369699"
---
# <a name="notifyparentallevelchange-method"></a><span data-ttu-id="a6a68-103">Notifyparser-allevelchange-Methode</span><span class="sxs-lookup"><span data-stu-id="a6a68-103">NotifyParentalLevelChange Method</span></span>

> [!Note]  
> <span data-ttu-id="a6a68-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a6a68-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a6a68-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a6a68-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a6a68-106">Die- `NotifyParentalLevelChange` Methode aktiviert oder deaktiviert die Ereignis Behandlung für Befehle der temporären Jugend Verwaltungsebene.</span><span class="sxs-lookup"><span data-stu-id="a6a68-106">The `NotifyParentalLevelChange` method enables or disables the event handling for temporary parental management level commands.</span></span>

``` syntax
MSWebDVD.NotifyParentalLevelChange(bNotify)
```

## <a name="parameters"></a><span data-ttu-id="a6a68-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6a68-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6a68-108"><span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bbenachrichtigen*</span><span class="sxs-lookup"><span data-stu-id="a6a68-108"><span id="bNotify"></span><span id="bnotify"></span><span id="BNOTIFY"></span>*bNotify*</span></span>
</dt> <dd>

<span data-ttu-id="a6a68-109">Gibt einen booleschen Wert an, der angibt, ob die Anwendung benachrichtigt wird, wenn das mswebdvd-Objekt Videosegmente mit einer restriktiveren Bewertung als die Gesamtbewertung für die Festplatte findet.</span><span class="sxs-lookup"><span data-stu-id="a6a68-109">Specifies a Boolean value indicating whether or not the application is notified when the MSWebDVD object encounters video segments with a rating more restrictive than the overall rating for the disc.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6a68-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a6a68-110">Return Value</span></span>

<span data-ttu-id="a6a68-111">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="a6a68-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6a68-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a6a68-112">Remarks</span></span>

<span data-ttu-id="a6a68-113">Benachrichtigungs Verwaltungs Benachrichtigungen sind standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="a6a68-113">Parental management notifications are disabled by default.</span></span> <span data-ttu-id="a6a68-114">Dies bedeutet, dass temporäre Jugend Befehle von der Festplatte zulässig sind, aber ignoriert werden und die Festplatte ohne Unterbrechung wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a6a68-114">This means that temporary parental commands from the disc are allowed but ignored and disc will play without interruption.</span></span> <span data-ttu-id="a6a68-115">Diese Methode wird während der Initialisierung der Anwendung aufgerufen, wenn Sie die temporären Befehle der Jugend Verwaltungsebene von der Festplatte verarbeiten müssen. Um die Jugendverwaltung zu deaktivieren, nachdem Sie aktiviert wurde, müssen Sie diese Methode mit dem Argument false aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="a6a68-115">Call this method during initialization of your application if you need to handle temporary parental management level commands from the disc. To disable parental management after it is enabled, call this method with an argument of false.</span></span> <span data-ttu-id="a6a68-116">Weitere Informationen zur Eltern Verwaltung finden Sie unter " [**Accept-Parser-allevelchange**](acceptparentallevelchange-method.md)".</span><span class="sxs-lookup"><span data-stu-id="a6a68-116">For more details on parental management, see [**AcceptParentalLevelChange**](acceptparentallevelchange-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6a68-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a6a68-117">Requirements</span></span>



| <span data-ttu-id="a6a68-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a6a68-118">Requirement</span></span> | <span data-ttu-id="a6a68-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a6a68-119">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a6a68-120">Header</span><span class="sxs-lookup"><span data-stu-id="a6a68-120">Header</span></span><br/> | <dl> <span data-ttu-id="a6a68-121"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6a68-121"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6a68-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6a68-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6a68-123">**Selectparser-allevel**</span><span class="sxs-lookup"><span data-stu-id="a6a68-123">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="a6a68-124">**Gettitleparamevels**</span><span class="sxs-lookup"><span data-stu-id="a6a68-124">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="a6a68-125">**Getplayerparameentalcountry**</span><span class="sxs-lookup"><span data-stu-id="a6a68-125">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="a6a68-126">**Getplayerparser**</span><span class="sxs-lookup"><span data-stu-id="a6a68-126">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="a6a68-127">**Selectpartalcountry**</span><span class="sxs-lookup"><span data-stu-id="a6a68-127">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> </dl>

 

 




