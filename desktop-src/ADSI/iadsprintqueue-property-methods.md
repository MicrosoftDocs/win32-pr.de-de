---
title: Iadsprintqueue-Eigenschaften Methoden (IADs. h)
description: Mit den Eigenschafts Methoden der iadsprintqueue-Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt. Weitere Informationen finden Sie unter Interface Property Methods.
ms.assetid: 7f5b4200-65c8-4230-8561-ad4fefb391f3
ms.tgt_platform: multiple
keywords:
- Iadsprintqueue-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsPrintQueue Property Methods
- IADsPrintQueue.BannerPage
- IADsPrintQueue.get_BannerPage
- IADsPrintQueue.put_BannerPage
- IADsPrintQueue.Datatype
- IADsPrintQueue.get_Datatype
- IADsPrintQueue.put_Datatype
- IADsPrintQueue.DefaultJobPriority
- IADsPrintQueue.get_DefaultJobPriority
- IADsPrintQueue.put_DefaultJobPriority
- IADsPrintQueue.Description
- IADsPrintQueue.get_Description
- IADsPrintQueue.put_Description
- IADsPrintQueue.HostComputer
- IADsPrintQueue.get_HostComputer
- IADsPrintQueue.put_HostComputer
- IADsPrintQueue.Location
- IADsPrintQueue.get_Location
- IADsPrintQueue.put_Location
- IADsPrintQueue.Model
- IADsPrintQueue.get_Model
- IADsPrintQueue.put_Model
- IADsPrintQueue.PrintDevices
- IADsPrintQueue.get_PrintDevices
- IADsPrintQueue.put_PrintDevices
- IADsPrintQueue.PrinterPath
- IADsPrintQueue.get_PrinterPath
- IADsPrintQueue.put_PrinterPath
- IADsPrintQueue.PrintProcessor
- IADsPrintQueue.get_PrintProcessor
- IADsPrintQueue.put_PrintProcessor
- IADsPrintQueue.Priority
- IADsPrintQueue.get_Priority
- IADsPrintQueue.put_Priority
- IADsPrintQueue.StartTime
- IADsPrintQueue.get_StartTime
- IADsPrintQueue.put_StartTime
- IADsPrintQueue.UntilTime
- IADsPrintQueue.get_UntilTime
- IADsPrintQueue.put_UntilTime
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e8b7b2260805dbf5fa144f239111b6e29f5ec78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104213727"
---
# <a name="iadsprintqueue-property-methods"></a><span data-ttu-id="0d507-105">Iadsprintqueue-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="0d507-105">IADsPrintQueue Property Methods</span></span>

<span data-ttu-id="0d507-106">Mit den Eigenschafts Methoden der [**iadsprintqueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) -Schnittstelle werden die in der folgenden Tabelle beschriebenen Eigenschaften angezeigt oder festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0d507-106">The property methods of the [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) interface get or set the properties described in the following table.</span></span> <span data-ttu-id="0d507-107">Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="0d507-107">For more information, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="0d507-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0d507-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="0d507-109">**Bannerpage**</span><span class="sxs-lookup"><span data-stu-id="0d507-109">**BannerPage**</span></span>
<span data-ttu-id="0d507-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d507-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d507-111">Der Dateisystempfad, der auf die Bannerseite verweist, die zum Trennen von Druckaufträgen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d507-111">The file system path that points to the banner page used to separate print jobs.</span></span> <span data-ttu-id="0d507-112">Wenn der Wert **null** ist, wird keine Bannerseite verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d507-112">If **NULL**, no banner page is used.</span></span>

<dt>

