---
title: Externes. OnViewChange-Ereignis
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Das OnViewChange-Ereignis tritt auf, wenn sich die Sicht in Windows Media Player ändert.
ms.assetid: aa1378ad-8b84-4592-85c5-5e284be05ea6
keywords:
- Externe. OnViewChange-Ereignisfenster Media Player
topic_type:
- apiref
api_name:
- External.OnViewChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7144e03955fb67ed90cad4a4336bf782ca1566
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369546"
---
# <a name="externalonviewchange-event"></a><span data-ttu-id="462e5-106">Externes. OnViewChange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="462e5-106">External.OnViewChange Event</span></span>

> [!Note]  
> <span data-ttu-id="462e5-107">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="462e5-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="462e5-108">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="462e5-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="462e5-109">Das **OnViewChange** -Ereignis tritt auf, wenn sich die Sicht in Windows Media Player ändert.</span><span class="sxs-lookup"><span data-stu-id="462e5-109">The **OnViewChange** event occurs when the view changes in Windows Media Player.</span></span>

``` syntax
window.external.OnViewChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="462e5-110">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="462e5-110">Possible Values</span></span>

<span data-ttu-id="462e5-111">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die den Namen der Funktion im Skript angibt, die von Windows Media Player bei Auftreten des Ereignisses aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="462e5-111">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="462e5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="462e5-112">Parameters</span></span>

<span data-ttu-id="462e5-113">Die Funktion, die dieses Ereignis behandelt, nimmt keine Parameter an.</span><span class="sxs-lookup"><span data-stu-id="462e5-113">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="462e5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="462e5-114">Remarks</span></span>

<span data-ttu-id="462e5-115">Die Ansicht in Windows Media Player kann aus einem der folgenden Gründe geändert werden:</span><span class="sxs-lookup"><span data-stu-id="462e5-115">The view in Windows Media Player can change for any of the following reasons:</span></span>

-   <span data-ttu-id="462e5-116">Der Benutzer interagiert mit der Windows Media Player-Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="462e5-116">The user interacts with the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="462e5-117">Der Benutzer interagiert mit einer Ermittlungs Seite, und das Skript auf der Ermittlungs Seite ruft [extern. changeView](external-changeview.md)auf.</span><span class="sxs-lookup"><span data-stu-id="462e5-117">The user interacts with a discovery page, and script on the discovery page calls [External.changeView](external-changeview.md).</span></span>
-   <span data-ttu-id="462e5-118">Der Benutzer interagiert mit einer Ermittlungs Seite, und das Skript auf der Ermittlungs Seite ruft [extern. changeviewonlinelist](external-changeviewonlinelist.md)auf.</span><span class="sxs-lookup"><span data-stu-id="462e5-118">The user interacts with a discovery page, and script on the discovery page calls [External.changeViewOnlineList](external-changeviewonlinelist.md).</span></span>

<span data-ttu-id="462e5-119">Wenn sich die Ansicht in Windows Media Player ändert, ruft der Player [iwmpcontentpartner:: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) auf, um die URL der nächsten Ermittlungs Seite anzuzeigen, die angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="462e5-119">When the view changes in Windows Media Player, the Player calls [IWMPContentPartner::GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) to get the URL of the next discovery page to display.</span></span> <span data-ttu-id="462e5-120">Bevor der Spieler jedoch die neue Ermittlungs Seite anzeigt, löst er das **OnViewChange** -Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="462e5-120">However, before the Player displays the new discovery page, it raises the **OnViewChange** event.</span></span> <span data-ttu-id="462e5-121">Wenn der **OnViewChange** -Ereignishandler " [extern. cancelnavigate](external-cancelnavigate.md)" aufruft, zeigt Windows Media Player die Seite "neue Ermittlung" nicht an.</span><span class="sxs-lookup"><span data-stu-id="462e5-121">If the **OnViewChange** event handler calls [External.cancelNavigate](external-cancelnavigate.md), Windows Media Player does not display the new discovery page.</span></span> <span data-ttu-id="462e5-122">Stattdessen wird die aktuelle Ermittlungs Seite weiterhin angezeigt.</span><span class="sxs-lookup"><span data-stu-id="462e5-122">Instead, it continues to display the current discovery page.</span></span>

## <a name="requirements"></a><span data-ttu-id="462e5-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="462e5-123">Requirements</span></span>



| <span data-ttu-id="462e5-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="462e5-124">Requirement</span></span> | <span data-ttu-id="462e5-125">Wert</span><span class="sxs-lookup"><span data-stu-id="462e5-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="462e5-126">Version</span><span class="sxs-lookup"><span data-stu-id="462e5-126">Version</span></span><br/> | <span data-ttu-id="462e5-127">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="462e5-127">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="462e5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="462e5-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="462e5-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="462e5-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="462e5-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="462e5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="462e5-131">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="462e5-131">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="462e5-132">**Extern. changeView**</span><span class="sxs-lookup"><span data-stu-id="462e5-132">**External.changeView**</span></span>](external-changeview.md)
</dt> <dt>

[<span data-ttu-id="462e5-133">**Extern. changeviewonlinelist**</span><span class="sxs-lookup"><span data-stu-id="462e5-133">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> </dl>

 

 





