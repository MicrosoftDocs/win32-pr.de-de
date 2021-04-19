---
description: Die TAPI-Zeile \_ appnewcallnachricht wird gesendet, um eine Anwendung zu benachrichtigen, wenn ein neues-Rückruf Handle in seinem Auftrag spontan erstellt wurde.
ms.assetid: 0c263025-e719-453e-91c4-a9f2d9321db3
title: LINE_APPNEWCALL Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33d24ca816fb69384e90e4215edbc90b9410b887
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368672"
---
# <a name="line_appnewcall-message"></a><span data-ttu-id="950ea-103">Zeile \_ appnewcallmeldung</span><span class="sxs-lookup"><span data-stu-id="950ea-103">LINE\_APPNEWCALL message</span></span>

<span data-ttu-id="950ea-104">Die TAPI- **Zeile \_ appnewcallnachricht** wird gesendet, um eine Anwendung zu benachrichtigen, wenn ein neues Rückruf Handle in seinem Namen (mit Ausnahme eines API-Aufrufes von der Anwendung) spontan erstellt wurde. in diesem Fall würde das Handle durch einen Zeiger Parameter zurückgegeben werden, der an die Funktion übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="950ea-104">The TAPI **LINE\_APPNEWCALL** message is sent to inform an application when a new call handle has been spontaneously created on its behalf (other than through an API call from the application, in which case the handle would have been returned through a pointer parameter passed into the function).</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="950ea-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="950ea-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="950ea-106">*hdevice*</span><span class="sxs-lookup"><span data-stu-id="950ea-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="950ea-107">Das Handle der Anwendung für das liniengerät, für das der-Rückruf erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="950ea-107">The application's handle to the line device on which the call has been created.</span></span>

</dd> <dt>

<span data-ttu-id="950ea-108">*dwcallbackinstance*</span><span class="sxs-lookup"><span data-stu-id="950ea-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="950ea-109">Die beim Öffnen der Zeile des Aufrufs angegebene Rückruf Instanz.</span><span class="sxs-lookup"><span data-stu-id="950ea-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="950ea-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="950ea-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="950ea-111">Der Bezeichner der Adresse in der Zeile, für die der-Befehl angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="950ea-111">Identifier of the address on the line on which the call appears.</span></span> <span data-ttu-id="950ea-112">Ein Adress Bezeichner ist dauerhaft einer Adresse zugeordnet. der Bezeichner bleibt bei Betriebssystem Upgrades konstant.</span><span class="sxs-lookup"><span data-stu-id="950ea-112">An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.</span></span>

</dd> <dt>

<span data-ttu-id="950ea-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="950ea-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="950ea-114">Das Handle der Anwendung für den neuen-Befehl.</span><span class="sxs-lookup"><span data-stu-id="950ea-114">The application's handle to the new call.</span></span>

</dd> <dt>

<span data-ttu-id="950ea-115">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="950ea-115">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="950ea-116">Die Anwendungs Berechtigung für den neuen-Befehl (linecallprivilege- \_ Besitzer oder linecallprivilege- \_ Monitor).</span><span class="sxs-lookup"><span data-stu-id="950ea-116">The applications privilege to the new call (LINECALLPRIVILEGE\_OWNER or LINECALLPRIVILEGE\_MONITOR).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="950ea-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="950ea-117">Return value</span></span>

<span data-ttu-id="950ea-118">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="950ea-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="950ea-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="950ea-119">Remarks</span></span>

<span data-ttu-id="950ea-120">Anwendungen, die TAPI-Version 2,0 oder höher unterstützen, werden immer dann an eine **Zeile \_ appnewcallnachricht** gesendet, wenn der Anwendung ein Handle für einen neuen Aufruf übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="950ea-120">Applications supporting TAPI version 2.0 or later are sent a **LINE\_APPNEWCALL** message whenever the application is spontaneously given a handle to a new call.</span></span> <span data-ttu-id="950ea-121">Da die Nachricht die Parameter " *hline* " und " *dwadressssid* " enthält, für die der-Befehl vorhanden ist, kann die Anwendung ein neues-Objekt im richtigen Kontext erstellen.</span><span class="sxs-lookup"><span data-stu-id="950ea-121">Because the message includes the *hLine* and *dwAddressID* parameters on which the call exists, the application can readily create a new call object in the correct context.</span></span> <span data-ttu-id="950ea-122">Der **\_ appnewcallmessage-Zeile** folgt immer sofort eine [**Zeile \_ CallState**](line-callstate.md) -Meldung, die den ursprünglichen Status des Aufrufes angibt.</span><span class="sxs-lookup"><span data-stu-id="950ea-122">The **LINE\_APPNEWCALL** message is always immediately followed by a [**LINE\_CALLSTATE**](line-callstate.md) message indicating the initial state of the call.</span></span>

