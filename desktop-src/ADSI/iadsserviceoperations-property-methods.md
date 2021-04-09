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
# <a name="iadsserviceoperations-property-methods"></a>Iadsserviceoperations-Eigenschaften Methoden

Die Eigenschaften Methoden der [**iadsserviceoperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations) -Schnittstelle lesen und schreiben die in der folgenden Liste beschriebenen Eigenschaften. Weitere Informationen zu Eigenschafts Methoden finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Status**
</dt> <dd> <dl>

Status des Dienstanbieter.

Die folgenden Werte sind möglich.

<dt>

<span id="ADS_SERVICE_STOPPED"></span><span id="ads_service_stopped"></span>

**Anzeigen \_ Der Dienst wurde \_ beendet** (0x00000001).


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_START_PENDING"></span><span id="ads_service_start_pending"></span>

**Anzeigen \_ Dienst \_ Start steht \_ aus** (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_STOP_PENDING"></span><span id="ads_service_stop_pending"></span>

**Anzeigen \_ Dienst \_ Beendigung steht \_ aus** (0x00000003)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_RUNNING"></span><span id="ads_service_running"></span>

**Anzeigen \_ Dienst wird \_ ausgeführt** (0x00000004)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_CONTINUE_PENDING"></span><span id="ads_service_continue_pending"></span>

**Anzeigen \_ Dienst \_ Fortsetzung steht \_ aus** (0x00000005 bei der)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSE_PENDING"></span><span id="ads_service_pause_pending"></span>

**Anzeigen \_ Dienst \_ Pause steht \_ aus** (0x00000006)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_PAUSED"></span><span id="ads_service_paused"></span>

**Anzeigen \_ Der Dienst wurde \_ angeh** alten (0x00000007).


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR"></span><span id="ads_service_error"></span>

**Anzeigen \_ Dienst \_ Fehler** (0x00000008)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

**Anzeigen \_ Dienst \_ eigener \_ Prozess** (0x00000010)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

**Anzeigen \_ Dienst \_ Freigabe \_ Prozess** (0x00000020)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

**Anzeigen \_ Dienst \_ Kernel \_ Treiber** (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

**Anzeigen \_ Dienst \_ Datei \_ System \_ Treiber** (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

**Anzeigen \_ Start des Dienst \_ \_ Starts** ( \_ Start des Dienst \_ Starts)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

**Anzeigen \_ Dienst \_ System \_ Start** (Dienst \_ System \_ Start)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

**Anzeigen \_ \_automatischer Dienst \_ Start** (Automatisches Starten des dienstanzstarts \_ \_ )


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

**Anzeigen \_ Service \_ Demand- \_ Start** (Service Demand- \_ \_ Start)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

**Anzeigen \_ Dienst \_ deaktiviert** (Dienst \_ deaktiviert)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

**Anzeigen \_ Dienst \_ Fehler \_ ignorieren** (0)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

**Anzeigen \_ Dienst \_ Fehler \_ Normal** (1)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

**Anzeigen \_ Dienst \_ Fehler \_ schwerwiegend** (2)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

**Anzeigen \_ Dienst \_ Fehler \_ kritisch** (3)


</dt> <dd></dd> </dl> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Skript Datentyp: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* pstatus
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Beispiele

Im folgenden Codebeispiel wird gezeigt, wie der Status eines Microsoft-Faxdiensts überprüft wird, der unter Windows 2000 ausgeführt wird.


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



Im folgenden Codebeispiel wird der Status eines Microsoft-Faxdiensts überprüft, der unter Windows 2000 ausgeführt wird.


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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                 |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>  |
| IID<br/>                      | IID \_ iadsserviceoperations ist als 5d7b33f0-31ca-11CF-a98a-00aa006bc149 definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iadsfileservice**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)
</dt> <dt>

[**Iadsfileserviceoperations**](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations)
</dt> <dt>

[**Iadsservice**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[**Iadsserviceoperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)
</dt> </dl>

 

 





