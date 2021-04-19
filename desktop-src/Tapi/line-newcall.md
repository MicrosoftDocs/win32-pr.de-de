---
description: Die TSPI-Zeilen- \_ newcall-Meldung wird immer dann an die LineEvent-Rückruffunktion gesendet, wenn ein neuer Aufruf, den TAPI nicht ausgelöst hat, in einer Zeile ankommt, die TAPI geöffnet hat.
ms.assetid: 36122dfb-1ed6-459d-aa2b-69c86daaddd8
title: LINE_NEWCALL Meldung (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed3e7380b2f328283e5f5cad9e84f5a1d0c450dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361911"
---
# <a name="line_newcall-message"></a><span data-ttu-id="15423-103">Zeilen- \_ newcallmeldung</span><span class="sxs-lookup"><span data-stu-id="15423-103">LINE\_NEWCALL message</span></span>

<span data-ttu-id="15423-104">Die TSPI- **Zeilen- \_ newcall-Meldung** wird immer dann an die [**LineEvent**](/windows/win32/api/tspi/nc-tspi-lineevent) -Rückruffunktion gesendet, wenn ein neuer Aufruf, den TAPI nicht ausgelöst hat, in einer Zeile ankommt, die TAPI geöffnet hat.</span><span class="sxs-lookup"><span data-stu-id="15423-104">The TSPI **LINE\_NEWCALL** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function whenever a new call that TAPI has not originated arrives on a line that TAPI has open.</span></span> <span data-ttu-id="15423-105">Dies muss die erste gesendete Nachricht bezüglich dieses Aufrufes sein.</span><span class="sxs-lookup"><span data-stu-id="15423-105">This must be the first message sent regarding that call.</span></span> <span data-ttu-id="15423-106">TAPI schreibt das nicht transparente " *htcallhandle* "-Handle an den Speicherort, der vom Dienstanbieter als *dwParam2*</span><span class="sxs-lookup"><span data-stu-id="15423-106">TAPI writes the *htCall* opaque handle to the location passed by the service provider as *dwParam2*.</span></span> <span data-ttu-id="15423-107">Dadurch erhält der Dienstanbieter den Wert " *htcall"* , der in nachfolgenden Nachrichten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="15423-107">This gives the service provider the *htCall* value to be used in subsequent messages.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="15423-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="15423-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15423-109">*htline*</span><span class="sxs-lookup"><span data-stu-id="15423-109">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="15423-110">Das nicht transparente TAPI-Objekt Handle für das liniengerät.</span><span class="sxs-lookup"><span data-stu-id="15423-110">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="15423-111">*"htcall"*</span><span class="sxs-lookup"><span data-stu-id="15423-111">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="15423-112">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="15423-112">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="15423-113">*dwmsg*</span><span class="sxs-lookup"><span data-stu-id="15423-113">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="15423-114">Der Wert für den Zeilen- \_ newcall.</span><span class="sxs-lookup"><span data-stu-id="15423-114">The value LINE\_NEWCALL.</span></span>

</dd> <dt>

<span data-ttu-id="15423-115">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="15423-115">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="15423-116">Das nicht transparente Handle des Dienstanbieters für den-Befehl vom Typ [**hdrvcall.**](hdrvline.md)</span><span class="sxs-lookup"><span data-stu-id="15423-116">The service provider's opaque handle for the call, of type [**HDRVCALL**](hdrvline.md).</span></span> <span data-ttu-id="15423-117">TAPI übergibt diesen Wert als *hdcallparameter* , um den Aufruf in nachfolgenden Prozeduren zu identifizieren, die für den Aufruf aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="15423-117">TAPI passes this value as the *hdCall* parameter to identify the call in subsequent procedures it invokes to operate on the call.</span></span>

</dd> <dt>

<span data-ttu-id="15423-118">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="15423-118">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="15423-119">Ein Zeiger vom Typ lphtapicall, der auf [**htapicall**](htapicall.md)verweist.</span><span class="sxs-lookup"><span data-stu-id="15423-119">A pointer of type LPHTAPICALL pointing to a [**HTAPICALL**](htapicall.md).</span></span> <span data-ttu-id="15423-120">TAPI schreibt das nicht transparente TAPI-Handle für den aufzurufenden Speicherort.</span><span class="sxs-lookup"><span data-stu-id="15423-120">TAPI writes the TAPI opaque handle for the call to the indicated location.</span></span> <span data-ttu-id="15423-121">Der Dienstanbieter muss diesen Wert speichern und als den Parameter " *htcall"* übergeben, um den-Rückruf in nachfolgenden Ereignissen zu identifizieren, die er für den-Befehl meldet.</span><span class="sxs-lookup"><span data-stu-id="15423-121">The service provider must save this value and pass it as the *htCall* parameter to identify the call in subsequent events it reports for the call.</span></span>

<span data-ttu-id="15423-122">Dieser Parameter kann auch den Wert **null** abrufen (siehe folgenden Abschnitt "Hinweise").</span><span class="sxs-lookup"><span data-stu-id="15423-122">This parameter can also acquire a value of **NULL** (see the following Remarks section).</span></span>

</dd> <dt>

<span data-ttu-id="15423-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="15423-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="15423-124">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="15423-124">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15423-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15423-125">Remarks</span></span>

<span data-ttu-id="15423-126">Der Dienstanbieter sollte die [**Zeilen \_ Aufruf Zustands**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) Meldung als nächste Nachricht für diesen Aufruf senden.</span><span class="sxs-lookup"><span data-stu-id="15423-126">The service provider should send the [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) message as the next message for this call.</span></span> <span data-ttu-id="15423-127">Das **Zeilen- \_ newcall-Ereignis** ist insofern ungewöhnlich, als dass es auch einen Wert an den Dienstanbieter zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="15423-127">The **LINE\_NEWCALL** event is unusual in that it also passes a value back to the service provider.</span></span>

<span data-ttu-id="15423-128">Diese Funktion meldet alle neuen Aufrufe, die aus dem Dienstanbieter stammen (eingehend, ausgehend, initiiert am Telefon usw.), für die TAPI und der Dienstanbieter noch keine nicht transparenten Handles ausgetauscht haben.</span><span class="sxs-lookup"><span data-stu-id="15423-128">This function reports any new calls that originate in the service provider (inbound, outbound, initiated at the phone, and so on) for which TAPI and the service provider have not yet exchanged opaque handles.</span></span> <span data-ttu-id="15423-129">Die Handles werden ausgetauscht, sodass TAPI und der Dienstanbieter dann Anfragen ausführen und Ereignisse mit dem-Befehl melden können.</span><span class="sxs-lookup"><span data-stu-id="15423-129">The handles are exchanged so that TAPI and the service provider can subsequently make requests and report events involving the call.</span></span> <span data-ttu-id="15423-130">Da diese neuen Aufrufe nicht zwangsläufig eingehenden, können sich die Aufrufe anfänglich in einem beliebigen Zustand befinden, nicht notwendigerweise dem *Angebots* Zustand.</span><span class="sxs-lookup"><span data-stu-id="15423-130">Because these new calls are not necessarily inbound, the calls can initially be in any state, not necessarily the *offering* state.</span></span> <span data-ttu-id="15423-131">Wenn der Dienstanbieter startet und ermittelt, dass ein oder mehrere Aufrufe bereits in der Zeile aktiv sind, informiert er TAPI über diese mit **Zeilen \_ newcallnachrichten** gefolgt von [**Zeilen \_ Aufruf Zustands**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) Meldungen, die den aktuellen Zustand angeben.</span><span class="sxs-lookup"><span data-stu-id="15423-131">If the service provider starts and discovers that one or more calls are already active on the line, it informs TAPI of them with **LINE\_NEWCALL** messages followed by [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) messages indicating the current state.</span></span> <span data-ttu-id="15423-132">Ein neuer ausgehender Aufruf, der vom Benutzer auf dem Telefon initiiert wurde, wird mit einer Zeile für einen **Zeilen \_ neuanruf** gemeldet, und die anfängliche **Zeile \_ CallState** -Meldung gibt an, dass der Aufruf im Zustand " **Dialtone** " war (und dann fortfahren).</span><span class="sxs-lookup"><span data-stu-id="15423-132">A new outgoing call, initiated on the phone by the user, would be reported with a **LINE\_NEWCALL** message, and the initial **LINE\_CALLSTATE** message would indicate that the call was in **DIALTONE** state (and then continuing on from there).</span></span>

<span data-ttu-id="15423-133">Wenn der Dienstanbieter innerhalb eines sehr kurzen Zeitraums eine große Anzahl von Aufrufen an TAPI übergibt (während desselben interruptcycle), kann TAPI bei der Verarbeitung dieser Aufrufe Rück protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="15423-133">If the service provider passes a large number of calls to TAPI in a very short amount of time (during the same interrupt cycle), TAPI can become backlogged in processing those calls.</span></span> <span data-ttu-id="15423-134">Wenn dies geschieht, signalisiert TAPI dem Dienstanbieter, dass vor dem Senden von weiteren Aufrufen eine kurze Zeit gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="15423-134">When this happens, TAPI signals to the service provider to wait a short time before sending any more calls.</span></span> <span data-ttu-id="15423-135">Dies signalisiert dies durch Schreiben eines Werts von **null** anstelle eines gültigen [**htapicall**](htapicall.md)-Werts in den Speicherort, auf den durch den *dwParam2* -Parameter von **Zeile \_ newcallverwiesen** wird.</span><span class="sxs-lookup"><span data-stu-id="15423-135">It signals this by writing a value of **NULL**, instead of a valid [**HTAPICALL**](htapicall.md), into the location pointed to by the *dwParam2* parameter of **LINE\_NEWCALL**.</span></span> <span data-ttu-id="15423-136">Dies weist darauf hin, dass der Versuch, das neu angebotene Telefon Handle zu verarbeiten, nicht erfolgreich war. Dies liegt wahrscheinlich daran, dass nicht genügend Arbeitsspeicher belegt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="15423-136">This indicates that the attempt to process the newly offered call handle was not successful, most likely due to a temporary inability to allocate memory.</span></span> <span data-ttu-id="15423-137">Der Dienstanbieter kann durch Löschen des Aufrufes oder durch erneutes Senden der **Zeile neuer \_ Aufruf** Nachricht nach einer Zeit Plan Verzögerung Antworten (während dieser Zeit sollte der Dienstanbieter den Prozessor erhalten, damit TAPI andere ausstehende Aktionen verarbeiten kann).</span><span class="sxs-lookup"><span data-stu-id="15423-137">The service provider can respond by dropping the call or by resending the **LINE\_NEWCALL** message after a scheduling delay (during which time the service provider should yield the processor to allow TAPI to process other pending actions).</span></span> <span data-ttu-id="15423-138">In jedem Fall können keine weiteren Nachrichten bezüglich des neuen Aufrufes an TAPI weitergegeben werden, bis der Handle-Austausch erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="15423-138">In any case, no further messages regarding the new call can be passed to TAPI until the handle exchange succeeds.</span></span> <span data-ttu-id="15423-139">Wenn der Speicherort, auf den von *dwParam2* verwiesen wird, einen Wert ungleich **null** erhält, weiß der Dienstanbieter, dass dieser Wert ein gültiges [**htapicall**](htapicall.md) -Handle für den-Befehl ist.</span><span class="sxs-lookup"><span data-stu-id="15423-139">When the location pointed to by *dwParam2* acquires a non-**NULL** value, the service provider knows that this value is a valid [**HTAPICALL**](htapicall.md) handle to the call.</span></span>

<span data-ttu-id="15423-140">Es gibt keine direkt entsprechende Meldung auf der TAPI-Ebene.</span><span class="sxs-lookup"><span data-stu-id="15423-140">There is no directly corresponding message at the TAPI level.</span></span> <span data-ttu-id="15423-141">Diese Meldung wird auf der TSPI-Ebene verwendet, um einen neuen eingehenden Befehl in TAPI eindeutig und eindeutig einzuführen und den nicht transparenten TAPI-Bezeichner für den-Befehl abzurufen.</span><span class="sxs-lookup"><span data-stu-id="15423-141">This message is used at the TSPI level to uniquely and unambiguously introduce a new incoming call to TAPI and retrieve the TAPI opaque identifier for the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="15423-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15423-142">Requirements</span></span>



| <span data-ttu-id="15423-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15423-143">Requirement</span></span> | <span data-ttu-id="15423-144">Wert</span><span class="sxs-lookup"><span data-stu-id="15423-144">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="15423-145">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="15423-145">TAPI version</span></span><br/> | <span data-ttu-id="15423-146">Erfordert TAPI 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="15423-146">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="15423-147">Header</span><span class="sxs-lookup"><span data-stu-id="15423-147">Header</span></span><br/>       | <dl> <span data-ttu-id="15423-148"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="15423-148"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15423-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15423-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="15423-150">[**\_liniencallstate**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="15423-150">[**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="15423-151">**LineEvent**</span><span class="sxs-lookup"><span data-stu-id="15423-151">**LINEEVENT**</span></span>](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> </dl>

 