<span data-ttu-id="950ea-123">Ältere Anwendungen (die eine API-Version vor 2,0 ausgehandelt haben) werden nur als [**Zeilen- \_ CallState**](line-callstate.md) -Nachricht gesendet, wie in früheren Versionen der API dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="950ea-123">Older applications (that negotiated an API version earlier than 2.0) are sent only a [**LINE\_CALLSTATE**](line-callstate.md) message, as documented in previous versions of the API.</span></span> <span data-ttu-id="950ea-124">Solche Anwendungen würden beim Empfangen einer [**Zeile \_ CallState**](line-callstate.md) -Nachricht ein neues Aufruf Objekt erstellen, bei dem *dwParam3* auf einen Wert ungleich 0 (null) festgelegt ist und ein Aufruf Handle enthält, das von der Anwendung derzeit nicht bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="950ea-124">Such applications would create a new call object upon receiving a [**LINE\_CALLSTATE**](line-callstate.md) message that has *dwParam3* set to a nonzero value and containing a call handle not presently known by the application.</span></span> <span data-ttu-id="950ea-125">Der Nachteil ist, dass die Anwendung [**linegetcallinfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) aufrufen muss, um die dem Aufruf zugeordneten *hline* -und *dwadressssid* -Parameter zu bestimmen. (b) die Anwendung muss alle bekannten aufrufhandles Scannen, um zu bestimmen, ob der-Befehl ein neuer-Befehl ist. und (c) Es ist möglich, unter bestimmten Bedingungen kann die Anwendung annehmen, dass Sie ein neues Aufruf handle empfängt, wenn Sie in der Praxis gerade das zugehörige Handle für den Aufruf freigegeben hat (z. b. hat die Anwendung soeben die Zuordnung eines Aufruf Handles aufgehoben, aber eine [**Zeile \_ CallState**](line-callstate.md) -Nachricht, die den [](/windows/desktop/api/Tapi/nf-tapi-linehandoff) Anwendungs Besitz des Aufrufes in der TAPI-Nachrichten Warteschlange der Anwendung bereitstellt).</span><span class="sxs-lookup"><span data-stu-id="950ea-125">The disadvantages are that (a) the application must call [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) to determine the *hLine* and *dwAddressID* parameters associated with the call; (b) the application must scan all known call handles to determine that the call is a new call; and (c) it is possible, under certain conditions, for the application to think it is receiving a new call handle when in reality it has just deallocated its handle to the call (for example, the application has just deallocated a call handle, but a [**LINE\_CALLSTATE**](line-callstate.md) message giving the application ownership of the call due to a [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) from another application was already in the application's TAPI message queue).</span></span>

## <a name="requirements"></a><span data-ttu-id="950ea-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="950ea-126">Requirements</span></span>



| <span data-ttu-id="950ea-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="950ea-127">Requirement</span></span> | <span data-ttu-id="950ea-128">Wert</span><span class="sxs-lookup"><span data-stu-id="950ea-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="950ea-129">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="950ea-129">TAPI version</span></span><br/> | <span data-ttu-id="950ea-130">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="950ea-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="950ea-131">Header</span><span class="sxs-lookup"><span data-stu-id="950ea-131">Header</span></span><br/>       | <dl> <span data-ttu-id="950ea-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="950ea-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="950ea-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="950ea-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="950ea-134">**\_liniencallstate**</span><span class="sxs-lookup"><span data-stu-id="950ea-134">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="950ea-135">**linegetcallinfo**</span><span class="sxs-lookup"><span data-stu-id="950ea-135">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[<span data-ttu-id="950ea-136">**linehandoff**</span><span class="sxs-lookup"><span data-stu-id="950ea-136">**lineHandoff**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehandoff)
</dt> </dl>

 

 




