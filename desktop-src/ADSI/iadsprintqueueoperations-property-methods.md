---
title: Iadsprintqueueoperations-Eigenschaften Methoden (IADs. h)
description: Die Eigenschaften Methoden der iadsprintqueueoperations-Schnittstelle lesen und schreiben die in der folgenden Liste aufgeführten Eigenschaften. Weitere Informationen zu Eigenschafts Methoden finden Sie unter Interface Property Methods.
ms.assetid: a4e6bac5-5d52-4492-b48e-f051fec6158c
ms.tgt_platform: multiple
keywords:
- Iadsprintqueueoperations-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsPrintQueueOperations Property Methods
- IADsPrintQueueOperations.Status
- IADsPrintQueueOperations.get_Name
- IADsPrintQueueOperations.put_Name
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8af7aef94dd9453af690f0c5d83b1e978d3b058
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956904"
---
# <a name="iadsprintqueueoperations-property-methods"></a><span data-ttu-id="3b44e-105">Iadsprintqueueoperations-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="3b44e-105">IADsPrintQueueOperations Property Methods</span></span>

<span data-ttu-id="3b44e-106">Die Eigenschaften Methoden der [**iadsprintqueueoperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations) -Schnittstelle lesen und schreiben die in der folgenden Liste aufgeführten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3b44e-106">The property methods of the [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations) interface read and write the properties listed in the following list.</span></span> <span data-ttu-id="3b44e-107">Weitere Informationen zu Eigenschafts Methoden finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="3b44e-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="3b44e-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3b44e-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="3b44e-109">**Status**</span><span class="sxs-lookup"><span data-stu-id="3b44e-109">**Status**</span></span>
<span data-ttu-id="3b44e-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="3b44e-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="3b44e-111">Aktueller Status der Druck Warteschlangen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="3b44e-111">Current status of the print queue operations.</span></span> <span data-ttu-id="3b44e-112">Die gültigen Statuscode Werte sind in der folgenden Liste aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b44e-112">The valid status code values are listed in the following list.</span></span>

<dt>

<span id="ADS_PRINTER_PAUSED"></span><span id="ads_printer_paused"></span>

