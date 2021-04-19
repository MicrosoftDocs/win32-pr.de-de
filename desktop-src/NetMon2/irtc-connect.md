---
description: Mit der Connect-Methode wird die NPP mithilfe einer angegebenen NIC mit dem Netzwerk verbunden, und es werden Konfigurationsinformationen für die Verbindung bereitstellt.
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: 'Untc:: Connect-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a14e34aeb0be30165aa18ddc7da18028d715be01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348157"
---
# <a name="irtcconnect-method"></a><span data-ttu-id="6a7ff-103">Untc:: Connect-Methode</span><span class="sxs-lookup"><span data-stu-id="6a7ff-103">IRTC::Connect method</span></span>

<span data-ttu-id="6a7ff-104">Mit der **Connect** -Methode wird die NPP mithilfe einer angegebenen NIC mit dem Netzwerk verbunden, und es werden Konfigurationsinformationen für die Verbindung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a7ff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a7ff-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID FramesCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="6a7ff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a7ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a7ff-107">*hinputblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a7ff-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a7ff-108">Handle für das BLOB, das die NIC angibt, mit der Sie eine Verbindung herstellen, und die Konfigurationsinformationen für diese Verbindung.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-108">Handle to the BLOB that specifies the NIC that you are connecting to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ff-109">*Status callbackproc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a7ff-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a7ff-110">Adresse der Status Rückruffunktion des Benutzers, die Statusaktualisierungen (z. b. Trigger) empfängt.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-110">Address of the user's status callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="6a7ff-111">Dieser Parameter kann auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-111">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ff-112">*Framescallbackproc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a7ff-112">*FramesCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a7ff-113">Adresse der Frame Rückruffunktion des Benutzers, die zum Empfangen von Statusaktualisierungen (z. b. Trigger) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-113">Address of the user's frame callback function, which is used to receive status updates such as triggers.</span></span> <span data-ttu-id="6a7ff-114">Dieser Parameter kann auf **null** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-114">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ff-115">*UserContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a7ff-115">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a7ff-116">Der Wert, der beim Aufrufen des Status und der Frame Rückruffunktion des Benutzers erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-116">Value passed when the user's status and frame callback function is called.</span></span> <span data-ttu-id="6a7ff-117">Wenn beide Rückruf Funktionen angegeben werden, muss der gleiche Benutzer Kontextwert verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-117">If both callback functions are specified, they must use the same user-context value.</span></span> <span data-ttu-id="6a7ff-118">Der Wert dieses Parameters ist in der Regel entweder HWND oder ein "This"-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-118">The value of this parameter is typically either HWND or a 'this' pointer.</span></span>

</dd> <dt>

<span data-ttu-id="6a7ff-119">*herrorblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6a7ff-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a7ff-120">Handle für ein fehlerblob, das zusätzliche Fehlerinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-120">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="6a7ff-121">Weitere Informationen zu den Funktionen im fehlerblob finden Sie in den Hinweisen am Ende dieses Themas.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-121">See Remarks at the bottom of this topic for information about what is in the error BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a7ff-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a7ff-122">Return value</span></span>

<span data-ttu-id="6a7ff-123">Wenn diese Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-123">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6a7ff-124">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes (einschließlich derjenigen, die vom internen " **iritc:: Configure** "-Befehl zurückgegeben werden):</span><span class="sxs-lookup"><span data-stu-id="6a7ff-124">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IRTC::Configure** call):</span></span>



