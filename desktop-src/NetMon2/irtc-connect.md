---
description: 'IRTC::Connect-Methode: Die Connect-Methode verbindet das NPP mithilfe einer angegebenen NIC mit dem Netzwerk und stellt Konfigurationsinformationen für die Verbindung zur Verfügung.'
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: IRTC::Connect-Methode (Netmon.h)
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
ms.openlocfilehash: ba62f3341b18ddfdbf09af4eec701322d901ab79
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110744"
---
# <a name="irtcconnect-method"></a><span data-ttu-id="aa5d1-103">IRTC::Connect-Methode</span><span class="sxs-lookup"><span data-stu-id="aa5d1-103">IRTC::Connect method</span></span>

<span data-ttu-id="aa5d1-104">Die **Connect-Methode** verbindet den NPP mithilfe einer angegebenen NIC mit dem Netzwerk und stellt Konfigurationsinformationen für die Verbindung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa5d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa5d1-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID FramesCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="aa5d1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa5d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa5d1-107">*hInputBlob* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="aa5d1-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa5d1-108">Handle für das BLOB, das die NIC angibt, mit der Sie eine Verbindung herstellen, und die Konfigurationsinformationen für diese Verbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-108">Handle to the BLOB that specifies the NIC that you are connecting to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="aa5d1-109">*StatusCallbackProc* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="aa5d1-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa5d1-110">Adresse der Statusrückruffunktion des Benutzers, die Statusupdates wie Trigger empfängt.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-110">Address of the user's status callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="aa5d1-111">Dieser Parameter kann auf NULL **festgelegt werden.**</span><span class="sxs-lookup"><span data-stu-id="aa5d1-111">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aa5d1-112">*FramesCallbackProc* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="aa5d1-112">*FramesCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa5d1-113">Adresse der Framerückruffunktion des Benutzers, die zum Empfangen von Statusupdates wie Triggern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-113">Address of the user's frame callback function, which is used to receive status updates such as triggers.</span></span> <span data-ttu-id="aa5d1-114">Dieser Parameter kann auf NULL **festgelegt werden.**</span><span class="sxs-lookup"><span data-stu-id="aa5d1-114">This parameter can be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="aa5d1-115">*UserContext* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="aa5d1-115">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa5d1-116">Der Wert wird übergeben, wenn der Status und die Framerückruffunktion des Benutzers aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-116">Value passed when the user's status and frame callback function is called.</span></span> <span data-ttu-id="aa5d1-117">Wenn beide Rückruffunktionen angegeben werden, müssen sie denselben Benutzerkontextwert verwenden.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-117">If both callback functions are specified, they must use the same user-context value.</span></span> <span data-ttu-id="aa5d1-118">Der Wert dieses Parameters ist in der Regel entweder HWND oder ein This-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-118">The value of this parameter is typically either HWND or a 'this' pointer.</span></span>

</dd> <dt>

<span data-ttu-id="aa5d1-119">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="aa5d1-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aa5d1-120">Handle für ein Fehlerblob, das zusätzliche Fehlerinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-120">Handle to an error BLOB that contains additional error information.</span></span> <span data-ttu-id="aa5d1-121">Informationen dazu, was im Fehlerblob enthalten ist, finden Sie unter Hinweise am Ende dieses Themas.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-121">See Remarks at the bottom of this topic for information about what is in the error BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa5d1-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa5d1-122">Return value</span></span>

<span data-ttu-id="aa5d1-123">Wenn diese Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-123">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="aa5d1-124">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes (einschließlich der Fehler, die vom internen **IRTC::Configure-Aufruf** zurückgegeben werden):</span><span class="sxs-lookup"><span data-stu-id="aa5d1-124">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IRTC::Configure** call):</span></span>