<span data-ttu-id="3b44e-113">**Anzeigen \_ Drucker \_ angeh** alten (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="3b44e-113">**ADS\_PRINTER\_PAUSED** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PENDING_DELETION"></span><span id="ads_printer_pending_deletion"></span>

<span data-ttu-id="3b44e-114">**Anzeigen \_ Drucker \_ ausstehende \_ Löschung** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="3b44e-114">**ADS\_PRINTER\_PENDING\_DELETION** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_ERROR"></span><span id="ads_printer_error"></span>

<span data-ttu-id="3b44e-115">**Anzeigen \_ Drucker \_ Fehler** (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="3b44e-115">**ADS\_PRINTER\_ERROR** (0x00000003)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_JAM"></span><span id="ads_printer_paper_jam"></span>

<span data-ttu-id="3b44e-116">**Anzeigen \_ Drucker \_ Papier \_ Stau** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="3b44e-116">**ADS\_PRINTER\_PAPER\_JAM** (0x00000004)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_OUT"></span><span id="ads_printer_paper_out"></span>

<span data-ttu-id="3b44e-117">**Anzeigen \_ Drucker \_ Papier \_** (0x00000005 bei der)</span><span class="sxs-lookup"><span data-stu-id="3b44e-117">**ADS\_PRINTER\_PAPER\_OUT** (0x00000005)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_MANUAL_FEED"></span><span id="ads_printer_manual_feed"></span>

<span data-ttu-id="3b44e-118">**Anzeigen \_ \_Manueller Drucker \_ Feed** (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="3b44e-118">**ADS\_PRINTER\_MANUAL\_FEED** (0x00000006)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_PROBLEM"></span><span id="ads_printer_paper_problem"></span>

<span data-ttu-id="3b44e-119">**Anzeigen \_ Drucker \_ Papier \_ Problem** (0x00000007)</span><span class="sxs-lookup"><span data-stu-id="3b44e-119">**ADS\_PRINTER\_PAPER\_PROBLEM** (0x00000007)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OFFLINE"></span><span id="ads_printer_offline"></span>

<span data-ttu-id="3b44e-120">**Anzeigen \_ Drucker \_ Offline** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="3b44e-120">**ADS\_PRINTER\_OFFLINE** (0x00000008)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_IO_ACTIVE"></span><span id="ads_printer_io_active"></span>

<span data-ttu-id="3b44e-121">**Anzeigen \_ Drucker \_ \_** -e/a aktiv (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="3b44e-121">**ADS\_PRINTER\_IO\_ACTIVE** (0x00000100)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_BUSY"></span><span id="ads_printer_busy"></span>

<span data-ttu-id="3b44e-122">**Anzeigen \_ Drucker \_ ausgelastet** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="3b44e-122">**ADS\_PRINTER\_BUSY** (0x00000200)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PRINTING"></span><span id="ads_printer_printing"></span>

<span data-ttu-id="3b44e-123">**Anzeigen \_ Drucker \_ Druck** (0x00000400)</span><span class="sxs-lookup"><span data-stu-id="3b44e-123">**ADS\_PRINTER\_PRINTING** (0x00000400)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUTPUT_BIN_FULL"></span><span id="ads_printer_output_bin_full"></span>

<span data-ttu-id="3b44e-124">**Anzeigen \_ Drucker \_ Ausgabe \_ bin \_ voll** (0x00000800)</span><span class="sxs-lookup"><span data-stu-id="3b44e-124">**ADS\_PRINTER\_OUTPUT\_BIN\_FULL** (0x00000800)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NOT_AVAILABLE"></span><span id="ads_printer_not_available"></span>

<span data-ttu-id="3b44e-125">**Anzeigen \_ Der Drucker ist \_ nicht \_ verfügbar** (0x00001000).</span><span class="sxs-lookup"><span data-stu-id="3b44e-125">**ADS\_PRINTER\_NOT\_AVAILABLE** (0x00001000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WAITING"></span><span id="ads_printer_waiting"></span>

<span data-ttu-id="3b44e-126">**Anzeigen \_ Drucker \_ wartet** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="3b44e-126">**ADS\_PRINTER\_WAITING** (0x00002000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PROCESSING"></span><span id="ads_printer_processing"></span>

<span data-ttu-id="3b44e-127">**Anzeigen \_ Drucker \_ Verarbeitung** (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="3b44e-127">**ADS\_PRINTER\_PROCESSING** (0x00004000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_INITIALIZING"></span><span id="ads_printer_initializing"></span>

<span data-ttu-id="3b44e-128">**Anzeigen \_ Drucker \_ Initialisierung** (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="3b44e-128">**ADS\_PRINTER\_INITIALIZING** (0x00008000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WARMING_UP"></span><span id="ads_printer_warming_up"></span>

<span data-ttu-id="3b44e-129">**Anzeigen \_ Drucker \_ Aufwärmen \_** (0x00010000 bis)</span><span class="sxs-lookup"><span data-stu-id="3b44e-129">**ADS\_PRINTER\_WARMING\_UP** (0x00010000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_TONER_LOW"></span><span id="ads_printer_toner_low"></span>

<span data-ttu-id="3b44e-130">**Anzeigen \_ Drucker \_ Toner \_ niedrig** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="3b44e-130">**ADS\_PRINTER\_TONER\_LOW** (0x00020000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NO_TONER"></span><span id="ads_printer_no_toner"></span>

<span data-ttu-id="3b44e-131">**Anzeigen \_ Drucker \_ kein \_ Toner** (0x00040000)</span><span class="sxs-lookup"><span data-stu-id="3b44e-131">**ADS\_PRINTER\_NO\_TONER** (0x00040000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAGE_PUNT"></span><span id="ads_printer_page_punt"></span>

<span data-ttu-id="3b44e-132">**Anzeigen \_ Drucker \_ Seite \_ Punt** (0x00080000)</span><span class="sxs-lookup"><span data-stu-id="3b44e-132">**ADS\_PRINTER\_PAGE\_PUNT** (0x00080000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_USER_INTERVENTION"></span><span id="ads_printer_user_intervention"></span>

<span data-ttu-id="3b44e-133">**Anzeigen \_ \_Benutzer \_ Eingriff** durch den Drucker (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="3b44e-133">**ADS\_PRINTER\_USER\_INTERVENTION** (0x00100000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUT_OF_MEMORY"></span><span id="ads_printer_out_of_memory"></span>

<span data-ttu-id="3b44e-134">**Anzeigen \_ Drucker \_ nicht \_ \_** genügend Arbeitsspeicher (0x00200000)</span><span class="sxs-lookup"><span data-stu-id="3b44e-134">**ADS\_PRINTER\_OUT\_OF\_MEMORY** (0x00200000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_DOOR_OPEN"></span><span id="ads_printer_door_open"></span>

<span data-ttu-id="3b44e-135">**Anzeigen \_ Drucker \_ Tür \_ geöffnet** (0x00400000)</span><span class="sxs-lookup"><span data-stu-id="3b44e-135">**ADS\_PRINTER\_DOOR\_OPEN** (0x00400000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_SERVER_UNKNOWN"></span><span id="ads_printer_server_unknown"></span>

<span data-ttu-id="3b44e-136">**Anzeigen \_ Drucker \_ Server \_ unbekannt** (0x00800000)</span><span class="sxs-lookup"><span data-stu-id="3b44e-136">**ADS\_PRINTER\_SERVER\_UNKNOWN** (0x00800000)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_POWER_SAVE"></span><span id="ads_printer_power_save"></span>

<span data-ttu-id="3b44e-137">**Anzeigen \_ Drucker \_ Strom \_ Speichern** (0x01000000)</span><span class="sxs-lookup"><span data-stu-id="3b44e-137">**ADS\_PRINTER\_POWER\_SAVE** (0x01000000)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="3b44e-138">Zugriffstyp: Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="3b44e-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="3b44e-139">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="3b44e-139">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] LONG* pbstrName
);
HRESULT put_Name(
  [in] LONG bstrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="3b44e-140">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b44e-140">Examples</span></span>

<span data-ttu-id="3b44e-141">Im folgenden Visual Basic Codebeispiel wird überprüft, ob ein Drucker Jammed ist.</span><span class="sxs-lookup"><span data-stu-id="3b44e-141">The following Visual Basic code example verifies that a printer is jammed.</span></span>


```VB
Dim pqo As IADsPrintQueueOperations
Set pqo = GetObject("WinNT://aMachine/aPrinter")
If pqo.Status = ADS_PRINTER_PAPER_JAM Then
MsgBox "Your printer is jammed."
End If
```



<span data-ttu-id="3b44e-142">Im folgenden C++-Codebeispiel wird überprüft, ob ein Drucker Jammed ist.</span><span class="sxs-lookup"><span data-stu-id="3b44e-142">The following C++ code example verifies that a printer is jammed.</span></span>


```C++
IADsPrintQueueOperations *pqo;
HRESULT hr = ADsGetObject(L"WinNT://aMachine/aPrinter",
IID_IADsPrintQueueOperations,
(void**)&pqo)
long status;
hr = pqo->get_Status(&status);
if(status = ADS_PRINTER_PAPER_JAM) {
printf("Your printer is jammed.\n");
}
hr = pqo->Release();
```



## <a name="requirements"></a><span data-ttu-id="3b44e-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b44e-143">Requirements</span></span>



| <span data-ttu-id="3b44e-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b44e-144">Requirement</span></span> | <span data-ttu-id="3b44e-145">Wert</span><span class="sxs-lookup"><span data-stu-id="3b44e-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b44e-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3b44e-146">Minimum supported client</span></span><br/> | <span data-ttu-id="3b44e-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b44e-147">Windows Vista</span></span><br/>                                                                    |
| <span data-ttu-id="3b44e-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3b44e-148">Minimum supported server</span></span><br/> | <span data-ttu-id="3b44e-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b44e-149">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="3b44e-150">Header</span><span class="sxs-lookup"><span data-stu-id="3b44e-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b44e-151"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b44e-151"><dt>Iads.h</dt></span></span> </dl>           |
| <span data-ttu-id="3b44e-152">DLL</span><span class="sxs-lookup"><span data-stu-id="3b44e-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b44e-153"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b44e-153"><dt>Activeds.dll</dt></span></span> </dl>     |
| <span data-ttu-id="3b44e-154">IID</span><span class="sxs-lookup"><span data-stu-id="3b44e-154">IID</span></span><br/>                      | <span data-ttu-id="3b44e-155">IID \_ iadsprintqueueoperations ist als 124be5c0-156e-11CF-a986-00aa006bc149 definiert.</span><span class="sxs-lookup"><span data-stu-id="3b44e-155">IID\_IADsPrintQueueOperations is defined as 124BE5C0-156E-11CF-A986-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3b44e-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b44e-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b44e-157">**Iadsprintqueue**</span><span class="sxs-lookup"><span data-stu-id="3b44e-157">**IADsPrintQueue**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[<span data-ttu-id="3b44e-158">**Iadsprintqueueoperations**</span><span class="sxs-lookup"><span data-stu-id="3b44e-158">**IADsPrintQueueOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)
</dt> </dl>

 

 





