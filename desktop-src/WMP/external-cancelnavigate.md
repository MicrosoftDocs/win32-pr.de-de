---
title: Extern. cancelnavigate-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. cancelnavigate-Methode
ms.assetid: e65d64fb-292c-4413-9727-b24609e78d68
keywords:
- cancelnavigate-Methode, Windows-Media Player
- cancelnavigate-Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, cancelnavigate-Methode
topic_type:
- apiref
api_name:
- External.cancelNavigate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6cbc0f749fd6ca33d78dfaed1d256634eb9c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370263"
---
# <a name="externalcancelnavigate-method"></a><span data-ttu-id="2103c-107">Extern. cancelnavigate-Methode</span><span class="sxs-lookup"><span data-stu-id="2103c-107">External.cancelNavigate method</span></span>

> [!Note]  
> <span data-ttu-id="2103c-108">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="2103c-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="2103c-109">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2103c-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="2103c-110">Die **cancelnavigate** -Methode informiert Windows Media Player, dass eine neue Ermittlungs Seite auch dann nicht angezeigt werden soll, wenn sich die Ansicht im Player geändert hat.</span><span class="sxs-lookup"><span data-stu-id="2103c-110">The **cancelNavigate** method informs Windows Media Player that it should not display a new discovery page even though the view has changed in the Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="2103c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2103c-111">Syntax</span></span>


```JScript
External.cancelNavigate()
```



## <a name="parameters"></a><span data-ttu-id="2103c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2103c-112">Parameters</span></span>

<span data-ttu-id="2103c-113">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2103c-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2103c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2103c-114">Return value</span></span>

<span data-ttu-id="2103c-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2103c-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2103c-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2103c-116">Remarks</span></span>

<span data-ttu-id="2103c-117">Wenn sich die Ansicht in Windows Media Player ändert, ruft der Player das Plug-in des Online Stores auf, um zu bestimmen, welche Ermittlungs Seite als nächstes angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2103c-117">When the view changes in Windows Media Player, the Player calls the online store's plug-in to determine which discovery page to display next.</span></span> <span data-ttu-id="2103c-118">In einigen Fällen kann es jedoch sein, dass der Player im Online Shop weiterhin die vorhandene Ermittlungs Seite anzeigt.</span><span class="sxs-lookup"><span data-stu-id="2103c-118">In some cases, however, the online store might want the Player to continue displaying the existing discovery page.</span></span> <span data-ttu-id="2103c-119">Der folgende Prozess bestimmt, ob der Spieler eine neue Ermittlungs Seite anzeigt:</span><span class="sxs-lookup"><span data-stu-id="2103c-119">The following process determines whether the Player displays a new discovery page:</span></span>

1.  <span data-ttu-id="2103c-120">Eine Aktion durch den Benutzer, entweder in der Benutzeroberfläche des Players oder auf der Ermittlungs Seite, fordert an, dass der Spieler seine Ansicht ändert.</span><span class="sxs-lookup"><span data-stu-id="2103c-120">An action by the user, either in the Player's user interface or on the discovery page, requests that the Player change its view.</span></span>
2.  <span data-ttu-id="2103c-121">Der Player Ruft die [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) -Methode des Plug-Ins auf, um zu bestimmen, welche Ermittlungs Seite als nächstes angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2103c-121">The Player calls the plug-in's [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) method to determine which discovery page to display next.</span></span> <span data-ttu-id="2103c-122">Der Player speichert die URL der neuen Ermittlungs Seite, zeigt jedoch derzeit nicht die neue Ermittlungs Seite an.</span><span class="sxs-lookup"><span data-stu-id="2103c-122">The Player stores the URL of the new discovery page but does not display the new discovery page at this time.</span></span>
3.  <span data-ttu-id="2103c-123">Der Player löst das [OnViewChange](external-onviewchange-event.md) -Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="2103c-123">The Player raises the [OnViewChange](external-onviewchange-event.md) event.</span></span>
4.  <span data-ttu-id="2103c-124">Wenn der **OnViewChange** -Ereignishandler auf der Ermittlungs Seite **cancelnavigate** aufruft, zeigt der Spieler nicht die neue Ermittlungs Seite an (in Schritt 2 festgelegt).</span><span class="sxs-lookup"><span data-stu-id="2103c-124">If the **OnViewChange** event handler on the discovery page calls **cancelNavigate**, the Player does not display the new discovery page (determined in step 2).</span></span> <span data-ttu-id="2103c-125">Stattdessen wird die vorhandene Ermittlungs Seite weiterhin angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2103c-125">Instead, it continues to display the existing discovery page.</span></span> <span data-ttu-id="2103c-126">Wenn der **OnViewChange** -Ereignishandler nicht **cancelnavigate** aufruft, zeigt der Spieler die neue Ermittlungs Seite an.</span><span class="sxs-lookup"><span data-stu-id="2103c-126">If the **OnViewChange** event handler does not call **cancelNavigate**, the Player does display the new discovery page.</span></span>

<span data-ttu-id="2103c-127">Angenommen, der Spieler zeigt derzeit die Ansicht eines Albums an, bei dem eine bestimmte Spur ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="2103c-127">For example, suppose the Player is currently displaying the view of an album with a certain track selected.</span></span> <span data-ttu-id="2103c-128">Außerdem wird angenommen, dass es sich bei der aktuellen Ermittlungs Seite um die Seite handelt, die das gesamte Album darstellt.</span><span class="sxs-lookup"><span data-stu-id="2103c-128">Also assume that the current discovery page is the page that represents the entire album.</span></span> <span data-ttu-id="2103c-129">Wenn der Benutzer auf eine andere Spur desselben Albums klickt, wird die Ansicht des Players leicht geändert, um anzuzeigen, dass die neue Spur ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="2103c-129">If the user clicks a different track from the same album, the Player's view changes slightly to show that the new track is selected.</span></span> <span data-ttu-id="2103c-130">Es ist jedoch nicht erforderlich, eine neue Ermittlungs Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2103c-130">But there is no need to display a new discovery page.</span></span> <span data-ttu-id="2103c-131">Die Suchseite, die das gesamte Album darstellt, ist immer noch die geeignete Seite, die der Player anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="2103c-131">The discovery page that represents the entire album is still the appropriate page for the Player to display.</span></span>

## <a name="requirements"></a><span data-ttu-id="2103c-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2103c-132">Requirements</span></span>



| <span data-ttu-id="2103c-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2103c-133">Requirement</span></span> | <span data-ttu-id="2103c-134">Wert</span><span class="sxs-lookup"><span data-stu-id="2103c-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2103c-135">Version</span><span class="sxs-lookup"><span data-stu-id="2103c-135">Version</span></span><br/> | <span data-ttu-id="2103c-136">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="2103c-136">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="2103c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2103c-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="2103c-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2103c-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2103c-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2103c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2103c-140">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="2103c-140">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="2103c-141">**Extern. changeviewonlinelist**</span><span class="sxs-lookup"><span data-stu-id="2103c-141">**External.changeViewOnlineList**</span></span>](external-changeviewonlinelist.md)
</dt> <dt>

[<span data-ttu-id="2103c-142">**Extern. OnViewChange**</span><span class="sxs-lookup"><span data-stu-id="2103c-142">**External.OnViewChange**</span></span>](external-onviewchange-event.md)
</dt> </dl>

 

 





