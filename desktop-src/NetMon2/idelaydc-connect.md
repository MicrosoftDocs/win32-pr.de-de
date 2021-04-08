---
description: Mit der Connect-Methode wird die NPP über eine angegebene Netzwerkschnittstellenkarte mit dem Netzwerk verbunden, und es werden Konfigurationsinformationen zur Verbindung bereitstellt.
ms.assetid: aae9ff9c-d077-4db2-a900-9916e4f7bb8b
title: 'Idelta-DC:: Connect-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b2cd1fb5ad694493c4a225aa3bf109d7775b9dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861999"
---
# <a name="idelaydcconnect-method"></a><span data-ttu-id="50931-103">Idelta aydc:: Connect-Methode</span><span class="sxs-lookup"><span data-stu-id="50931-103">IDelaydC::Connect method</span></span>

<span data-ttu-id="50931-104">Mit der **Connect** -Methode wird die NPP über eine angegebene Netzwerkschnittstellenkarte mit dem Netzwerk verbunden, und es werden Konfigurationsinformationen zur Verbindung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="50931-104">The **Connect** method connects the NPP to the network by using a specified network interface card and provides configuration information about the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="50931-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50931-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="50931-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50931-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50931-107">*hinputblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50931-107">*hInputBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50931-108">Handle für das BLOB, das die NIC angibt, mit der Sie eine Verbindung herstellen, und die Konfigurationsinformationen über diese Verbindung.</span><span class="sxs-lookup"><span data-stu-id="50931-108">Handle to the BLOB that specifies the NIC that you are connecting to and the configuration information about that connection.</span></span>

</dd> <dt>

<span data-ttu-id="50931-109">*Status callbackproc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50931-109">*StatusCallbackProc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50931-110">Adresse der Rückruffunktion des Benutzers, die zum Empfangen von Statusaktualisierungen (z. b. Trigger) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="50931-110">Address of the user's callback function, which is used to receive status updates such as triggers.</span></span> <span data-ttu-id="50931-111">Wenn keine Rückruffunktion verwendet wird, legen Sie diesen Parameter und den *userContext* -Parameter auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="50931-111">If no callback function is used, set this parameter and the *UserContext* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="50931-112">*UserContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50931-112">*UserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50931-113">Der Wert, der beim Aufrufen der Rückruffunktion des Benutzers erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="50931-113">Value passed when the user's callback function is called.</span></span> <span data-ttu-id="50931-114">Der Wert dieses Parameters ist in der Regel entweder HWND oder ein "This"-Zeiger.</span><span class="sxs-lookup"><span data-stu-id="50931-114">The value of this parameter is typically either HWND or a 'this' pointer.</span></span> <span data-ttu-id="50931-115">Wenn keine Rückruffunktion angegeben ist, legen Sie diesen Parameter und den Parameter " *Status callbackproc* " auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="50931-115">If a callback function is not specified, set this parameter and the *StatusCallbackProc* parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="50931-116">*herrorblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="50931-116">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50931-117">Handle für ein fehlerblob, das zusätzliche Fehlerinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="50931-117">Handle to an error BLOB that contains additional error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50931-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50931-118">Return value</span></span>

