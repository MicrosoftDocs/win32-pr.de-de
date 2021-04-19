---
title: Externes. onloginchange-Ereignis
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Externes. onloginchange-Ereignis
ms.assetid: 096794d5-977a-414f-8a98-b7998674c268
keywords:
- Externe. onloginchange-Ereignisfenster Media Player
topic_type:
- apiref
api_name:
- External.OnLoginChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b7d54da86ffdde896a44580567b0cd381725d5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355887"
---
# <a name="externalonloginchange-event"></a><span data-ttu-id="15637-105">Externes. onloginchange-Ereignis</span><span class="sxs-lookup"><span data-stu-id="15637-105">External.OnLoginChange Event</span></span>

> [!Note]  
> <span data-ttu-id="15637-106">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="15637-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="15637-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="15637-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="15637-108">Das **onloginchange** -Ereignis tritt auf, wenn der Anmeldestatus des Benutzers geändert wird oder wenn der Anmeldeversuch fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="15637-108">The **OnLoginChange** event occurs when the user's log-in status changes or when an attempt to log in fails.</span></span>

``` syntax
window.external.OnLoginChange = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="15637-109">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="15637-109">Possible Values</span></span>

<span data-ttu-id="15637-110">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die den Namen der Funktion im Skript angibt, die von Windows Media Player bei Auftreten des Ereignisses aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="15637-110">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="15637-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="15637-111">Parameters</span></span>

<span data-ttu-id="15637-112">Die Funktion, die dieses Ereignis behandelt, nimmt keine Parameter an.</span><span class="sxs-lookup"><span data-stu-id="15637-112">The function that handles this event takes no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="15637-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15637-113">Remarks</span></span>

<span data-ttu-id="15637-114">Dieses Ereignis tritt jedes Mal auf, wenn das Plug-in des Online Stores [iwmpcontentpartnercallback:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify)aufruft und dabei wmpcnloginstatechange im *Typparameter* übergibt.</span><span class="sxs-lookup"><span data-stu-id="15637-114">This event occurs every time the online store's plug-in calls [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnLoginStateChange in the *type* parameter.</span></span> <span data-ttu-id="15637-115">Manchmal führt das Plug-in diesen Rückruf aus, um Windows Media Player zu benachrichtigen, dass es eine Änderung des Anmelde Zustands des Benutzers gab.</span><span class="sxs-lookup"><span data-stu-id="15637-115">Sometimes the plug-in makes this call to notify Windows Media Player that there was a change in the user's log-in state.</span></span> <span data-ttu-id="15637-116">In anderen Zeiten führt das Plug-in diesen Versuch aus, den Player zu benachrichtigen, dass ein Anmeldeversuch fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="15637-116">Other times, the plug-in makes this call to notify the Player that an attempt to log in failed.</span></span> <span data-ttu-id="15637-117">Der *pContext* -Parameter der **Notify** -Methode gibt an, ob die Benachrichtigung für eine Änderung des Anmelde Zustands oder für einen fehlgeschlagenen Anmeldeversuch vorliegt.</span><span class="sxs-lookup"><span data-stu-id="15637-117">The *pContext* parameter of the **Notify** method specifies whether the notification is for a change of log-in state or for a failed log-in attempt.</span></span>

<span data-ttu-id="15637-118">Da jeder Aufruf von `Notify(wmpcnLoginStateChange, ...)` bewirkt, dass Windows Media Player das **onloginchange** -Ereignis auslöst, wird der **onloginchange** -Ereignishandler manchmal als Ergebnis einer Änderung des Anmelde Zustands aufgerufen und manchmal als Ergebnis eines fehlgeschlagenen Anmelde Versuchs.</span><span class="sxs-lookup"><span data-stu-id="15637-118">Because every call to `Notify(wmpcnLoginStateChange, ...)` causes Windows Media Player to raise the **OnLoginChange** event, the **OnLoginChange** event handler is called sometimes as the result of a change in log-in state and sometimes as the result of a failed log-in attempt.</span></span> <span data-ttu-id="15637-119">Um den aktuellen Anmeldestatus des Benutzers zu bestimmen, muss der **onloginchange** -Ereignishandler [extern. userloggedin](external-userloggedin.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="15637-119">To determine the user's current log-in state, the **OnLoginChange** event handler must call [External.userLoggedIn](external-userloggedin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15637-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15637-120">Requirements</span></span>



| <span data-ttu-id="15637-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15637-121">Requirement</span></span> | <span data-ttu-id="15637-122">Wert</span><span class="sxs-lookup"><span data-stu-id="15637-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15637-123">Version</span><span class="sxs-lookup"><span data-stu-id="15637-123">Version</span></span><br/> | <span data-ttu-id="15637-124">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="15637-124">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="15637-125">DLL</span><span class="sxs-lookup"><span data-stu-id="15637-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="15637-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15637-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15637-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15637-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15637-128">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="15637-128">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="15637-129">**Extern.-Anmelde Name**</span><span class="sxs-lookup"><span data-stu-id="15637-129">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="15637-130">**Extern. userloggedin**</span><span class="sxs-lookup"><span data-stu-id="15637-130">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





