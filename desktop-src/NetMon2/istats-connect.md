---
description: 'IStats::Connect-Methode: Die Connect-Methode verbindet den NPP mithilfe einer angegebenen NIC mit dem Netzwerk und stellt Konfigurationsinformationen für die Verbindung zur Verfügung.'
ms.assetid: 29a12df7-9c81-40ff-ac12-33ce1de833b1
title: IStats::Connect-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0719b6ff56aaa8c0be02f86d62ac23d4003aa3d6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098478"
---
# <a name="istatsconnect-method"></a><span data-ttu-id="8df43-103">IStats::Connect-Methode</span><span class="sxs-lookup"><span data-stu-id="8df43-103">IStats::Connect method</span></span>

<span data-ttu-id="8df43-104">Die **Connect-Methode** verbindet den NPP mithilfe einer angegebenen NIC mit dem Netzwerk und stellt Konfigurationsinformationen für die Verbindung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="8df43-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8df43-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8df43-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="8df43-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8df43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8df43-107">*hInputBlob* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8df43-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df43-108">Handle für das BLOB, das die NIC angibt, mit der das NPP eine Verbindung herstellt, und die Konfigurationsinformationen für diese Verbindung angibt.</span><span class="sxs-lookup"><span data-stu-id="8df43-108">Handle to the BLOB that specifies the NIC that the NPP connects to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="8df43-109">*StatusCallbackProc* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8df43-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df43-110">Adresse der Rückruffunktion des Benutzers, die Statusaktualisierungen wie Trigger empfängt.</span><span class="sxs-lookup"><span data-stu-id="8df43-110">Address of the user's callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="8df43-111">Wenn keine Rückruffunktion verwendet wird, legen Sie diesen Parameter und den *UserContext-Parameter* auf **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="8df43-111">If a callback function is not used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8df43-112">*UserContext* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8df43-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df43-113">Wert, der übergeben wird, wenn die Rückruffunktion des Benutzers aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8df43-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="8df43-114">Der Wert dieses Parameters ist in der Regel entweder HWND oder ein This-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="8df43-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="8df43-115">Wenn keine Rückruffunktion angegeben wird, legen Sie diesen Parameter und den *StatusCallbackProc-Parameter* auf **NULL fest.**</span><span class="sxs-lookup"><span data-stu-id="8df43-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8df43-116">*hErrorBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8df43-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8df43-117">Handle für ein Fehlerblob, das zusätzliche Fehlerinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="8df43-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8df43-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8df43-118">Return value</span></span>