<span data-ttu-id="0d507-113">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0d507-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d507-114">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d507-114">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BannerPage(
  [out] BSTR* pbstrBannerPage
);
HRESULT put_BannerPage(
  [in] BSTR bstrBannerPage
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0d507-115">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="0d507-115">**Datatype**</span></span>
<span data-ttu-id="0d507-116"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d507-116"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d507-117">Der Datentyp, der von dieser Warteschlange verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0d507-117">The data type that can be processed by this queue.</span></span>

<dt>

<span data-ttu-id="0d507-118">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0d507-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d507-119">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d507-119">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Datatype(
  [out] BSTR* pbstrDatatype
);
HRESULT put_Datatype(
  [in] BSTR bstrDatatype
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0d507-120">**Defaultjobpriority**</span><span class="sxs-lookup"><span data-stu-id="0d507-120">**DefaultJobPriority**</span></span>
<span data-ttu-id="0d507-121"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d507-121"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d507-122">Die jedem Druckauftrag zugewiesene Standardpriorität.</span><span class="sxs-lookup"><span data-stu-id="0d507-122">The default priority assigned to each print job.</span></span>

<dt>

<span data-ttu-id="0d507-123">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0d507-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d507-124">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d507-124">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DefaultJobPriority(
  [out] LONG* plDefaultJobPriority
);
HRESULT put_DefaultJobPriority(
  [in] BSTR lDefaultJobPriority
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0d507-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d507-125">**Description**</span></span>
<span data-ttu-id="0d507-126"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d507-126"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d507-127">Die Textbeschreibung dieser Druck Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="0d507-127">The text description of this print queue.</span></span>

<dt>

<span data-ttu-id="0d507-128">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0d507-128">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d507-129">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d507-129">Scripting data type: **BSTR**</span></span>
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

<span data-ttu-id="0d507-130">**Host Computer**</span><span class="sxs-lookup"><span data-stu-id="0d507-130">**HostComputer**</span></span>
<span data-ttu-id="0d507-131"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d507-131"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d507-132">Die ADsPath-Zeichenfolge, die auf den Host Computer verweist.</span><span class="sxs-lookup"><span data-stu-id="0d507-132">The ADsPath string that references the host computer.</span></span>

<dt>

<span data-ttu-id="0d507-133">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0d507-133">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d507-134">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d507-134">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_HostComputer(
  [out] BSTR* pbstrHostComputer
);
HRESULT put_HostComputer(
  [in] BSTR bstrHostComputer
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0d507-135">**Location**</span><span class="sxs-lookup"><span data-stu-id="0d507-135">**Location**</span></span>
<span data-ttu-id="0d507-136"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d507-136"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d507-137">Der Speicherort der Warteschlange, wie von einem Administrator beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0d507-137">The location of the queue as described by an administrator.</span></span>

<dt>

<span data-ttu-id="0d507-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0d507-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d507-139">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d507-139">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Location(
  [out] BSTR* pbstrLocation
);
HRESULT put_Location(
  [in] BSTR bstrLocation
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0d507-140">**Modell**</span><span class="sxs-lookup"><span data-stu-id="0d507-140">**Model**</span></span>
<span data-ttu-id="0d507-141"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d507-141"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d507-142">Der Name des Treibers, der von dieser Druck Warteschlange verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0d507-142">The name of the driver used by this print queue.</span></span>

<dt>

<span data-ttu-id="0d507-143">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0d507-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d507-144">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d507-144">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Model(
  [out] BSTR* pbstrModel
);
HRESULT put_Model(
  [in] BSTR bstrModel
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0d507-145">**Printdevices**</span><span class="sxs-lookup"><span data-stu-id="0d507-145">**PrintDevices**</span></span>
<span data-ttu-id="0d507-146"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d507-146"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d507-147">Ein SafeArray von **BSTR** , das die Namen der Druckgeräte enthält, für die diese Druck Warteschlange Aufträge Spool.</span><span class="sxs-lookup"><span data-stu-id="0d507-147">A SAFEARRAY of **BSTR** that contains the names of the print devices to which this print queue spools jobs.</span></span>

<dt>

<span data-ttu-id="0d507-148">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0d507-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d507-149">Skript Datentyp: **Variant**</span><span class="sxs-lookup"><span data-stu-id="0d507-149">Scripting data type: **VARIANT**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintDevices(
  [out] VARIANT* pvPrintDevices
);
HRESULT put_PrintDevices(
  [in] VARIANT vPrintDevices
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0d507-150">**PrinterPath**</span><span class="sxs-lookup"><span data-stu-id="0d507-150">**PrinterPath**</span></span>
<span data-ttu-id="0d507-151"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d507-151"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d507-152">Die Zeichenfolge, die auf den Pfad verweist, über den auf einen freigegebenen Drucker zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="0d507-152">The string that references the path by which a shared printer can be accessed.</span></span>

<dt>

<span data-ttu-id="0d507-153">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0d507-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d507-154">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d507-154">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrinterPath(
  [out] BSTR* pbstrPrinterPath
);
HRESULT put_PrinterPath(
  [in] BSTR bstrPrinterPath
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0d507-155">**PrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="0d507-155">**PrintProcessor**</span></span>
<span data-ttu-id="0d507-156"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d507-156"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d507-157">Der Druck Prozessor, der dieser Warteschlange zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0d507-157">The print processor associated with this queue.</span></span>

<dt>

<span data-ttu-id="0d507-158">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0d507-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d507-159">Skript Datentyp: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d507-159">Scripting data type: **BSTR**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PrintProcessor(
  [out] BSTR* pbstrPrintProcessor
);
HRESULT put_PrintProcessor(
  [in] BSTR bstrPrintProcessor
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="0d507-160">**Priority**</span><span class="sxs-lookup"><span data-stu-id="0d507-160">**Priority**</span></span>
<span data-ttu-id="0d507-161"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d507-161"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d507-162">Die Priorität dieser Drucker Objekt-Auftrags Warteschlange für alle verbundenen Geräte.</span><span class="sxs-lookup"><span data-stu-id="0d507-162">The priority of this printer object job queue for any connected devices.</span></span> <span data-ttu-id="0d507-163">Alle Aufträge in Druck Warteschlangen Objekten höherer Priorität werden zuerst verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0d507-163">All jobs in higher priority print queue objects will be processed first.</span></span>

<dt>

<span data-ttu-id="0d507-164">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0d507-164">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d507-165">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="0d507-165">Scripting data type: **LONG**</span></span>
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

<span data-ttu-id="0d507-166">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="0d507-166">**StartTime**</span></span>
<span data-ttu-id="0d507-167"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d507-167"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d507-168">Der Zeitpunkt, zu dem die Warteschlange die Verarbeitung von Aufträgen beginnen soll.</span><span class="sxs-lookup"><span data-stu-id="0d507-168">The time when the queue should begin processing jobs.</span></span> <span data-ttu-id="0d507-169">Der Datums Teil der Uhrzeit wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0d507-169">The date portion of the time is ignored.</span></span>

<dt>

<span data-ttu-id="0d507-170">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0d507-170">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d507-171">Skript Datentyp: **Datum**</span><span class="sxs-lookup"><span data-stu-id="0d507-171">Scripting data type: **DATE**</span></span>
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

<span data-ttu-id="0d507-172">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="0d507-172">**UntilTime**</span></span>
<span data-ttu-id="0d507-173"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="0d507-173"></dt> <dd> <dl></span></span>

<span data-ttu-id="0d507-174">Der Zeitpunkt, zu dem die Warteschlange die Verarbeitung von Aufträgen beenden soll.</span><span class="sxs-lookup"><span data-stu-id="0d507-174">The time when the queue should stop processing jobs.</span></span>

<dt>

<span data-ttu-id="0d507-175">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="0d507-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0d507-176">Skript Datentyp: **Datum**</span><span class="sxs-lookup"><span data-stu-id="0d507-176">Scripting data type: **DATE**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_UntilTime(
  [out] DATE* pdateUntilTime
);
HRESULT put_UntilTime(
  [in] DATE dateUntilTime
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="0d507-177">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0d507-177">Examples</span></span>

<span data-ttu-id="0d507-178">Im folgenden Codebeispiel wird gezeigt, wie ermittelt wird, ob ein angegebener Drucker online oder offline ist.</span><span class="sxs-lookup"><span data-stu-id="0d507-178">The following code example shows how to determine if a specified printer is online or offline.</span></span>


```VB
Dim pq As IADsPrintQueue
Dim pqo As IADsPrintQueueOperations
On Error GoTo Cleanup
 
Set pq = GetObject("WinNT://aMachine/aPrinter")
Set pqo = pq
If pqo.status = ADS_PRINTER_OFFLINE Then
    MsgBox pq.Model & "@" & pq.Location & is offline."
Else
    MsgBox pq.Model & "@" & pq.Location & is online."
End If

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pq = Nothing
    Set pqo = Nothing
```



<span data-ttu-id="0d507-179">Im folgenden Codebeispiel wird gezeigt, wie ermittelt wird, ob ein angegebener Drucker online oder offline ist.</span><span class="sxs-lookup"><span data-stu-id="0d507-179">The following code example shows how to determine if a specified printer is online or offline.</span></span>


```C++
IADsPrintQueue *pq = NULL;
HRESULT hr = S_OK;
IADsPrintQueueOperations *pqo = NULL;
BSTR model = NULL;
BSTR location = NULL;

LPWSTR adsPath = L"WinNT://aMachine/aPrinter";
hr = ADsGetObject(adsPath,
                  IID_IADsPrintQueue,
                  (void**)&pq);
if(FAILED(hr)) {goto Cleanup;}


hr = pq->QueryInterface(IID_IADsPrintQueueOperations,(void**)&pqo);
if(FAILED(hr)) {goto Cleanup;}

long status;
hr = pqo->get_Status(&status);
if(FAILED(hr)) {goto Cleanup;}

hr = pq->get_Model(&model);
if(FAILED(hr)) {goto Cleanup;}

hr =pq->get_Location(&location);
if(FAILED(hr)) {goto Cleanup;}

if(status == ADS_PRINTER_OFFLINE) 
{
    printf("%S @ %S is offline.\n",model,location);
} 
else 
{
    printf("%S @ %S is online.\n",model,location);
}


Cleanup:
    SysFreeString(model);
    SysFreeString(location);
    if(pq) pq->Release();
    if(pqo) pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="0d507-180">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d507-180">Requirements</span></span>



| <span data-ttu-id="0d507-181">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d507-181">Requirement</span></span> | <span data-ttu-id="0d507-182">Wert</span><span class="sxs-lookup"><span data-stu-id="0d507-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d507-183">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d507-183">Minimum supported client</span></span><br/> | <span data-ttu-id="0d507-184">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d507-184">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d507-185">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d507-185">Minimum supported server</span></span><br/> | <span data-ttu-id="0d507-186">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d507-186">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d507-187">Header</span><span class="sxs-lookup"><span data-stu-id="0d507-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d507-188"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d507-188"><dt>Iads.h</dt></span></span> </dl>       |
| <span data-ttu-id="0d507-189">DLL</span><span class="sxs-lookup"><span data-stu-id="0d507-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d507-190"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d507-190"><dt>Activeds.dll</dt></span></span> </dl> |
| <span data-ttu-id="0d507-191">IID</span><span class="sxs-lookup"><span data-stu-id="0d507-191">IID</span></span><br/>                      | <span data-ttu-id="0d507-192">IID \_ iadsprintqueue ist als B15160D0-1226-11CF-A985-00AA006BC149 definiert.</span><span class="sxs-lookup"><span data-stu-id="0d507-192">IID\_IADsPrintQueue is defined as B15160D0-1226-11CF-A985-00AA006BC149</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0d507-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d507-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d507-194">**Iadsprintqueue**</span><span class="sxs-lookup"><span data-stu-id="0d507-194">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="0d507-195">Schnittstelleneigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="0d507-195">Interface Property Methods</span></span>](interface-property-methods.md)
</dt> </dl>

 

 





