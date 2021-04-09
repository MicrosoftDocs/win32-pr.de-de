---
title: Iadsserviceoperations-Eigenschaften Methoden (IADs. h)
description: Die Eigenschaften Methoden der iadsserviceoperations-Schnittstelle lesen und schreiben die in der folgenden Liste beschriebenen Eigenschaften. Weitere Informationen zu Eigenschafts Methoden finden Sie unter Interface Property Methods.
ms.assetid: ebddfc42-1d2f-495b-b57c-f57419b54ff8
ms.tgt_platform: multiple
keywords:
- Iadsserviceoperations-Eigenschaften Methoden ADSI
topic_type:
- apiref
api_name:
- IADsServiceOperations Property Methods
- IADsServiceOperations.Status
- IADsServiceOperations.get_Status
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 654a92be1052d4e4c70e0274d719a49be965d8cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858829"
---
# <a name="iadsserviceoperations-property-methods"></a><span data-ttu-id="241bc-105">Iadsserviceoperations-Eigenschaften Methoden</span><span class="sxs-lookup"><span data-stu-id="241bc-105">IADsServiceOperations Property Methods</span></span>

<span data-ttu-id="241bc-106">Die Eigenschaften Methoden der [**iadsserviceoperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) -Schnittstelle lesen und schreiben die in der folgenden Liste beschriebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="241bc-106">The property methods of the [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) interface read and write the properties described in the following list.</span></span> <span data-ttu-id="241bc-107">Weitere Informationen zu Eigenschafts Methoden finden Sie unter [Interface Property Methods](interface-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="241bc-107">For more information about property methods, see [Interface Property Methods](interface-property-methods.md).</span></span>

## <a name="properties"></a><span data-ttu-id="241bc-108">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="241bc-108">Properties</span></span>

<dl> <dt>

<span data-ttu-id="241bc-109">**Status**</span><span class="sxs-lookup"><span data-stu-id="241bc-109">**Status**</span></span>
<span data-ttu-id="241bc-110"></dt> <dd> <dl></span><span class="sxs-lookup"><span data-stu-id="241bc-110"></dt> <dd> <dl></span></span>

<span data-ttu-id="241bc-111">Status des Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="241bc-111">Status of service.</span></span>

<span data-ttu-id="241bc-112">Die folgenden Werte sind möglich.</span><span class="sxs-lookup"><span data-stu-id="241bc-112">The following are possible values.</span></span>

<dt>

<span id="ADS_SERVICE_STOPPED"></span><span id="ads_service_stopped"></span>

<span data-ttu-id="241bc-113">**Anzeigen \_ Der Dienst wurde \_ beendet** (0x00000001).</span><span class="sxs-lookup"><span data-stu-id="241bc-113">**ADS\_SERVICE\_STOPPED** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_START_PENDING"></span><span id="ads_service_start_pending"></span>

<span data-ttu-id="241bc-114">**Anzeigen \_ Dienst \_ Start steht \_ aus** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="241bc-114">**ADS\_SERVICE\_START\_PENDING** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_STOP_PENDING"></span><span id="ads_service_stop_pending"></span>

<span data-ttu-id="241bc-115">**Anzeigen \_ Dienst \_ Beendigung steht \_ aus** (0x00000003)</span><span class="sxs-lookup"><span data-stu-id="241bc-115">**ADS\_SERVICE\_STOP\_PENDING** (0x00000003)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_RUNNING"></span><span id="ads_service_running"></span>

<span data-ttu-id="241bc-116">**Anzeigen \_ Dienst wird \_ ausgeführt** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="241bc-116">**ADS\_SERVICE\_RUNNING** (0x00000004)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_CONTINUE_PENDING"></span><span id="ads_service_continue_pending"></span>

<span data-ttu-id="241bc-117">**Anzeigen \_ Dienst \_ Fortsetzung steht \_ aus** (0x00000005 bei der)</span><span class="sxs-lookup"><span data-stu-id="241bc-117">**ADS\_SERVICE\_CONTINUE\_PENDING** (0x00000005)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSE_PENDING"></span><span id="ads_service_pause_pending"></span>

<span data-ttu-id="241bc-118">**Anzeigen \_ Dienst \_ Pause steht \_ aus** (0x00000006)</span><span class="sxs-lookup"><span data-stu-id="241bc-118">**ADS\_SERVICE\_PAUSE\_PENDING** (0x00000006)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSED"></span><span id="ads_service_paused"></span>

<span data-ttu-id="241bc-119">**Anzeigen \_ Der Dienst wurde \_ angeh** alten (0x00000007).</span><span class="sxs-lookup"><span data-stu-id="241bc-119">**ADS\_SERVICE\_PAUSED** (0x00000007)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR"></span><span id="ads_service_error"></span>

<span data-ttu-id="241bc-120">**Anzeigen \_ Dienst \_ Fehler** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="241bc-120">**ADS\_SERVICE\_ERROR** (0x00000008)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

<span data-ttu-id="241bc-121">**Anzeigen \_ Dienst \_ eigener \_ Prozess** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="241bc-121">**ADS\_SERVICE\_OWN\_PROCESS** (0x00000010)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

<span data-ttu-id="241bc-122">**Anzeigen \_ Dienst \_ Freigabe \_ Prozess** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="241bc-122">**ADS\_SERVICE\_SHARE\_PROCESS** (0x00000020)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

<span data-ttu-id="241bc-123">**Anzeigen \_ Dienst \_ Kernel \_ Treiber** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="241bc-123">**ADS\_SERVICE\_KERNEL\_DRIVER** (0x00000001)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

<span data-ttu-id="241bc-124">**Anzeigen \_ Dienst \_ Datei \_ System \_ Treiber** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="241bc-124">**ADS\_SERVICE\_FILE\_SYSTEM\_DRIVER** (0x00000002)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span data-ttu-id="241bc-125">**Anzeigen \_ Start des Dienst \_ \_ Starts** ( \_ Start des Dienst \_ Starts)</span><span class="sxs-lookup"><span data-stu-id="241bc-125">**ADS\_SERVICE\_BOOT\_START** (SERVICE\_BOOT\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span data-ttu-id="241bc-126">**Anzeigen \_ Dienst \_ System \_ Start** (Dienst \_ System \_ Start)</span><span class="sxs-lookup"><span data-stu-id="241bc-126">**ADS\_SERVICE\_SYSTEM\_START** (SERVICE\_SYSTEM\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span data-ttu-id="241bc-127">**Anzeigen \_ \_automatischer Dienst \_ Start** (Automatisches Starten des dienstanzstarts \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="241bc-127">**ADS\_SERVICE\_AUTO\_START** (SERVICE\_AUTO\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span data-ttu-id="241bc-128">**Anzeigen \_ Service \_ Demand- \_ Start** (Service Demand- \_ \_ Start)</span><span class="sxs-lookup"><span data-stu-id="241bc-128">**ADS\_SERVICE\_DEMAND\_START** (SERVICE\_DEMAND\_START)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span data-ttu-id="241bc-129">**Anzeigen \_ Dienst \_ deaktiviert** (Dienst \_ deaktiviert)</span><span class="sxs-lookup"><span data-stu-id="241bc-129">**ADS\_SERVICE\_DISABLED** (SERVICE\_DISABLED)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span data-ttu-id="241bc-130">**Anzeigen \_ Dienst \_ Fehler \_ ignorieren** (0)</span><span class="sxs-lookup"><span data-stu-id="241bc-130">**ADS\_SERVICE\_ERROR\_IGNORE** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span data-ttu-id="241bc-131">**Anzeigen \_ Dienst \_ Fehler \_ Normal** (1)</span><span class="sxs-lookup"><span data-stu-id="241bc-131">**ADS\_SERVICE\_ERROR\_NORMAL** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span data-ttu-id="241bc-132">**Anzeigen \_ Dienst \_ Fehler \_ schwerwiegend** (2)</span><span class="sxs-lookup"><span data-stu-id="241bc-132">**ADS\_SERVICE\_ERROR\_SEVERE** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span data-ttu-id="241bc-133">**Anzeigen \_ Dienst \_ Fehler \_ kritisch** (3)</span><span class="sxs-lookup"><span data-stu-id="241bc-133">**ADS\_SERVICE\_ERROR\_CRITICAL** (3)</span></span>


</dt> <dd></dd> </dl> <dt>

<span data-ttu-id="241bc-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="241bc-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="241bc-135">Skript Datentyp: **Long**</span><span class="sxs-lookup"><span data-stu-id="241bc-135">Scripting data type: **LONG**</span></span>
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* pstatus
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a><span data-ttu-id="241bc-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="241bc-136">Examples</span></span>

<span data-ttu-id="241bc-137">Im folgenden Codebeispiel wird gezeigt, wie der Status eines Microsoft-Faxdiensts überprüft wird, der unter Windows 2000 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="241bc-137">The following code example shows how to verify the status of a Microsoft Fax Service running on Windows 2000.</span></span>


```VB
Dim cp As IADsComputer
Dim sr As IADsService
Dim so As IADsServiceOperations
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
Set sr = cp.GetObject("Service", "Fax")
Set so = sr

Select Case so.Status
    Case ADS_SERVICE_STOPPED
        MsgBox "Microsoft Fax Service has stopped."
    Case ADS_SERVICE_RUNNING
        MsgBox "Microsoft Fax Service is running."
    Case ADS_SERVICE_PAUSED
        MsgBox "Microsoft Fax Service has paused."
    Case ADS_SERVICE_ERROR
        MsgBox "Microsoft Fax Service has errors."
End Select

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
    Set sr = Nothing
    Set so = Nothing
```



<span data-ttu-id="241bc-138">Im folgenden Codebeispiel wird der Status eines Microsoft-Faxdiensts überprüft, der unter Windows 2000 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="241bc-138">The following code example verifies the status of a Microsoft Fax Service running on Windows 2000.</span></span>


```C++
IADsContainer *pCont = NULL;
IADsServiceOperations *pSrvOp = NULL;
LPWSTR adsPath = L"WinNT://myMachine,computer";
IDispatch *pDisp = NULL;
long status = 0;

HRESULT hr = S_OK;

hr = ADsGetObject(adsPath,IID_IADsContainer,(void**)&pCont);
if(FAILED(hr)) {goto Cleanup;}

hr = pCont->GetObject(CComBSTR("Service"), CComBSTR("Fax"), &pDisp);
if(FAILED(hr)) {goto Cleanup;}

hr = pDisp->QueryInterface(IID_IADsServiceOperations,(void**)&pSrvOp);
if(FAILED(hr)) {goto Cleanup;}

hr = pSrvOp->get_Status(&status);
switch (status) 
{
    case ADS_SERVICE_STOPPED:
        printf("The service has stopped.\n");
        break;
    case ADS_SERVICE_RUNNING:
        printf("The service is running.\n");
        break;
    case ADS_SERVICE_PAUSED:
        printf("The service has paused.\n");
        break;
    case ADS_SERVICE_ERROR:
        printf("The service has errors.\n");
        break;
}

Cleanup:
    if(pDisp) pDisp->Release();
    if(pCont) pCont->Release();
    if(pSrvOp) pSrvOp->Release();
```



## <a name="requirements"></a><span data-ttu-id="241bc-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="241bc-139">Requirements</span></span>



| <span data-ttu-id="241bc-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="241bc-140">Requirement</span></span> | <span data-ttu-id="241bc-141">Wert</span><span class="sxs-lookup"><span data-stu-id="241bc-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="241bc-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="241bc-142">Minimum supported client</span></span><br/> | <span data-ttu-id="241bc-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="241bc-143">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="241bc-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="241bc-144">Minimum supported server</span></span><br/> | <span data-ttu-id="241bc-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="241bc-145">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="241bc-146">Header</span><span class="sxs-lookup"><span data-stu-id="241bc-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="241bc-147"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="241bc-147"><dt>Iads.h</dt></span></span> </dl>        |
| <span data-ttu-id="241bc-148">DLL</span><span class="sxs-lookup"><span data-stu-id="241bc-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="241bc-149"><dt>Activeds.dll</dt></span><span class="sxs-lookup"><span data-stu-id="241bc-149"><dt>Activeds.dll</dt></span></span> </dl>  |
| <span data-ttu-id="241bc-150">IID</span><span class="sxs-lookup"><span data-stu-id="241bc-150">IID</span></span><br/>                      | <span data-ttu-id="241bc-151">IID \_ iadsserviceoperations ist als 5d7b33f0-31ca-11CF-a98a-00aa006bc149 definiert.</span><span class="sxs-lookup"><span data-stu-id="241bc-151">IID\_IADsServiceOperations is defined as 5D7B33F0-31CA-11CF-A98A-00AA006BC149</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="241bc-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="241bc-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="241bc-153">**Iadsfileservice**</span><span class="sxs-lookup"><span data-stu-id="241bc-153">**IADsFileService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[<span data-ttu-id="241bc-154">**Iadsfileserviceoperations**</span><span class="sxs-lookup"><span data-stu-id="241bc-154">**IADsFileServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[<span data-ttu-id="241bc-155">**Iadsservice**</span><span class="sxs-lookup"><span data-stu-id="241bc-155">**IADsService**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[<span data-ttu-id="241bc-156">**Iadsserviceoperations**</span><span class="sxs-lookup"><span data-stu-id="241bc-156">**IADsServiceOperations**</span></span>](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> </dl>

 

 





