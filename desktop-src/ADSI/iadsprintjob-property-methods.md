---
title: Iadsprintjob-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden für die iadsprintjob-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 23e7cbf3-09ce-44ce-b618-2c0fa6b34428
ms.tgt_platform: multiple
keywords:
- Iadsprintjob-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsPrintJob Property Methods
- IADsPrintJob.Description
- IADsPrintJob.get_Description
- IADsPrintJob.put_Description
- IADsPrintJob.HostPrintQueue
- IADsPrintJob.get_HostPrintQueue
- IADsPrintJob.Notify
- IADsPrintJob.get_Notify
- IADsPrintJob.put_Notify
- IADsPrintJob.NotifyPath
- IADsPrintJob.get_NotifyPath
- IADsPrintJob.put_NotifyPath
- IADsPrintJob.Priority
- IADsPrintJob.get_Priority
- IADsPrintJob.put_Priority
- IADsPrintJob.Size
- IADsPrintJob.get_Size
- IADsPrintJob.StartTime
- IADsPrintJob.get_StartTime
- IADsPrintJob.put_StartTime
- IADsPrintJob.TimeSubmitted
- IADsPrintJob.get_TimeSubmitted
- IADsPrintJob.TotalPages
- IADsPrintJob.get_TotalPages
- IADsPrintJob.UntilTime
- IADsPrintJob.get_UntilTime
- IADsPrintJob.User
- IADsPrintJob.get_User
- IADsPrintJob.UserPath
- IADsPrintJob.get_UserPath
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d1680484ff16d563ef5bc89de6d5abbfec2ce6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478120"
---
# <a name="iadsprintjob-property-methods"></a><span data-ttu-id="f3f85-105">Iadsprintjob-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="f3f85-105">IADsPrintJob Property Methods</span></span>