<span data-ttu-id="8df43-119">Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="8df43-119">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="8df43-120">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes (einschließlich der Fehler, die vom internen **IStats::Configure-Aufruf zurückgegeben** werden):</span><span class="sxs-lookup"><span data-stu-id="8df43-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IStats::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8df43-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="8df43-121">Return code</span></span></th>
<th><span data-ttu-id="8df43-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8df43-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="8df43-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8df43-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8df43-124">Diese Instanz des NPP-COM-Objekts ist bereits mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="8df43-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="8df43-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8df43-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8df43-126">Das Konfigurations-BLOB ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="8df43-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="8df43-127">Dieser Fehler wird durch den <strong>IStats::Configure-Aufruf</strong> generiert.</span><span class="sxs-lookup"><span data-stu-id="8df43-127">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="8df43-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8df43-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8df43-129">Dem durch den <em>hInputBlob-Parameter</em> angegebenen Eingabeblob fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8df43-129">The input BLOB specified by the <em>hInputBlob</em> parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="8df43-130">Dieser Fehler kann durch den <strong>Aufruf IStats::Connect</strong> oder <strong>IStats::Configure</strong> generiert werden.</span><span class="sxs-lookup"><span data-stu-id="8df43-130">This error might be generated by the <strong>IStats::Connect</strong> or <strong>IStats::Configure</strong> call.</span></span> <span data-ttu-id="8df43-131">Sehen Sie sich den von <em>hErrorBlob</em> zurückgegebenen Fehler-BLOB an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="8df43-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="8df43-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8df43-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8df43-133">Die <strong>CreateBlob-Funktion</strong> wurde nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8df43-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="8df43-134">Dieser Fehler wird durch den <strong>IStats::Configure-Aufruf</strong> generiert.</span><span class="sxs-lookup"><span data-stu-id="8df43-134">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="8df43-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8df43-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8df43-136">Die Zeichenfolge ist nicht NULL-terminiert.</span><span class="sxs-lookup"><span data-stu-id="8df43-136">The string is not null-terminated.</span></span> <span data-ttu-id="8df43-137">Dieser Fehler wird durch den <strong>IStats::Configure-Aufruf</strong> generiert.</span><span class="sxs-lookup"><span data-stu-id="8df43-137">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="8df43-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8df43-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8df43-139">Der Triggerteil des Eingabeblobs ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="8df43-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="8df43-140">Dieser Fehler wird durch den <strong>IStats::Configure-Aufruf</strong> generiert.</span><span class="sxs-lookup"><span data-stu-id="8df43-140">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="8df43-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8df43-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8df43-142">Das in <em>hInputBlob</em> angegebene Objekt ist kein BLOB.</span><span class="sxs-lookup"><span data-stu-id="8df43-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="8df43-143">Dieser Fehler wird durch den <strong>IStats::Configure-Aufruf</strong> generiert.</span><span class="sxs-lookup"><span data-stu-id="8df43-143">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="8df43-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8df43-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8df43-145">Das Standarderfassungsverzeichnis wurde in der Registrierung nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8df43-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="8df43-146">Verwenden Sie zum Festlegen des Erfassungsverzeichnisses den folgenden Pfad.</span><span class="sxs-lookup"><span data-stu-id="8df43-146">To set the capture directory, use the following path.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="8df43-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8df43-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8df43-148">Der zum Ausführen dieses Vorgangs erforderliche Arbeitsspeicher war nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8df43-148">The memory required to perform this operation was unavailable.</span></span> <span data-ttu-id="8df43-149">Dieser Fehler wird durch den <strong>Aufruf IStats::Configure</strong> generiert.</span><span class="sxs-lookup"><span data-stu-id="8df43-149">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="8df43-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8df43-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8df43-151">Für die Anforderung ist ein Time out erfolgt. Dieser Fehler wird durch den <strong>Aufruf IStats::Configure</strong> generiert.</span><span class="sxs-lookup"><span data-stu-id="8df43-151">The request has timed out. This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="8df43-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="8df43-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="8df43-153">Die In <em>hInputBlob</em> angegebene Versionsnummer des BLOB ist falsch.</span><span class="sxs-lookup"><span data-stu-id="8df43-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="8df43-154">Dieser Fehler wird durch den <strong>Aufruf IStats::Configure</strong> generiert.</span><span class="sxs-lookup"><span data-stu-id="8df43-154">This error is generated by the <strong>IStats::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="8df43-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8df43-155">Remarks</span></span>

<span data-ttu-id="8df43-156">Wenn die **Connect-Methode** aufgerufen wird, ruft Netzwerkmonitor **die IStats::Configure-Methode** automatisch auf, indem das vom *hInputBlob-Parameter* bereitgestellte BLOB verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8df43-156">When the **Connect** method is called, Network Monitor automatically calls the **IStats::Configure** method by using the BLOB provided by the *hInputBlob* parameter.</span></span> <span data-ttu-id="8df43-157">Beachten Sie, dass alle Fehlercodes, die durch den Aufruf von **IStats::Configure** zurückgegeben werden, zurückgegeben und vom **IStats::Connect-Aufruf zurückgegeben** werden.</span><span class="sxs-lookup"><span data-stu-id="8df43-157">Note that any error codes returned by the call to **IStats::Configure** are passed back and returned by the **IStats::Connect** call.</span></span>

