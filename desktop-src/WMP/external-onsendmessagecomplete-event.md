---
title: Externes. onsendmessagecomplete-Ereignis
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Externes. onsendmessagecomplete-Ereignis
ms.assetid: 9ae60aa5-4ecd-41dd-aeb0-afb1a3686982
keywords:
- Externe. onsendmessagecomplete-Ereignisfenster Media Player
topic_type:
- apiref
api_name:
- External.OnSendMessageComplete Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d4de69a753811537f60ae8a3244cfaf012f60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367439"
---
# <a name="externalonsendmessagecomplete-event"></a><span data-ttu-id="92201-105">Externes. onsendmessagecomplete-Ereignis</span><span class="sxs-lookup"><span data-stu-id="92201-105">External.OnSendMessageComplete Event</span></span>

> [!Note]  
> <span data-ttu-id="92201-106">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="92201-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="92201-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="92201-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="92201-108">Das **onsendmessagecomplete** -Ereignis tritt auf, wenn der Online Shop die Verarbeitung einer Nachricht abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="92201-108">The **OnSendMessageComplete** event occurs when the online store has finished processing a message.</span></span> <span data-ttu-id="92201-109">Das Skript auf der Ermittlungs Seite hat die Nachricht zuvor durch Aufrufen von " [extern. SendMessage](external-sendmessage.md)" gesendet.</span><span class="sxs-lookup"><span data-stu-id="92201-109">Script on the discovery page previously sent the message by calling [External.sendMessage](external-sendmessage.md).</span></span>

``` syntax
window.external.OnSendMessageComplete = FunctionName
```

## <a name="possible-values"></a><span data-ttu-id="92201-110">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="92201-110">Possible Values</span></span>

<span data-ttu-id="92201-111">Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die den Namen der Funktion im Skript angibt, die von Windows Media Player bei Auftreten des Ereignisses aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="92201-111">This is a write-only property that specifies the name of the function in script that Windows Media Player calls when the event occurs.</span></span>

## <a name="parameters"></a><span data-ttu-id="92201-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="92201-112">Parameters</span></span>

<span data-ttu-id="92201-113">Die Funktion, die dieses Ereignis behandelt, verfügt über die folgenden Parameter.</span><span class="sxs-lookup"><span data-stu-id="92201-113">The function that handles this event has the following parameters.</span></span>

<dl> <dt>

<span data-ttu-id="92201-114"><span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Meldung*</span><span class="sxs-lookup"><span data-stu-id="92201-114"><span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Msg*</span></span>
</dt> <dd>

<span data-ttu-id="92201-115">Dieselbe Zeichenfolge, die im **msg** -Parameter von **SendMessage** übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="92201-115">The same string that was passed in the **Msg** parameter of **sendMessage**.</span></span>

</dd> <dt>

<span data-ttu-id="92201-116"><span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*</span><span class="sxs-lookup"><span data-stu-id="92201-116"><span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Param*</span></span>
</dt> <dd>

<span data-ttu-id="92201-117">Dieselbe Zeichenfolge, die im **param** -Parameter von **SendMessage** übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="92201-117">The same string that was passed in the **Param** parameter of **sendMessage**.</span></span>

</dd> <dt>

<span data-ttu-id="92201-118"><span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Dadurch*</span><span class="sxs-lookup"><span data-stu-id="92201-118"><span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Result*</span></span>
</dt> <dd>

<span data-ttu-id="92201-119">Eine **Zeichen** Folge, die das Ergebnis der Nachrichten Behandlung enthält.</span><span class="sxs-lookup"><span data-stu-id="92201-119">**String** that contains the result of the message handling.</span></span> <span data-ttu-id="92201-120">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="92201-120">See Remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92201-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92201-121">Remarks</span></span>

<span data-ttu-id="92201-122">Die **SendMessage** -Methode ruft [iwmpcontentpartner:: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)auf, das asynchron zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="92201-122">The **sendMessage** method calls [IWMPContentPartner::SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), which returns asynchronously.</span></span> <span data-ttu-id="92201-123">Das heißt, es wird zurückgegeben, bevor der Online Shop die Verarbeitung der Nachricht abschließt.</span><span class="sxs-lookup"><span data-stu-id="92201-123">That is, it returns before the online store finishes processing the message.</span></span> <span data-ttu-id="92201-124">Wenn der Online Shop die Verarbeitung der Nachricht abgeschlossen hat, wird [iwmpcontentpartnercallback:: sendmessagecomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)aufgerufen, das wiederum den **onsendmessagecomplete** -Ereignishandler des Skripts aufruft.</span><span class="sxs-lookup"><span data-stu-id="92201-124">When the online store finishes processing the message, it calls [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), which in turn calls the script's **OnSendMessageComplete** event handler.</span></span>

<span data-ttu-id="92201-125">Wenn der Onlinespeicher **iwmpcontentpartnercallback:: sendmessagecomplete** aufruft, liefert er einen Ergebniscode im *bstrinresult* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="92201-125">When the online store calls **IWMPContentPartnerCallback::SendMessageComplete**, it supplies a result code in the *bstrResult* parameter.</span></span> <span data-ttu-id="92201-126">Der Ergebniscode wird von Windows Media Player nicht interpretiert.</span><span class="sxs-lookup"><span data-stu-id="92201-126">Windows Media Player does not interpret that result code.</span></span> <span data-ttu-id="92201-127">Stattdessen übergibt Windows Media Player den Ergebniscode an den **onsendmessagecomplete** -Ereignishandler im *Ergebnis* Parameter.</span><span class="sxs-lookup"><span data-stu-id="92201-127">Instead, Windows Media Player passes the result code along to the **OnSendMessageComplete** event handler in the *Result* parameter.</span></span>

<span data-ttu-id="92201-128">Keiner der Parameter (*msg*, *param*, *Result*) des **onsendmessagecomplete** -Ereignis Handlers wird von Windows Media Player interpretiert.</span><span class="sxs-lookup"><span data-stu-id="92201-128">None of the parameters (*Msg*, *Param*, *Result*) of the **OnSendMessageComplete** event handler is interpreted by Windows Media Player.</span></span> <span data-ttu-id="92201-129">Die Parameter sind nur für den Online Shop von Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="92201-129">The parameters have meaning only to the online store.</span></span>

## <a name="requirements"></a><span data-ttu-id="92201-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92201-130">Requirements</span></span>



| <span data-ttu-id="92201-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92201-131">Requirement</span></span> | <span data-ttu-id="92201-132">Wert</span><span class="sxs-lookup"><span data-stu-id="92201-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92201-133">Version</span><span class="sxs-lookup"><span data-stu-id="92201-133">Version</span></span><br/> | <span data-ttu-id="92201-134">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="92201-134">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="92201-135">DLL</span><span class="sxs-lookup"><span data-stu-id="92201-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="92201-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92201-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92201-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92201-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92201-138">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="92201-138">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="92201-139">**Extern. SendMessage**</span><span class="sxs-lookup"><span data-stu-id="92201-139">**External.sendMessage**</span></span>](external-sendmessage.md)
</dt> <dt>

[<span data-ttu-id="92201-140">**Iwmpcontentpartner:: SendMessage**</span><span class="sxs-lookup"><span data-stu-id="92201-140">**IWMPContentPartner::SendMessage**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[<span data-ttu-id="92201-141">**Iwmpcontentpartnercallback:: sendmessagecomplete**</span><span class="sxs-lookup"><span data-stu-id="92201-141">**IWMPContentPartnerCallback::SendMessageComplete**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