<span data-ttu-id="f3f85-106">Mit den Eigenschafts Methoden für die [**iadsprintjob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f3f85-106">Property methods for the [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="f3f85-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="f3f85-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="f3f85-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f3f85-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="f3f85-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f3f85-109">**Description**</span></span>
<span data-ttu-id="f3f85-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f3f85-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="f3f85-111">Die Beschreibung des Druckauftrags.</span><span class="sxs-lookup"><span data-stu-id="f3f85-111">The description of the print job.</span></span>

<dt>

<span data-ttu-id="f3f85-112">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f3f85-112">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f3f85-113">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f3f85-113">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Description(
  [out] BSTR* pbstrDescription
);
HRESULT put_Description(
  [in] BSTR bstrDescription
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3f85-114">**Hostprintqueue**</span><span class="sxs-lookup"><span data-stu-id="f3f85-114">**HostPrintQueue**</span></span>
<span data-ttu-id="f3f85-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f3f85-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="f3f85-116">Die ADsPath-Zeichenfolge der Druck Warteschlange, die den Druckauftrag verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f3f85-116">The ADsPath string of the Print Queue that processes the print job.</span></span>

<dt>

<span data-ttu-id="f3f85-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f85-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f85-118">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f3f85-118">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostPrintQueue(
  [out] BSTR* pbstrHostPrintQueue
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3f85-119">**Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="f3f85-119">**Notify**</span></span>
<span data-ttu-id="f3f85-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f3f85-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="f3f85-121">Der Benutzer, der benachrichtigt werden soll, wenn der Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f3f85-121">The user to be notified when job is completed.</span></span>

<dt>

<span data-ttu-id="f3f85-122">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f3f85-122">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f3f85-123">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f3f85-123">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Notify(
  [out] BSTR* pbstrNotify
);
HRESULT put_Notify(
  [in] BSTR bstrNotify
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3f85-124">**Notifypath**</span><span class="sxs-lookup"><span data-stu-id="f3f85-124">**NotifyPath**</span></span>
<span data-ttu-id="f3f85-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f3f85-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="f3f85-126">Die ADsPath-Zeichenfolge des Benutzer Objekts, das benachrichtigt werden soll, wenn der Druckauftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f3f85-126">The ADsPath string of the user object to be notified when the print job is completed.</span></span>

<dt>

<span data-ttu-id="f3f85-127">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f3f85-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f3f85-128">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f3f85-128">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_NotifyPath(
  [out] BSTR* pbstrNotifyPath
);
HRESULT put_NotifyPath(
  [in] BSTR bstrNotifyPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3f85-129">**Priority**</span><span class="sxs-lookup"><span data-stu-id="f3f85-129">**Priority**</span></span>
<span data-ttu-id="f3f85-130"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f3f85-130"></dt> <dd> <dl></span></span>

<span data-ttu-id="f3f85-131">Die Priorität des Druckauftrags.</span><span class="sxs-lookup"><span data-stu-id="f3f85-131">The priority of the print job.</span></span>

<dt>

<span data-ttu-id="f3f85-132">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f3f85-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f3f85-133">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="f3f85-133">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Priority(
  [out] LONG* plPriority
);
HRESULT put_Priority(
  [in] LONG lPriority
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3f85-134">**Größe**</span><span class="sxs-lookup"><span data-stu-id="f3f85-134">**Size**</span></span>
<span data-ttu-id="f3f85-135"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f3f85-135"></dt> <dd> <dl></span></span>

<span data-ttu-id="f3f85-136">Die Größe des Druckauftrags in Byte.</span><span class="sxs-lookup"><span data-stu-id="f3f85-136">The size, in bytes, of the print job.</span></span>

<dt>

<span data-ttu-id="f3f85-137">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f85-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f85-138">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="f3f85-138">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Size(
  [out] LONG* plSize
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3f85-139">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="f3f85-139">**StartTime**</span></span>
<span data-ttu-id="f3f85-140"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f3f85-140"></dt> <dd> <dl></span></span>

<span data-ttu-id="f3f85-141">Der früheste Zeitpunkt, zu dem der Druckauftrag gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3f85-141">The earliest time when the print job should be started.</span></span>

<dt>

<span data-ttu-id="f3f85-142">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f3f85-142">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f3f85-143">Skript Datentyp: **Datum**</span><span class="sxs-lookup"><span data-stu-id="f3f85-143">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartTime(
  [out] DATE* pdateStartTime
);
HRESULT put_StartTime(
  [in] DATE dateStartTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3f85-144">**Timesub;**</span><span class="sxs-lookup"><span data-stu-id="f3f85-144">**TimeSubmitted**</span></span>
<span data-ttu-id="f3f85-145"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f3f85-145"></dt> <dd> <dl></span></span>

<span data-ttu-id="f3f85-146">Der Zeitpunkt, zu dem der Auftrag an die Warteschlange übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="f3f85-146">The time when the job was submitted to the queue.</span></span>

<dt>

<span data-ttu-id="f3f85-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f85-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f85-148">Skript Datentyp: **Datum**</span><span class="sxs-lookup"><span data-stu-id="f3f85-148">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeSubmitted(
  [out] DATE* pdateTimeSubmitted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3f85-149">**TotalPages**</span><span class="sxs-lookup"><span data-stu-id="f3f85-149">**TotalPages**</span></span>
<span data-ttu-id="f3f85-150"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f3f85-150"></dt> <dd> <dl></span></span>

<span data-ttu-id="f3f85-151">Die Gesamtanzahl der Seiten im Druckauftrag.</span><span class="sxs-lookup"><span data-stu-id="f3f85-151">The total number of pages in the print job.</span></span>

<dt>

<span data-ttu-id="f3f85-152">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f85-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f85-153">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="f3f85-153">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TotalPages(
  [out] LONG* plTotalPages
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3f85-154">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="f3f85-154">**UntilTime**</span></span>
<span data-ttu-id="f3f85-155"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f3f85-155"></dt> <dd> <dl></span></span>

<span data-ttu-id="f3f85-156">Der letzte Zeitpunkt, zu dem der Druckauftrag gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3f85-156">The latest time when the print job should be started.</span></span>

<dt>

<span data-ttu-id="f3f85-157">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="f3f85-157">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f3f85-158">Skript Datentyp: **Datum**</span><span class="sxs-lookup"><span data-stu-id="f3f85-158">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UntilTime(
  [out] DATE* pdateUntilTime
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3f85-159">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="f3f85-159">**User**</span></span>
<span data-ttu-id="f3f85-160"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f3f85-160"></dt> <dd> <dl></span></span>

<span data-ttu-id="f3f85-161">Der Name des Benutzers, der den Druckauftrag übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="f3f85-161">The name of user who submitted the print job.</span></span>

<dt>

<span data-ttu-id="f3f85-162">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f85-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f85-163">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f3f85-163">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_User(
  [out] BSTR* pbstrUser
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="f3f85-164">**UserPath**</span><span class="sxs-lookup"><span data-stu-id="f3f85-164">**UserPath**</span></span>
<span data-ttu-id="f3f85-165"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="f3f85-165"></dt> <dd> <dl></span></span>

<span data-ttu-id="f3f85-166">Die ADsPath-Zeichenfolge des Benutzer Objekts, das diesen Druckauftrag übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="f3f85-166">The ADsPath string of the user object that submitted this print job.</span></span>

<dt>

<span data-ttu-id="f3f85-167">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="f3f85-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3f85-168">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f3f85-168">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UserPath(
  [out] BSTR* pbstrUserPath
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="f3f85-169">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3f85-169">Examples</span></span>

<span data-ttu-id="f3f85-170">Im folgenden Codebeispiel wird gezeigt, wie Sie mit Eigenschaften eines Druckauftrags Objekts arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f3f85-170">The following code example shows how to work with properties of a print job object.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Dim pj As IADsPrintJob
On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    MsgBox "Host Printer: " & pj.HostPrintQueue
    MsgBox "Job description: " & pj.Description
    MsgBox "job requester: " & pj.User 
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pj = Nothing
```



<span data-ttu-id="f3f85-171">Im folgenden Codebeispiel wird gezeigt, wie Sie mit Eigenschaften eines Druckauftrags Objekts arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f3f85-171">The following code example shows how to work with properties of a print job object.</span></span>


```C++
IADsPrintQueueOperations *pqo = NULL;
IADsPrintJob *pJob = NULL;
HRESULT hr = S_OK;
BSTR bstr = NULL;
VARIANT var;
ULONG lFetch = 0;
IDispatch *pDisp = NULL;
IADsCollection *pColl = NULL;
IUnknown *pUnk = NULL;
LPWSTR adsPath =L"WinNT://aMachine/aPrinter";

VariantInit(&var);

hr = ADsGetObject(adsPath, 
                  IID_IADsPrintQueueOperations, 
                  (void**)&pqo);
if(FAILED(hr)){goto Cleanup;}


hr = pqo->PrintJobs(&pColl);

// Enumerate print jobs. Code omitted.

hr = pColl->get__NewEnum(&pUnk);
if(FAILED(hr)){goto Cleanup;}


IEnumVARIANT *pEnum;
hr = pUnk->QueryInterface(IID_IEnumVARIANT,(void**)&pEnum);
if(FAILED(hr)){goto Cleanup;}


// Now Enumerate.
hr = pEnum->Next(1, &var, &lFetch);
if(FAILED(hr)){goto Cleanup;}

while(hr == S_OK)
{
    if (lFetch == 1)    
    {
        pDisp = V_DISPATCH(&var);
        pDisp->QueryInterface(IID_IADsPrintJob, (void**)&pJob);

        pJob->get_HostPrintQueue(&bstr);
        printf("HostPrintQueue: %S\n",bstr);
        SysFreeString(bstr);

        pJob->get_Description(&bstr);
        printf("Print job name: %S\n",bstr);
        SysFreeString(bstr);

        pJob->get_User(&bstr);
        printf("Requester: %S\n",bstr);
        SysFreeString(bstr);

        pJob->Release();
    }
    pDisp->Release();
    VariantClear(&var);
    hr = pEnum->Next(1, &var, &lFetch);
};

Cleanup:
    if(pEnum) pEnum->Release();
    if(pUnk) pUnk->Release();
    if(pColl) pColl->Release();
    if(pqo) pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="f3f85-172">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3f85-172">Requirements</span></span>



| <span data-ttu-id="f3f85-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3f85-173">Requirement</span></span> | <span data-ttu-id="f3f85-174">Wert</span><span class="sxs-lookup"><span data-stu-id="f3f85-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f85-175">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3f85-175">Minimum supported client</span></span><br/> | <span data-ttu-id="f3f85-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3f85-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f3f85-177">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3f85-177">Minimum supported server</span></span><br/> | <span data-ttu-id="f3f85-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3f85-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f3f85-179">Header</span><span class="sxs-lookup"><span data-stu-id="f3f85-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3f85-180"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3f85-180"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="f3f85-181">DLL</span><span class="sxs-lookup"><span data-stu-id="f3f85-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3f85-182"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3f85-182"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="f3f85-183">IID</span><span class="sxs-lookup"><span data-stu-id="f3f85-183">IID</span></span><br/>                      | <span data-ttu-id="f3f85-184">IID \_ iadsprintjob ist als 32fb6780-1ed0-11CF-A988-00aa006bc149 definiert.</span><span class="sxs-lookup"><span data-stu-id="f3f85-184">IID\_IADsPrintJob is defined as 32FB6780-1ED0-11CF-A988-00AA006BC149</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="f3f85-185">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3f85-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3f85-186">**Iadsprintjob**</span><span class="sxs-lookup"><span data-stu-id="f3f85-186">**IADsPrintJob**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[<span data-ttu-id="f3f85-187">Schnittstelleneigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="f3f85-187">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