| <span data-ttu-id="aa5d1-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="aa5d1-125">Return code</span></span>                                                                                                         | <span data-ttu-id="aa5d1-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa5d1-126">Description</span></span>                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aa5d1-127"><dt>**NMERR \_ BEREITS \_ VERBUNDEN**</dt></span><span class="sxs-lookup"><span data-stu-id="aa5d1-127"><dt>**NMERR\_ALREADY\_CONNECTED**</dt></span></span> </dl>            | <span data-ttu-id="aa5d1-128">Diese Instanz des NPP-COM-Objekts ist bereits mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-128">This instance of the NPP COM object is already connected to the network.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="aa5d1-129"><dt>**\_ \_ NMERR-BLOBKONVERTIERUNGSFEHLER \_**</dt></span><span class="sxs-lookup"><span data-stu-id="aa5d1-129"><dt>**NMERR\_BLOB\_CONVERSION\_ERROR**</dt></span></span> </dl>       | <span data-ttu-id="aa5d1-130">Das Konfigurations-BLOB ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-130">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="aa5d1-131">Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-131">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="aa5d1-132"><dt>**NMERR \_ BLOB ENTRY DOES NOT EXIST (NMERR-BLOBEINTRAG IST NICHT \_ \_ \_ \_ VORHANDEN)**</dt></span><span class="sxs-lookup"><span data-stu-id="aa5d1-132"><dt>**NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST**</dt></span></span> </dl> | <span data-ttu-id="aa5d1-133">Dem durch den *hInputBlob-Parameter* angegebenen Eingabeblob fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-133">The input BLOB specified by the *hInputBlob* parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="aa5d1-134">Dieser Fehler kann durch den **IRTC::Connect-** oder **IRTC::Configure-Aufruf** generiert werden.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-134">This error may be generated by the **IRTC::Connect** or **IRTC::Configure** call.</span></span> <span data-ttu-id="aa5d1-135">Sehen Sie sich den von *hErrorBlob* zurückgegebenen Fehler-BLOB an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-135">Look at the error BLOB returned by *hErrorBlob* to determine which entry was not found.</span></span><br/> |
| <dl> <span data-ttu-id="aa5d1-136"><dt>**\_NMERR-BLOB \_ NICHT \_ INITIALISIERT**</dt></span><span class="sxs-lookup"><span data-stu-id="aa5d1-136"><dt>**NMERR\_BLOB\_NOT\_INITIALIZED**</dt></span></span> </dl>        | <span data-ttu-id="aa5d1-137">Die **CreateBlob-Funktion** wurde nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-137">The **CreateBlob** function has not been called.</span></span> <span data-ttu-id="aa5d1-138">Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-138">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="aa5d1-139"><dt>**NMERR \_ BLOB \_ STRING \_ INVALID**</dt></span><span class="sxs-lookup"><span data-stu-id="aa5d1-139"><dt>**NMERR\_BLOB\_STRING\_INVALID**</dt></span></span> </dl>         | <span data-ttu-id="aa5d1-140">Die Zeichenfolge ist nicht NULL-terminiert.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-140">The string is not null-terminated.</span></span> <span data-ttu-id="aa5d1-141">Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-141">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                       |
| <dl> <span data-ttu-id="aa5d1-142"><dt>**NMERR \_ ILLEGAL \_ TRIGGER**</dt></span><span class="sxs-lookup"><span data-stu-id="aa5d1-142"><dt>**NMERR\_ILLEGAL\_TRIGGER**</dt></span></span> </dl>              | <span data-ttu-id="aa5d1-143">Der Triggerteil des Eingabeblobs ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-143">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="aa5d1-144">Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-144">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                        |
| <dl> <span data-ttu-id="aa5d1-145"><dt>**NMERR \_ UNGÜLTIGES \_ BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="aa5d1-145"><dt>**NMERR\_INVALID\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="aa5d1-146">Das in *hInputBlob* angegebene Objekt ist kein BLOB.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-146">The object specified in *hInputBlob* is not a BLOB.</span></span> <span data-ttu-id="aa5d1-147">Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-147">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                      |
| <dl> <span data-ttu-id="aa5d1-148"><dt>**NMERR \_ NICHT \_ GENÜGEND \_ ARBEITSSPEICHER**</dt></span><span class="sxs-lookup"><span data-stu-id="aa5d1-148"><dt>**NMERR\_OUT\_OF\_MEMORY**</dt></span></span> </dl>               | <span data-ttu-id="aa5d1-149">Der zum Ausführen dieses Vorgangs erforderliche Arbeitsspeicher ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-149">The memory needed to perform this operation is unavailable.</span></span> <span data-ttu-id="aa5d1-150">Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-150">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="aa5d1-151"><dt>**NMERR \_ TIMEOUT**</dt></span><span class="sxs-lookup"><span data-stu-id="aa5d1-151"><dt>**NMERR\_TIMEOUT**</dt></span></span> </dl>                       | <span data-ttu-id="aa5d1-152">Für die Anforderung ist ein Time out aufgetreten. Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-152">The request has timed out. This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="aa5d1-153"><dt>**\_ \_ NMERR-UPLEVEL-BLOB**</dt></span><span class="sxs-lookup"><span data-stu-id="aa5d1-153"><dt>**NMERR\_UPLEVEL\_BLOB**</dt></span></span> </dl>                 | <span data-ttu-id="aa5d1-154">Die In *hInputBlob* angegebene Versionsnummer des BLOB ist falsch.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-154">The version number of the BLOB specified in *hInputBlob* is incorrect.</span></span> <span data-ttu-id="aa5d1-155">Dieser Fehler wird durch den **IRTC::Configure-Aufruf** generiert.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-155">This error is generated by the **IRTC::Configure** call.</span></span><br/>                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="aa5d1-156">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa5d1-156">Remarks</span></span>

