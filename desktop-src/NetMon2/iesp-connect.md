---
description: Mit der Connect-Methode wird die NPP mithilfe einer angegebenen NIC mit dem Netzwerk verbunden, und es werden Konfigurationsinformationen zur Verbindung bereitstellt.
ms.assetid: 48189b2b-9889-4bd8-8972-26005fb7c341
title: 'IESP:: Connect-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 4fc9c88b0eb4671c61f268c5857dceba3dc500f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128329"
---
# <a name="iespconnect-method"></a><span data-ttu-id="c1cea-103">IESP:: Connect-Methode</span><span class="sxs-lookup"><span data-stu-id="c1cea-103">IESP::Connect method</span></span>

<span data-ttu-id="c1cea-104">Mit der **Connect** -Methode wird die NPP mithilfe einer angegebenen NIC mit dem Netzwerk verbunden, und es werden Konfigurationsinformationen zur Verbindung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c1cea-104">The **Connect** method connects the NPP to the network by using a specified NIC and provides configuration information about the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1cea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1cea-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB hInputBlob,
  [in]  DWORD StatusCallbackProc,
  [in]  DWORD UserContext,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="c1cea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1cea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1cea-107">*hinputblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1cea-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cea-108">Handle für das BLOB, das die NIC angibt, mit der der NPP eine Verbindung herstellt, und die Konfigurationsinformationen für diese Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c1cea-108">Handle to the BLOB that specifies the NIC that the NPP connects to and the configuration information for that connection.</span></span>

</dd> <dt>

<span data-ttu-id="c1cea-109">*Status callbackproc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1cea-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cea-110">Adresse der Rückruffunktion des Benutzers, die Statusaktualisierungen (z. b. Trigger) empfängt.</span><span class="sxs-lookup"><span data-stu-id="c1cea-110">Address of the user's callback function, which receives status updates such as triggers.</span></span> <span data-ttu-id="c1cea-111">Wenn eine Rückruffunktion nicht verwendet wird, legen Sie diesen Parameter und den *userContext* -Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="c1cea-111">If a callback function is not used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c1cea-112">*UserContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1cea-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cea-113">Der Wert, der beim Aufrufen der Rückruffunktion des Benutzers erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="c1cea-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="c1cea-114">Der Wert dieses Parameters ist in der Regel entweder HWND oder ein "This"-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="c1cea-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="c1cea-115">Wenn keine Rückruffunktion angegeben ist, legen Sie diesen Parameter und den Parameter " *Status callbackproc* " auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="c1cea-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c1cea-116">*herrorblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c1cea-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cea-117">Handle für ein fehlerblob, das zusätzliche Fehlerinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="c1cea-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1cea-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1cea-118">Return value</span></span>

<span data-ttu-id="c1cea-119">Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c1cea-119">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c1cea-120">Wenn die Methode nicht erfolgreich ist, handelt es sich bei dem Rückgabewert um einen der folgenden Fehlercodes (einschließlich der vom internen **iESP:: Configure** -Befehl zurückgegebenen Fehler):</span><span class="sxs-lookup"><span data-stu-id="c1cea-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IESP::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c1cea-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c1cea-121">Return code</span></span></th>
<th><span data-ttu-id="c1cea-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1cea-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="c1cea-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c1cea-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c1cea-124">Diese Instanz des NPP-com-Objekts ist bereits mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="c1cea-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c1cea-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c1cea-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c1cea-126">Das konfigurationsblob ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="c1cea-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="c1cea-127">Dieser Fehler wird durch den <strong>iESP:: Configure</strong> -Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="c1cea-127">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c1cea-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c1cea-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c1cea-129">Für das vom <em>hinputblob</em> -Parameter angegebene eingabeblob fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c1cea-129">The input BLOB specified by the <em>hInputBlob</em> parameter lacks an entry needed to perform this operation.</span></span> <span data-ttu-id="c1cea-130">Dieser Fehler kann durch den <strong>iESP:: Connect</strong> -oder <strong>iESP:: Configure</strong> -Befehl generiert werden.</span><span class="sxs-lookup"><span data-stu-id="c1cea-130">This error might be generated by the <strong>IESP::Connect</strong> or <strong>IESP::Configure</strong> call.</span></span> <span data-ttu-id="c1cea-131">Sehen Sie sich den von <em>herrorblob</em> zurückgegebenen Fehler-BLOB an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="c1cea-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c1cea-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c1cea-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c1cea-133">Die Funktion "| <strong>ateblob</strong> " wurde nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c1cea-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="c1cea-134">Dieser Fehler wird durch den <strong>iESP:: Configure</strong> -Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="c1cea-134">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c1cea-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c1cea-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c1cea-136">Die Zeichenfolge wird nicht mit Null beendet.</span><span class="sxs-lookup"><span data-stu-id="c1cea-136">The string is not null-terminated.</span></span> <span data-ttu-id="c1cea-137">Dieser Fehler wird durch den <strong>iESP:: Configure</strong> -Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="c1cea-137">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c1cea-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c1cea-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c1cea-139">Der Auslöse Teil des eingabeblobs ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="c1cea-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="c1cea-140">Dieser Fehler wird durch den <strong>iESP:: Configure</strong> -Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="c1cea-140">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c1cea-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c1cea-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c1cea-142">Das in <em>hinputblob</em> angegebene Objekt ist kein BLOB.</span><span class="sxs-lookup"><span data-stu-id="c1cea-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="c1cea-143">Dieser Fehler wird durch den <strong>iESP:: Configure</strong> -Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="c1cea-143">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c1cea-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c1cea-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c1cea-145">Das Standard Erfassungs Verzeichnis wurde nicht in der Registrierung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c1cea-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="c1cea-146">Verwenden Sie den folgenden Pfad, um das Erfassungs Verzeichnis festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c1cea-146">Use the following path to set the capture directory.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c1cea-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c1cea-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c1cea-148">Der zum Ausführen dieses Vorgangs erforderliche Arbeitsspeicher ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c1cea-148">The memory needed to perform this operation is unavailable.</span></span> <span data-ttu-id="c1cea-149">Dieser Fehler wird durch den <strong>iESP:: Configure</strong> -Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="c1cea-149">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="c1cea-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c1cea-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c1cea-151">Timeout bei der Anforderung. Dieser Fehler wird durch den <strong>iESP:: Configure</strong> -Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="c1cea-151">The request has timed out. This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="c1cea-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="c1cea-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="c1cea-153">Die in <em>hinputblob</em> angegebene Versionsnummer des BLOB ist falsch.</span><span class="sxs-lookup"><span data-stu-id="c1cea-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="c1cea-154">Dieser Fehler wird durch den <strong>iESP:: Configure</strong> -Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="c1cea-154">This error is generated by the <strong>IESP::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="c1cea-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1cea-155">Remarks</span></span>