<span data-ttu-id="50931-119">Wenn diese Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="50931-119">If this method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="50931-120">Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes (einschließlich der Fehler, die vom internen **idelta-DC:: Configure** -Befehl zurückgegeben werden):</span><span class="sxs-lookup"><span data-stu-id="50931-120">If the method is unsuccessful, the return value is one of the following error codes (which include those errors returned by the internal **IDelaydC::Configure** call):</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="50931-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="50931-121">Return code</span></span></th>
<th><span data-ttu-id="50931-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="50931-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="50931-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="50931-123"><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="50931-124">Diese Instanz des NPP-com-Objekts ist bereits mit dem Netzwerk verbunden.</span><span class="sxs-lookup"><span data-stu-id="50931-124">This instance of the NPP COM object is already connected to the network.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="50931-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="50931-125"><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="50931-126">Das konfigurationsblob ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="50931-126">The configuration BLOB is corrupt.</span></span> <span data-ttu-id="50931-127">Dieser Fehler wird durch den <strong>idelta aydc:: Configure</strong> -Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="50931-127">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="50931-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="50931-128"><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="50931-129">Für das von <em>hinputblob</em> angegebene eingabeblob fehlt ein Eintrag, der zum Ausführen dieses Vorgangs erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="50931-129">The input BLOB specified by <em>hInputBlob</em> is missing an entry needed to perform this operation.</span></span> <span data-ttu-id="50931-130">Dieser Fehler kann vom <strong>idelta-DC:: Connect</strong> -oder <strong>idelta-DC:: Configure</strong> -Befehl generiert werden.</span><span class="sxs-lookup"><span data-stu-id="50931-130">This error may be generated by the <strong>IDelaydC::Connect</strong> or <strong>IDelaydC::Configure</strong> call.</span></span> <span data-ttu-id="50931-131">Sehen Sie sich den von <em>herrorblob</em> zurückgegebenen Fehler-BLOB an, um zu ermitteln, welcher Eintrag nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="50931-131">Look at the error BLOB returned by <em>hErrorBlob</em> to determine which entry was not found.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="50931-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="50931-132"><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="50931-133">Die Funktion "| <strong>ateblob</strong> " wurde nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="50931-133">The <strong>CreateBlob</strong> function has not been called.</span></span> <span data-ttu-id="50931-134">Dieser Fehler wird durch den <strong>idelta aydc:: Configure</strong> -Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="50931-134">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="50931-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="50931-135"><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="50931-136">Die Zeichenfolge wird nicht mit Null beendet.</span><span class="sxs-lookup"><span data-stu-id="50931-136">The string is not null-terminated.</span></span> <span data-ttu-id="50931-137">Dieser Fehler wird durch den <strong>idelta aydc:: Configure</strong> -Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="50931-137">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="50931-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="50931-138"><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="50931-139">Der Auslöse Teil des eingabeblobs ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="50931-139">The trigger portion of the input BLOB is corrupt.</span></span> <span data-ttu-id="50931-140">Dieser Fehler wird durch den <strong>idelta aydc:: Configure</strong> -Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="50931-140">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="50931-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="50931-141"><dt><strong>NMERR_INVALID_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="50931-142">Das in <em>hinputblob</em> angegebene Objekt ist kein BLOB.</span><span class="sxs-lookup"><span data-stu-id="50931-142">The object specified in <em>hInputBlob</em> is not a BLOB.</span></span> <span data-ttu-id="50931-143">Dieser Fehler wird durch den <strong>idelta aydc:: Configure</strong> -Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="50931-143">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="50931-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="50931-144"><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="50931-145">Das Standard Erfassungs Verzeichnis wurde nicht in der Registrierung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="50931-145">The default capture directory was not set in the registry.</span></span> <span data-ttu-id="50931-146">Verwenden Sie den folgenden Pfad, um das Erfassungs Verzeichnis festzulegen.</span><span class="sxs-lookup"><span data-stu-id="50931-146">Use the following path to set the capture directory.</span></span> <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="50931-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="50931-147"><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="50931-148">Es war kein Arbeitsspeicher verfügbar, um diesen Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="50931-148">No memory was available to perform this operation.</span></span> <span data-ttu-id="50931-149">Dieser Fehler wird durch den <strong>idelta aydc:: Configure</strong> -Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="50931-149">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="50931-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="50931-150"><dt><strong>NMERR_TIMEOUT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="50931-151">Timeout bei der Anforderung. Dieser Fehler wird durch den <strong>idelta aydc:: Configure</strong> -Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="50931-151">The request has timed out. This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="50931-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="50931-152"><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="50931-153">Die in <em>hinputblob</em> angegebene Versionsnummer des BLOB ist falsch.</span><span class="sxs-lookup"><span data-stu-id="50931-153">The version number of the BLOB specified in <em>hInputBlob</em> is incorrect.</span></span> <span data-ttu-id="50931-154">Dieser Fehler wird durch den <strong>idelta aydc:: Configure</strong> -Befehl generiert.</span><span class="sxs-lookup"><span data-stu-id="50931-154">This error is generated by the <strong>IDelaydC::Configure</strong> call.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="50931-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="50931-155">Remarks</span></span>

<span data-ttu-id="50931-156">Wenn die **Connect** -Methode aufgerufen wird, ruft der NPP automatisch **idelta-DC:: Configure** mithilfe des BLOBs auf, das von *hinputblob* bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="50931-156">When the **Connect** method is called, the NPP automatically calls **IDelaydC::Configure** by using the BLOB provided by *hInputBlob*.</span></span> <span data-ttu-id="50931-157">Beachten Sie, dass alle Fehlercodes, die vom idelta- **DC:: Configure** -Befehl zurückgegeben werden, zurückgegeben und vom **idelta-DC:: Connect** -Befehl zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="50931-157">Note that any error codes returned by the call to **IDelaydC::Configure** are passed back and returned by the **IDelaydC::Connect** call.</span></span>