<span data-ttu-id="aa5d1-157">Wenn die **Connect-Methode** aufgerufen wird, ruft das NPP automatisch die **IRTC::Configure-Methode** auf, indem das von *hInputBlob* bereitgestellte BLOB verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-157">When the **Connect** method is called, the NPP automatically calls the **IRTC::Configure** method by using the BLOB provided by *hInputBlob*.</span></span> <span data-ttu-id="aa5d1-158">Beachten Sie, dass alle Fehlercodes, die vom Aufruf von **IRTC::Configure** zurückgegeben werden, zurückgegeben und vom **IRTC::Connect-Aufruf** zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-158">Note that any error codes returned by the call to **IRTC::Configure** are passed back and returned by the **IRTC::Connect** call.</span></span>

<span data-ttu-id="aa5d1-159">Diese Methode muss aufgerufen werden, bevor Sie mit der Erfassung von Frames beginnen können.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-159">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="aa5d1-160">Beachten Sie Folgendes: Wenn Sie mit dieser Methode eine Verbindung mit dem Netzwerk herstellen, müssen Sie weiterhin die **IRTC-Schnittstelle** verwenden, um Frames zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-160">Note that when you connect to the network using this method, you must continue to use the **IRTC** interface to capture frames.</span></span>

<span data-ttu-id="aa5d1-161">Beim Aufrufen dieser Funktion müssen Sie einen Status oder eine Framerückruffunktion angeben, auch wenn sie nur als Platzhalter fungiert.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-161">When calling this function, you must specify a status or frame callback function, even if it only acts as a placeholder.</span></span>

<span data-ttu-id="aa5d1-162">Das von *hInputBlob* angegebene Eingabeblob kann durch Aufrufen der Methoden **GetNPPBlobFromUI,** **GetNPPBlobTable** und **SelectNPPBlobFromTable** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-162">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="aa5d1-163">Das in *hErrorBlob* zurückgegebene Fehlerblob enthält Fehlerinformationen, die der Entwickler oder die Anwendung für die Problembehandlung verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-163">The error BLOB returned in *hErrorBlob* contains error information that the developer or the application can use for troubleshooting.</span></span> <span data-ttu-id="aa5d1-164">Das von *hErrorBlob* zurückgegebene Fehlerblob enthält Einträge, die Netzwerkmonitor nicht verstehen oder im Eingabe-BLOB finden konnten, das in *hInputBlob* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-164">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="aa5d1-165">Wenn z. B. NMERR \_ BLOB ENTRY DOES NOT EXIST zurückgegeben \_ \_ \_ \_ wird, ist der Eintrag, den Netzwerkmonitor nicht finden konnte, im zurückgegebenen Fehlerblob enthalten.</span><span class="sxs-lookup"><span data-stu-id="aa5d1-165">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="aa5d1-166">Informationen über</span><span class="sxs-lookup"><span data-stu-id="aa5d1-166">For information about</span></span>                          | <span data-ttu-id="aa5d1-167">Finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="aa5d1-167">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="aa5d1-168">Abrufen des Eingabeblobs, das eine NIC darstellt</span><span class="sxs-lookup"><span data-stu-id="aa5d1-168">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="aa5d1-169">Auswählen einer Netzwerkschnittstellenkarte</span><span class="sxs-lookup"><span data-stu-id="aa5d1-169">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="aa5d1-170">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa5d1-170">Requirements</span></span>



| <span data-ttu-id="aa5d1-171">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa5d1-171">Requirement</span></span> | <span data-ttu-id="aa5d1-172">Wert</span><span class="sxs-lookup"><span data-stu-id="aa5d1-172">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa5d1-173">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aa5d1-173">Minimum supported client</span></span><br/> | <span data-ttu-id="aa5d1-174">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa5d1-174">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="aa5d1-175">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aa5d1-175">Minimum supported server</span></span><br/> | <span data-ttu-id="aa5d1-176">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aa5d1-176">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="aa5d1-177">Header</span><span class="sxs-lookup"><span data-stu-id="aa5d1-177">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa5d1-178"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="aa5d1-178"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="aa5d1-179">DLL</span><span class="sxs-lookup"><span data-stu-id="aa5d1-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa5d1-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa5d1-180"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa5d1-181">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="aa5d1-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa5d1-182">IRTC</span><span class="sxs-lookup"><span data-stu-id="aa5d1-182">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="aa5d1-183">IRTC::Configure</span><span class="sxs-lookup"><span data-stu-id="aa5d1-183">IRTC::Configure</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="aa5d1-184">IRTC::D isconnect</span><span class="sxs-lookup"><span data-stu-id="aa5d1-184">IRTC::Disconnect</span></span>](irtc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="aa5d1-185">IRTC::Start</span><span class="sxs-lookup"><span data-stu-id="aa5d1-185">IRTC::Start</span></span>](irtc-start.md)
</dt> </dl>

 

 




