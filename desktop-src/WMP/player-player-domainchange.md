---
title: Player. domainchange-Ereignis
description: Das domainchange-Ereignis tritt auf, wenn die DVD-Domäne geändert wird. | Player. domainchange-Ereignis
ms.assetid: 01965492-276e-4d30-99eb-767e0776b423
keywords:
- Windows-Media Player für Domänen Änderungs Ereignisse
- Domainchange-Ereignis, Windows Media Player, Player-Klasse
- Player-Klasse Windows Media Player, domainchange-Ereignis
topic_type:
- apiref
api_name:
- Player.DomainChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9637913451aa5bba937906130899c46e0bd34d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365487"
---
# <a name="playerdomainchange-event"></a><span data-ttu-id="5f421-107">Player. domainchange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="5f421-107">Player.DomainChange event</span></span>

<span data-ttu-id="5f421-108">Das **domainchange** -Ereignis tritt auf, wenn die DVD-Domäne geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5f421-108">The **DomainChange** event occurs when the DVD domain changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f421-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f421-109">Syntax</span></span>


```JScript
Player.DomainChange(
  strDomain
)
```



## <a name="parameters"></a><span data-ttu-id="5f421-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f421-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f421-111">*Domäne*</span><span class="sxs-lookup"><span data-stu-id="5f421-111">*strDomain*</span></span> 
</dt> <dd>

<span data-ttu-id="5f421-112">**Zeichenfolge** , die die neue Domäne angibt.</span><span class="sxs-lookup"><span data-stu-id="5f421-112">**String** indicating the new domain.</span></span> <span data-ttu-id="5f421-113">Enthält einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="5f421-113">Contains one of the following values.</span></span>



| <span data-ttu-id="5f421-114">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5f421-114">String</span></span>            | <span data-ttu-id="5f421-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f421-115">Description</span></span>                                                          |
|-------------------|----------------------------------------------------------------------|
| <span data-ttu-id="5f421-116">FirstPlay</span><span class="sxs-lookup"><span data-stu-id="5f421-116">firstplay</span></span>         | <span data-ttu-id="5f421-117">Die Standard Initialisierung einer DVD-CD wird durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f421-117">Performing default initialization of a DVD disc.</span></span>                     |
| <span data-ttu-id="5f421-118">videomanagermenu</span><span class="sxs-lookup"><span data-stu-id="5f421-118">videoManagerMenu</span></span>  | <span data-ttu-id="5f421-119">Anzeigen von Menüs für die gesamte Festplatte. Wird auch als "Root Menu" oder "topmenu" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5f421-119">Displaying menus for whole disc. Also known as Root Menu or topMenu.</span></span> |
| <span data-ttu-id="5f421-120">videotitlesetmenu</span><span class="sxs-lookup"><span data-stu-id="5f421-120">videoTitleSetMenu</span></span> | <span data-ttu-id="5f421-121">Anzeigen von Menüs für den aktuellen Titel Satz.</span><span class="sxs-lookup"><span data-stu-id="5f421-121">Displaying menus for current title set.</span></span> <span data-ttu-id="5f421-122">Wird auch als titlemenu bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5f421-122">Also known as titleMenu.</span></span>     |
| <span data-ttu-id="5f421-123">title</span><span class="sxs-lookup"><span data-stu-id="5f421-123">title</span></span>             | <span data-ttu-id="5f421-124">Anzeigen des aktuellen Titels.</span><span class="sxs-lookup"><span data-stu-id="5f421-124">Displaying the current title.</span></span>                                        |
| <span data-ttu-id="5f421-125">stop</span><span class="sxs-lookup"><span data-stu-id="5f421-125">stop</span></span>              | <span data-ttu-id="5f421-126">Der DVD-Navigator befindet sich in der DVD-stoppdomäne.</span><span class="sxs-lookup"><span data-stu-id="5f421-126">The DVD Navigator is in the DVD Stop domain.</span></span>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f421-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5f421-127">Return value</span></span>

<span data-ttu-id="5f421-128">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5f421-128">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f421-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f421-129">Remarks</span></span>

<span data-ttu-id="5f421-130">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="5f421-130">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="5f421-131">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="5f421-131">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="5f421-132">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5f421-132">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f421-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5f421-133">Requirements</span></span>



| <span data-ttu-id="5f421-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5f421-134">Requirement</span></span> | <span data-ttu-id="5f421-135">Wert</span><span class="sxs-lookup"><span data-stu-id="5f421-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5f421-136">Version</span><span class="sxs-lookup"><span data-stu-id="5f421-136">Version</span></span><br/> | <span data-ttu-id="5f421-137">Windows Media Player für Windows XP oder höher.</span><span class="sxs-lookup"><span data-stu-id="5f421-137">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="5f421-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5f421-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="5f421-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f421-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f421-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f421-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f421-141">**DVD-Objekt**</span><span class="sxs-lookup"><span data-stu-id="5f421-141">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="5f421-142">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="5f421-142">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