<span data-ttu-id="c1cea-156">Wenn die **Connect** -Methode aufgerufen wird, ruft Netzwerkmonitor automatisch **iESP:: Configure** mithilfe des BLOBs auf, der vom *hinputblob* -Parameter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c1cea-156">When the **Connect** method is called, Network Monitor automatically calls **IESP::Configure** by using the BLOB provided by the *hInputBlob* parameter.</span></span> <span data-ttu-id="c1cea-157">Beachten Sie, dass alle vom iESP:: **configure** -Aufrufe zurückgegebenen Fehlercodes zurückgegeben und vom **iESP:: Connect** -Befehl zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c1cea-157">Note that any error codes returned by the call to **IESP::Configure** are passed back and returned by the **IESP::Connect** call.</span></span>

<span data-ttu-id="c1cea-158">Diese Methode muss aufgerufen werden, bevor Sie mit dem Erfassen von Frames beginnen können.</span><span class="sxs-lookup"><span data-stu-id="c1cea-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="c1cea-159">Beachten Sie Folgendes: Wenn Sie mithilfe dieser Methode eine Verbindung mit dem Netzwerk herstellen, müssen Sie die **iESP** -Schnittstelle weiterhin verwenden, um Frames zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="c1cea-159">Note that when you connect to the network by using this method, you must continue to use the **IESP** interface to capture frames.</span></span>

<span data-ttu-id="c1cea-160">Das von *hinputblob* angegebene eingabeblob kann durch Aufrufen von **getnppblobfromui**, **getnppblobtable** und **selectnppblobfromtable** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c1cea-160">The input BLOB specified by *hInputBlob* can be obtained by calling **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable**.</span></span>

<span data-ttu-id="c1cea-161">Der von *herrorblob* zurückgegebene fehlerblob enthält Einträge, die Netzwerkmonitor in dem in *hinputblob* angegebenen eingabeblob nicht verstehen oder finden konnten.</span><span class="sxs-lookup"><span data-stu-id="c1cea-161">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="c1cea-162">Das zurückgegebene fehlerblob enthält Fehlerinformationen, die von der Anwendung für die Problembehandlung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c1cea-162">The returned error BLOB contains error information that the application can use for troubleshooting.</span></span> <span data-ttu-id="c1cea-163">Wenn z. b. der nmerr- \_ \_ blobeintrag \_ \_ nicht \_ vorhanden ist, wird der Eintrag, den Netzwerkmonitor nicht finden konnte, in das zurückgegebene fehlerblob eingefügt.</span><span class="sxs-lookup"><span data-stu-id="c1cea-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry that Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="c1cea-164">Informationen über</span><span class="sxs-lookup"><span data-stu-id="c1cea-164">For information about</span></span>                          | <span data-ttu-id="c1cea-165">Finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="c1cea-165">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="c1cea-166">Abrufen des eingabeblobs, das eine NIC darstellt</span><span class="sxs-lookup"><span data-stu-id="c1cea-166">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="c1cea-167">Auswählen einer Netzwerkschnittstellenkarte</span><span class="sxs-lookup"><span data-stu-id="c1cea-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="c1cea-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1cea-168">Requirements</span></span>



| <span data-ttu-id="c1cea-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1cea-169">Requirement</span></span> | <span data-ttu-id="c1cea-170">Wert</span><span class="sxs-lookup"><span data-stu-id="c1cea-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1cea-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1cea-171">Minimum supported client</span></span><br/> | <span data-ttu-id="c1cea-172">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1cea-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c1cea-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1cea-173">Minimum supported server</span></span><br/> | <span data-ttu-id="c1cea-174">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1cea-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c1cea-175">Header</span><span class="sxs-lookup"><span data-stu-id="c1cea-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1cea-176"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1cea-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c1cea-177">DLL</span><span class="sxs-lookup"><span data-stu-id="c1cea-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1cea-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1cea-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1cea-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1cea-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1cea-180">IESP</span><span class="sxs-lookup"><span data-stu-id="c1cea-180">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="c1cea-181">IESP:: Configure</span><span class="sxs-lookup"><span data-stu-id="c1cea-181">IESP::Configure</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="c1cea-182">IESP::D isconnect</span><span class="sxs-lookup"><span data-stu-id="c1cea-182">IESP::Disconnect</span></span>](iesp-disconnect.md)
</dt> <dt>

[<span data-ttu-id="c1cea-183">IESP:: Start</span><span class="sxs-lookup"><span data-stu-id="c1cea-183">IESP::Start</span></span>](iesp-start.md)
</dt> </dl>

 

 




