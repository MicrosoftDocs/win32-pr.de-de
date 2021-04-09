---
title: Iadsprintjoboperations-Eigenschaften Methoden (IADs. h)
description: Die Eigenschaften Methoden der iadsprintjoboperations-Schnittstelle lesen und schreiben die in der folgenden Tabelle aufgeführten Eigenschaften. Weitere Informationen zu Eigenschafts Methoden finden Sie unter Interface Property Methods.
ms.assetid: d1710bd4-e600-4d92-892a-16b4316851d4
ms.tgt_platform: multiple
keywords:
- Iadsprintjoboperations-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsPrintJobOperations Property Methods
- IADsPrintJobOperations.Status
- IADsPrintJobOperations.get_Status
- IADsPrintJobOperations.TimeElapsed
- IADsPrintJobOperations.get_TimeElapsed
- IADsPrintJobOperations.PagesPrinted
- IADsPrintJobOperations.get_PagesPrinted
- IADsPrintJobOperations.Position
- IADsPrintJobOperations.get_Position
- IADsPrintJobOperations.put_Position
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2981fcdd8043c0eb0ee8b05cfd0331fe3abfabe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859114"
---
# <a name="iadsprintjoboperations-property-methods"></a><span data-ttu-id="48e72-105">Iadsprintjoboperations-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="48e72-105">IADsPrintJobOperations Property Methods</span></span>

<span data-ttu-id="48e72-106">Die Eigenschaften Methoden der [**iadsprintjoboperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) -Schnittstelle lesen und schreiben die in der folgenden Tabelle aufgeführten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="48e72-106">The property methods of the [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) interface read and write the properties listed in the following table.</span></span> <span data-ttu-id="48e72-107">Weitere Informationen zu Eigenschafts Methoden finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="48e72-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="48e72-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="48e72-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="48e72-109">**PagesPrinted**</span><span class="sxs-lookup"><span data-stu-id="48e72-109">**PagesPrinted**</span></span>
<span data-ttu-id="48e72-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48e72-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="48e72-111">Enthält die Anzahl der gedruckten Seiten.</span><span class="sxs-lookup"><span data-stu-id="48e72-111">Contains the number of pages printed.</span></span>

<dt>

<span data-ttu-id="48e72-112">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48e72-112">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48e72-113">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="48e72-113">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PagesPrinted(
  [out] LONG* plPagesPrinted
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="48e72-114">**Position**</span><span class="sxs-lookup"><span data-stu-id="48e72-114">**Position**</span></span>
<span data-ttu-id="48e72-115"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48e72-115"></dt> <dd> <dl></span></span>

<span data-ttu-id="48e72-116">Enthält die Position dieses Druckauftrags in der Druck Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="48e72-116">Contains the position of this print job in the print queue.</span></span>

<dt>

<span data-ttu-id="48e72-117">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="48e72-117">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48e72-118">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="48e72-118">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Position(
  [out] LONG* plPosition
);
HRESULT put_Position(
  [in] LONG lPosition
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="48e72-119">**Status**</span><span class="sxs-lookup"><span data-stu-id="48e72-119">**Status**</span></span>
<span data-ttu-id="48e72-120"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48e72-120"></dt> <dd> <dl></span></span>

<span data-ttu-id="48e72-121">Enthält den aktuellen Status des Druckauftrags, wie durch einen der [**ADSI Print Job-Status Konstanten**](adsi-print-job-status-constants.md) Werte angegeben.</span><span class="sxs-lookup"><span data-stu-id="48e72-121">Contains the current status of the print job as indicated by one of the [**ADSI Print Job Status Constants**](adsi-print-job-status-constants.md) values.</span></span>

<dt>

<span data-ttu-id="48e72-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48e72-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48e72-123">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="48e72-123">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* plStatus
);
```


</dt> </dl> </dd> <dt>

<span data-ttu-id="48e72-124">**Verstrichene Zeit**</span><span class="sxs-lookup"><span data-stu-id="48e72-124">**TimeElapsed**</span></span>
<span data-ttu-id="48e72-125"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="48e72-125"></dt> <dd> <dl></span></span>

<span data-ttu-id="48e72-126">Enthält die Anzahl der Millisekunden, die seit dem Start des Druckauftrags verstrichen sind.</span><span class="sxs-lookup"><span data-stu-id="48e72-126">Contains the number of milliseconds elapsed since the print job started.</span></span>

<dt>

<span data-ttu-id="48e72-127">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="48e72-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48e72-128">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="48e72-128">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeElapsed(
  [out] LONG* plTimeElapsed
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="48e72-129">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48e72-129">Examples</span></span>

<span data-ttu-id="48e72-130">Im folgenden Codebeispiel wird gezeigt, wie die Eigenschaften für [**iadsprintjoboperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="48e72-130">The following code example shows how the properties for [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) may be used.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Dim pjo As IADsPrintJobOperations

On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    Set pjo = pj
    MsgBox pjo.PagesPrinted & " pages printed for job " & pj.Name
    If (pjo.position > 1) Then
        pjo.Position = pjo.status - 1
    End If
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pjo = Nothing
```



## <a name="requirements"></a><span data-ttu-id="48e72-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="48e72-131">Requirements</span></span>



| <span data-ttu-id="48e72-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="48e72-132">Requirement</span></span> | <span data-ttu-id="48e72-133">Wert</span><span class="sxs-lookup"><span data-stu-id="48e72-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="48e72-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="48e72-134">Minimum supported client</span></span><br/> | <span data-ttu-id="48e72-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48e72-135">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="48e72-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="48e72-136">Minimum supported server</span></span><br/> | <span data-ttu-id="48e72-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48e72-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="48e72-138">Header</span><span class="sxs-lookup"><span data-stu-id="48e72-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="48e72-139"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="48e72-139"><dt>Iads.h</dt></span></span> </dl>         |
| <span data-ttu-id="48e72-140">DLL</span><span class="sxs-lookup"><span data-stu-id="48e72-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48e72-141"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48e72-141"><dt>Activeds.dll</dt></span></span> </dl>   |
| <span data-ttu-id="48e72-142">IID</span><span class="sxs-lookup"><span data-stu-id="48e72-142">IID</span></span><br/>                      | <span data-ttu-id="48e72-143">IID \_ iadsprintjoboperations ist als 32fb6780-1ed0-11CF-A988-00aa006bc149 definiert.</span><span class="sxs-lookup"><span data-stu-id="48e72-143">IID\_IADsPrintJobOperations is defined as 32FB6780-1ED0-11CF-A988-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48e72-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48e72-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48e72-145">**Iadsprintjob**</span><span class="sxs-lookup"><span data-stu-id="48e72-145">**IADsPrintJob**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[<span data-ttu-id="48e72-146">**Iadsprintjoboperations**</span><span class="sxs-lookup"><span data-stu-id="48e72-146">**IADsPrintJobOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)
</dt> <dt>

[<span data-ttu-id="48e72-147">**Iadsprintqueue**</span><span class="sxs-lookup"><span data-stu-id="48e72-147">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="48e72-148">**Status Konstanten für den ADSI-Druckauftrag**</span><span class="sxs-lookup"><span data-stu-id="48e72-148">**ADSI Print Job Status Constants**</span></span>](adsi-print-job-status-constants.md)
</dt> </dl>

 

 