<span data-ttu-id="50931-158">Diese Methode muss aufgerufen werden, bevor Sie mit dem Erfassen von Frames beginnen können.</span><span class="sxs-lookup"><span data-stu-id="50931-158">This method must be called before you can start capturing frames.</span></span> <span data-ttu-id="50931-159">Beachten Sie Folgendes: Wenn Sie mithilfe dieser Methode eine Verbindung mit dem Netzwerk herstellen, müssen Sie die **idelta-DC** -Schnittstellen Methoden weiterhin verwenden, um Frames zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="50931-159">Note that when you connect to the network by using this method, you must continue to use the **IDelaydC** interface methods to capture frames.</span></span>

<span data-ttu-id="50931-160">Der durch den *hinputblob* -Parameter angegebene eingabeblob kann durch Aufrufen von **getnppblobfromui**, **getnppblobtable** und **selectnppblobfromtable** abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="50931-160">The input BLOB specified by the *hInputBlob* parameter can be obtained by calling **GetNPPBlobFromUI**, **GetNPPBlobTable**, and **SelectNPPBlobFromTable**.</span></span>

<span data-ttu-id="50931-161">Das in *herrorblob* zurückgegebene Fehler-BLOB enthält Fehlerinformationen, die der Entwickler oder die Anwendung für die Problembehandlung verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="50931-161">The error BLOB returned in *hErrorBlob* contains error information that the developer or the application can use for troubleshooting.</span></span> <span data-ttu-id="50931-162">Der von *herrorblob* zurückgegebene fehlerblob enthält Einträge, die Netzwerkmonitor in dem in *hinputblob* angegebenen eingabeblob nicht verstehen oder finden konnten.</span><span class="sxs-lookup"><span data-stu-id="50931-162">The error BLOB returned by *hErrorBlob* contains entries that Network Monitor could not understand or find in the input BLOB specified in *hInputBlob*.</span></span> <span data-ttu-id="50931-163">Wenn z. b. der nmerr- \_ \_ blobeintrag \_ \_ nicht \_ vorhanden ist, wird der Eintrag Netzwerkmonitor der nicht gefunden wurde, im zurückgegebenen fehlerblob enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="50931-163">For example, if NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST is returned, the entry Network Monitor could not find is included in the returned error BLOB.</span></span>



| <span data-ttu-id="50931-164">Informationen über</span><span class="sxs-lookup"><span data-stu-id="50931-164">For information about</span></span>                          | <span data-ttu-id="50931-165">Finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="50931-165">See</span></span>                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="50931-166">Abrufen des eingabeblobs, das eine NIC darstellt</span><span class="sxs-lookup"><span data-stu-id="50931-166">Obtaining the input BLOB that represents a NIC</span></span> | [<span data-ttu-id="50931-167">Auswählen einer Netzwerkschnittstellenkarte</span><span class="sxs-lookup"><span data-stu-id="50931-167">Selecting a Network Interface Card</span></span>](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a><span data-ttu-id="50931-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50931-168">Requirements</span></span>



| <span data-ttu-id="50931-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50931-169">Requirement</span></span> | <span data-ttu-id="50931-170">Wert</span><span class="sxs-lookup"><span data-stu-id="50931-170">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50931-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50931-171">Minimum supported client</span></span><br/> | <span data-ttu-id="50931-172">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50931-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="50931-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50931-173">Minimum supported server</span></span><br/> | <span data-ttu-id="50931-174">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="50931-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="50931-175">Header</span><span class="sxs-lookup"><span data-stu-id="50931-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="50931-176"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="50931-176"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="50931-177">DLL</span><span class="sxs-lookup"><span data-stu-id="50931-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50931-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50931-178"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50931-179">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50931-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50931-180">Idelta-DC</span><span class="sxs-lookup"><span data-stu-id="50931-180">IDelaydC</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="50931-181">Idelta aydc:: Configure</span><span class="sxs-lookup"><span data-stu-id="50931-181">IDelaydC::Configure</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="50931-182">Idelta aydc::D isconnect</span><span class="sxs-lookup"><span data-stu-id="50931-182">IDelaydC::Disconnect</span></span>](idelaydc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="50931-183">Idelta aydc:: Start</span><span class="sxs-lookup"><span data-stu-id="50931-183">IDelaydC::Start</span></span>](idelaydc-start.md)
</dt> </dl>

 

 