| <span data-ttu-id="6a7ff-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6a7ff-125">Return code</span></span>                                                                                                         | <span data-ttu-id="6a7ff-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a7ff-126">Description</span></span>                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6a7ff-127"><dt>**nmerr \_ bereits \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ff-127"><dt>**NMERR\_ALREADY\_CONNECTED**</dt></span></span> </dl>            | <span data-ttu-id="6a7ff-128">Diese Instanz des NPP-com-Objekts ist bereits mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-128">This instance of the NPP COM object is already connected to the network.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="6a7ff-129"><dt>**nmerr- \_ BLOB- \_ Konvertierungs \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ff-129"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="6a7ff-130">Das konfigurationsblob ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-130">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="6a7ff-131">Dieser Fehler wird durch den " **untc:: Configure** "-Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-131">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="6a7ff-132"><dt>**der nmerr- \_ \_ blobeintrag \_ ist \_ nicht \_ vorhanden.**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ff-132"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="6a7ff-133">Für das vom *hinputblob* -Parameter angegebene eingabeblob fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-133">The input BLOB specified by the *hInputBlob* parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="6a7ff-134">Dieser Fehler kann durch den " **untc:: Connect** "-oder " **untc:: Configure** "-Befehl generiert werden.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-134">This error may be generated by the **IRTC::Connect** or **IRTC::Configure** call.</span></span> <span data-ttu-id="6a7ff-135">Sehen Sie sich den von *herrorblob* zurückgegebenen Fehler-BLOB an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-135">Look at the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="6a7ff-136"><dt>**nmerr- \_ BLOB wurde \_ nicht \_ initialisiert.**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ff-136"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="6a7ff-137">Die Funktion "| **ateblob** " wurde nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-137">The **CreateBlob** function has not been called.</span></span> <span data-ttu-id="6a7ff-138">Dieser Fehler wird durch den " **untc:: Configure** "-Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-138">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="6a7ff-139"><dt>**nmerr- \_ BLOB- \_ Zeichenfolge \_ ungültig**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ff-139"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="6a7ff-140">Die Zeichenfolge wird nicht mit Null beendet.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-140">The string is not null-terminated.</span></span> <span data-ttu-id="6a7ff-141">Dieser Fehler wird durch den " **untc:: Configure** "-Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-141">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="6a7ff-142"><dt>**nmerr-Fehler (unzulässig) \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ff-142"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="6a7ff-143">Der Auslöse Teil des eingabeblobs ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-143">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="6a7ff-144">Dieser Fehler wird durch den " **untc:: Configure** "-Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-144">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                        |
| <dl> <span data-ttu-id="6a7ff-145"><dt>**Ungültiges nmerr- \_ \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ff-145"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="6a7ff-146">Das in *hinputblob* angegebene Objekt ist kein BLOB.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-146">The object specified in *hInputBlob* is not a BLOB.</span></span> <span data-ttu-id="6a7ff-147">Dieser Fehler wird durch den " **untc:: Configure** "-Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-147">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                      |
| <dl> <span data-ttu-id="6a7ff-148"><dt>**nicht genügend Arbeits \_ \_ Speicher für nmerr \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ff-148"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>               | <span data-ttu-id="6a7ff-149">Der zum Ausführen dieses Vorgangs erforderliche Arbeitsspeicher ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-149">The memory needed to perform this operation is unavailable.</span></span> <span data-ttu-id="6a7ff-150">Dieser Fehler wird durch den " **untc:: Configure** "-Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-150">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="6a7ff-151"><dt>**nmerr- \_ Timeout**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ff-151"><dt>**NMERR\_TIMEOUT**</dt></span></span> </dl>                       | <span data-ttu-id="6a7ff-152">Timeout bei der Anforderung. Dieser Fehler wird durch den " **untc:: Configure** "-Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-152">The request has timed out. This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="6a7ff-153"><dt>**nmerr- \_ Uplevel- \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ff-153"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="6a7ff-154">Die in *hinputblob* angegebene Versionsnummer des BLOB ist falsch.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-154">The version number of the BLOB specified in *hInputBlob* is incorrect.</span></span> <span data-ttu-id="6a7ff-155">Dieser Fehler wird durch den " **untc:: Configure** "-Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-155">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="6a7ff-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a7ff-156">Remarks</span></span>

<span data-ttu-id="6a7ff-157">Wenn die **Connect** -Methode aufgerufen wird, ruft der NPP die Methode " **untc:: Configure** " automatisch mithilfe des von *hinputblob* bereitgestellten BLOB auf.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-157">When the **Connect** method is called, the NPP automatically calls the **IRTC::Configure** method by using the BLOB provided by *hInputBlob*.</span></span> <span data-ttu-id="6a7ff-158">Beachten Sie, dass alle Fehlercodes, die vom-Befehl an " **untc:: Configure** " zurückgegeben werden, vom " **untc:: Connect** "-Befehl zurückgegeben und zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="6a7ff-158">Note that any error codes returned by the call to **IRTC::Configure** are passed back and returned by the **IRTC::Connect** call.</span></span>