<span data-ttu-id="8df43-158">Diese Methode muss aufgerufen werden, bevor Sie mit dem Erfassen von Frames beginnen können.</span><span class="sxs-lookup"><span data-stu-id="8df43-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="8df43-159">Beachten Sie, dass Sie beim Herstellen einer Verbindung mit dem Netzwerk mit dieser Methode weiterhin die **IStats-Schnittstelle** verwenden müssen, um Frames zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="8df43-159">Note that when you connect to the network by using this method, you must continue to use the **IStats** interface to capture frames.</span></span>

<span data-ttu-id="8df43-160">Das von *hInputBlob* angegebene EingabeBLOB kann durch Aufrufen der **Methoden GetNPPBlobFromUI,** **GetNPPBlobTable** und **SelectNPPBlobFromTable** ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="8df43-160">The input BLOB specified by *hInputBlob* can be obtained by calling the **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable** methods.</span></span>

<span data-ttu-id="8df43-161">Das vom *hErrorBlob-Parameter* zurückgegebene FehlerBLOB enthält Einträge, die Netzwerkmonitor in dem in *hInputBlob* angegebenen EingabeBLOB nicht verstehen oder finden konnten.</span><span class="sxs-lookup"><span data-stu-id="8df43-161">The error BLOB returned by the *hErrorBlob* parameter contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="8df43-162">Das zurückgegebene Fehlerblob enthält Fehlerinformationen, die die Anwendung für die Problembehandlung verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="8df43-162">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="8df43-163">Wenn beispielsweise NMERR BLOB ENTRY DOES NOT EXIST zurückgegeben wird, wird der Eintrag, den Netzwerkmonitor nicht finden konnte, \_ \_ in das zurückgegebene \_ \_ FehlerBLOB \_ eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8df43-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry that Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="8df43-164">Informationen über</span><span class="sxs-lookup"><span data-stu-id="8df43-164">For information about</span></span>                                             | <span data-ttu-id="8df43-165">Finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="8df43-165">See</span></span>                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="8df43-166">Abrufen des Eingabeblobs, das eine Netzwerkschnittstellenkarte darstellt</span><span class="sxs-lookup"><span data-stu-id="8df43-166">Obtaining the input BLOB that represents a network interface card</span></span> | [<span data-ttu-id="8df43-167">Auswählen einer Netzwerkschnittstellenkarte</span><span class="sxs-lookup"><span data-stu-id="8df43-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="8df43-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8df43-168">Requirements</span></span>



| <span data-ttu-id="8df43-169">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8df43-169">Requirement</span></span> | <span data-ttu-id="8df43-170">Wert</span><span class="sxs-lookup"><span data-stu-id="8df43-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8df43-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8df43-171">Minimum supported client</span></span><br/> | <span data-ttu-id="8df43-172">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8df43-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="8df43-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8df43-173">Minimum supported server</span></span><br/> | <span data-ttu-id="8df43-174">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8df43-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="8df43-175">Header</span><span class="sxs-lookup"><span data-stu-id="8df43-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="8df43-176"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="8df43-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="8df43-177">DLL</span><span class="sxs-lookup"><span data-stu-id="8df43-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8df43-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8df43-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8df43-179">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8df43-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8df43-180">IStats</span><span class="sxs-lookup"><span data-stu-id="8df43-180">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="8df43-181">IStats::Configure</span><span class="sxs-lookup"><span data-stu-id="8df43-181">IStats::Configure</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="8df43-182">IStats::D isconnect</span><span class="sxs-lookup"><span data-stu-id="8df43-182">IStats::Disconnect</span></span>](istats-disconnect.md)
</dt> <dt>

[<span data-ttu-id="8df43-183">Netzwerkmonitor BLOBS</span><span class="sxs-lookup"><span data-stu-id="8df43-183">Network Monitor BLOBS</span></span>](network-monitor-blobs.md)
</dt> </dl>

 

 




