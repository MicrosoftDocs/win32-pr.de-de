---
title: Extern. SendMessage-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die SendMessage-Methode sendet eine Nachricht an das Plug-in des Online Stores.
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- SendMessage-Methode (Windows Media Player)
- SendMessage-Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, SendMessage-Methode
topic_type:
- apiref
api_name:
- External.sendMessage
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4648f3cf433a2828d3c97604ebf9ee6e7223b7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353008"
---
# <a name="externalsendmessage-method"></a><span data-ttu-id="6717d-108">Extern. SendMessage-Methode</span><span class="sxs-lookup"><span data-stu-id="6717d-108">External.sendMessage method</span></span>

> [!Note]  
> <span data-ttu-id="6717d-109">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="6717d-109">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="6717d-110">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6717d-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="6717d-111">Die **SendMessage** -Methode sendet eine Nachricht an das Plug-in des Online Stores.</span><span class="sxs-lookup"><span data-stu-id="6717d-111">The **sendMessage** method sends a message to the online store's plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="6717d-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="6717d-112">Syntax</span></span>


```JScript
External.sendMessage(
  Msg,
  Param
)
```



## <a name="parameters"></a><span data-ttu-id="6717d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="6717d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6717d-114"> Meldung \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6717d-114">*Msg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6717d-115">**Zeichenfolge** , die die Meldung enthält.</span><span class="sxs-lookup"><span data-stu-id="6717d-115">**String** containing the message.</span></span>

</dd> <dt>

<span data-ttu-id="6717d-116">*Param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6717d-116">*Param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6717d-117">**Zeichenfolge** mit Parametern, die der Meldung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6717d-117">**String** containing parameters associated with the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6717d-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6717d-118">Return value</span></span>

<span data-ttu-id="6717d-119">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6717d-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6717d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6717d-120">Remarks</span></span>

<span data-ttu-id="6717d-121">Die Nachricht wird asynchron gesendet.</span><span class="sxs-lookup"><span data-stu-id="6717d-121">The message is sent asynchronously.</span></span> <span data-ttu-id="6717d-122">Das heißt, dass diese Methode sofort zurückgegeben wird, anstatt darauf zu warten, dass die Nachricht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="6717d-122">That is, this method returns immediately rather than waiting for the message to be processed.</span></span> <span data-ttu-id="6717d-123">Wenn das Plug-in die Verarbeitung der Nachricht abgeschlossen hat, ruft es die [iwmpcontentpartnercallback:: sendmessagecomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) -Methode auf, die wiederum den [onsendmessagecomplete](external-onsendmessagecomplete-event.md) -Ereignishandler des Skripts aufruft.</span><span class="sxs-lookup"><span data-stu-id="6717d-123">When the plug-in finishes processing the message, it calls the [IWMPContentPartnerCallback::SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) method, which in turn calls the script's [OnSendMessageComplete](external-onsendmessagecomplete-event.md) event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="6717d-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6717d-124">Requirements</span></span>



| <span data-ttu-id="6717d-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6717d-125">Requirement</span></span> | <span data-ttu-id="6717d-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6717d-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6717d-127">Version</span><span class="sxs-lookup"><span data-stu-id="6717d-127">Version</span></span><br/> | <span data-ttu-id="6717d-128">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="6717d-128">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="6717d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6717d-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="6717d-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6717d-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6717d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6717d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6717d-132">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="6717d-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="6717d-133">**Extern. onsendmessagecomplete**</span><span class="sxs-lookup"><span data-stu-id="6717d-133">**External.OnSendMessageComplete**</span></span>](external-onsendmessagecomplete-event.md)
</dt> <dt>

[<span data-ttu-id="6717d-134">**Iwmpcontentpartner:: SendMessage**</span><span class="sxs-lookup"><span data-stu-id="6717d-134">**IWMPContentPartner::SendMessage**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[<span data-ttu-id="6717d-135">**Iwmpcontentpartnercallback:: sendmessagecomplete**</span><span class="sxs-lookup"><span data-stu-id="6717d-135">**IWMPContentPartnerCallback::SendMessageComplete**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