<span data-ttu-id="6a7ff-159">Diese Methode muss aufgerufen werden, bevor Sie mit dem Erfassen von Frames beginnen können.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-159">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="6a7ff-160">Beachten Sie Folgendes: Wenn Sie mithilfe dieser Methode eine Verbindung mit dem Netzwerk herstellen, müssen Sie weiterhin die Schnittstelle " **iritc** " verwenden, um Frames zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-160">Note that when you connect to the network using this method, you must continue to use the **IRTC** interface to capture frames.</span></span>

<span data-ttu-id="6a7ff-161">Wenn Sie diese Funktion aufrufen, müssen Sie eine Status-oder Frame Rückruffunktion angeben, auch wenn Sie nur als Platzhalter fungiert.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-161">When calling this function, you must specify a status or frame callback function, even if it only acts as a placeholder.</span></span>

<span data-ttu-id="6a7ff-162">Das von *hinputblob* angegebene Eingabe-BLOB kann durch Aufrufen der Methoden **getnppblobfromui**, **getnppblobtable** und **selectnppblobfromtable** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-162">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="6a7ff-163">Das in *herrorblob* zurückgegebene Fehler-BLOB enthält Fehlerinformationen, die der Entwickler oder die Anwendung für die Problembehandlung verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-163">The error BLOB returned in *hErrorBlob* contains error information that the developer or the application can use for troubleshooting.</span></span> <span data-ttu-id="6a7ff-164">Der von *herrorblob* zurückgegebene fehlerblob enthält Einträge, die Netzwerkmonitor in dem in *hinputblob* angegebenen eingabeblob nicht verstehen oder finden konnten.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-164">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="6a7ff-165">Wenn z. b. der nmerr- \_ \_ blobeintrag \_ \_ nicht \_ vorhanden ist, wird der Eintrag Netzwerkmonitor der nicht gefunden wurde, im zurückgegebenen fehlerblob enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6a7ff-165">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="6a7ff-166">Informationen über</span><span class="sxs-lookup"><span data-stu-id="6a7ff-166">For information about</span></span>                          | <span data-ttu-id="6a7ff-167">Finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="6a7ff-167">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="6a7ff-168">Abrufen des eingabeblobs, das eine NIC darstellt</span><span class="sxs-lookup"><span data-stu-id="6a7ff-168">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="6a7ff-169">Auswählen einer Netzwerkschnittstellenkarte</span><span class="sxs-lookup"><span data-stu-id="6a7ff-169">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="6a7ff-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a7ff-170">Requirements</span></span>



| <span data-ttu-id="6a7ff-171">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a7ff-171">Requirement</span></span> | <span data-ttu-id="6a7ff-172">Wert</span><span class="sxs-lookup"><span data-stu-id="6a7ff-172">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a7ff-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a7ff-173">Minimum supported client</span></span><br/> | <span data-ttu-id="6a7ff-174">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a7ff-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="6a7ff-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a7ff-175">Minimum supported server</span></span><br/> | <span data-ttu-id="6a7ff-176">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a7ff-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="6a7ff-177">Header</span><span class="sxs-lookup"><span data-stu-id="6a7ff-177">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a7ff-178"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ff-178"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="6a7ff-179">DLL</span><span class="sxs-lookup"><span data-stu-id="6a7ff-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a7ff-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a7ff-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a7ff-181">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a7ff-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a7ff-182">"Iran"</span><span class="sxs-lookup"><span data-stu-id="6a7ff-182">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="6a7ff-183">"Iran:: Configure"</span><span class="sxs-lookup"><span data-stu-id="6a7ff-183">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="6a7ff-184">:D isconnect</span><span class="sxs-lookup"><span data-stu-id="6a7ff-184">IRTC::Disconnect</span></span>](irtc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="6a7ff-185">"Iran:: Start"</span><span class="sxs-lookup"><span data-stu-id="6a7ff-185">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




