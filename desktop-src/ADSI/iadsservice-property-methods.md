---
title: IADsService-Eigenschaftsmethoden (Iads.h)
description: Lesen und schreiben Sie die in diesem Thema beschriebenen Eigenschaften.
ms.assetid: ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8
ms.tgt_platform: multiple
keywords:
- IADsService-Eigenschaftsmethoden ADSI
topic_type:
- apiref
api_name:
- IADsService Property Methods
- IADsService.Dependencies
- IADsService.get_Dependencies
- IADsService.put_Dependencies
- IADsService.DisplayName
- IADsService.get_DisplayName
- IADsService.put_DisplayName
- IADsService.ErrorControl
- IADsService.get_ErrorControl
- IADsService.put_ErrorControl
- IADsService.HostComputer
- IADsService.get_HostComputer
- IADsService.put_HostComputer
- IADsService.LoadOrderGroup
- IADsService.get_LoadOrderGroup
- IADsService.put_LoadOrderGroup
- IADsService.Path
- IADsService.get_Path
- IADsService.put_Path
- IADsService.ServiceAccountName
- IADsService.get_ServiceAccountName
- IADsService.put_ServiceAccountName
- IADsService.ServiceAccountPath
- IADsService.get_ServiceAccountPath
- IADsService.put_ServiceAccountPath
- IADsService.ServiceType
- IADsService.get_ServiceType
- IADsService.put_ServiceType
- IADsService.StartType
- IADsService.get_StartType
- IADsService.put_StartType
- IADsService.StartupParameters
- IADsService.get_StartupParameters
- IADsService.put_StartupParameters
- IADsService.Version
- IADsService.get_Version
- IADsService.put_Version
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: babbd7605b990776141d158d455e9df2aeb9864d7619158e16bab7e113f84d7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690979"
---
# <a name="iadsservice-property-methods"></a>IADsService-Eigenschaftsmethoden

Die Eigenschaftenmethoden der [**IADsService-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadsservice) lesen und schreiben die in diesem Thema beschriebenen Eigenschaften. Weitere Informationen finden Sie unter [Schnittstelleneigenschaftsmethoden.](interface-property-methods.md)

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Abhängigkeiten**
</dt> <dd> <dl>

Array von **BSTR-Namen** von Diensten oder Ladegruppen, die geladen werden müssen, damit dieser Dienst geladen werden kann. Die Syntax für den Eintrag ist "Service:", gefolgt vom Dienstnamen oder "Group:", gefolgt vom Namen der Ladegruppe.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Dependencies(
  [out] VARIANT* pvServiceDepend
);
HRESULT put_Dependencies(
  [in] VARIANT vServiceDepend
);
```


</dt> </dl> </dd> <dt>

**DisplayName**
</dt> <dd> <dl>

Der Benutzerfreundlichkeitsname des Diensts.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DisplayName(
  [out] BSTR* pbstrDisplayName
);
HRESULT put_DisplayName(
  [in] BSTR bstrDisplayName
);
```


</dt> </dl> </dd> <dt>

**ErrorControl**
</dt> <dd> <dl>

Die Aktion, die ausgeführt werden soll, wenn dieser Dienst beim Start fehlschlägt. Im Folgenden finden Sie gültige Werte für diese Eigenschaft.

<dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>ADS \_ SERVICE \_ ERROR \_ IGNORE**


</dt> <dd>

Das Startprogramm protokolliert den Fehler, setzt den Startvorgang jedoch fort.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>ADS \_ SERVICE \_ ERROR \_ NORMAL**


</dt> <dd>

Das Startprogramm protokolliert den Fehler und zeigt ein Meldungsfeld an, setzt den Startvorgang jedoch fort.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>ADS \_ SERVICE \_ ERROR \_ SEVERE**


</dt> <dd>

Das Startprogramm protokolliert den Fehler. Wenn die letzte als funktionierend bekannte Konfiguration gestartet wird, wird der Startvorgang fortgesetzt. Andernfalls wird das System mit der letzten als gut bekannten Konfiguration neu gestartet.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>\_ADS-DIENSTFEHLER \_ \_ KRITISCH


</dt> <dd>

Das Startprogramm protokolliert den Fehler nach Möglichkeit. Wenn die letzte als funktionierend bekannte Konfiguration gestartet wird, schlägt der Startvorgang fehl. Andernfalls wird das System mit der letzten bekannten guten Konfiguration neu gestartet.

</dd> </dl> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ErrorControl(
  [out] LONG* plErrorControl
);
HRESULT put_ErrorControl(
  [in] LONG lErrorControl
);
```


</dt> </dl> </dd> <dt>

**HostComputer**
</dt> <dd> <dl>

Die ADsPath-Zeichenfolge des Hosts dieses Diensts.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
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

**LoadOrderGroup**
</dt> <dd> <dl>

Name der Ladeauftragsgruppe, in der dieser Dienst Mitglied ist.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LoadOrderGroup(
  [out] BSTR* pbstrLoadOrderGroup
);
HRESULT put_LoadOrderGroup(
  [in] BSTR bstrLoadOrderGroup
);
```


</dt> </dl> </dd> <dt>

**Path**
</dt> <dd> <dl>

Pfad und Dateiname zur ausführbaren Datei dieses Diensts.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Path(
  [out] BSTR* pbstrPath
);
HRESULT put_Path(
  [in] BSTR bstrPath
);
```


</dt> </dl> </dd> <dt>

**ServiceAccountName**
</dt> <dd> <dl>

Name des Kontos, das dieser Dienst verwendet, um sich beim Start zu authentifizieren.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountName(
  [out] BSTR* pbstrServiceAccountName
);
HRESULT put_ServiceAccountName(
  [in] BSTR bstrServiceAccountName
);
```


</dt> </dl> </dd> <dt>

**ServiceAccountPath**
</dt> <dd> <dl>

Der Pfad des kontos, das durch die **ServiceAccountPath-Eigenschaft angegeben** wird.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceAccountPath(
  [out] BSTR* pbstrServiceAccountPath
);
HRESULT put_ServiceAccountPath(
  [in] BSTR bstrServiceAccountPath
);
```


</dt> </dl> </dd> <dt>

**ServiceType**
</dt> <dd> <dl>

Die Beschreibung der Darstellung eines Diensts auf dem Hostcomputer. Diese Eigenschaft kann 0 (null) oder eine Kombination aus mindestens einem der folgenden Werte sein.

<dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

ADS \_ SERVICE \_ KERNEL \_ DRIVER** (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

ADS \_ SERVICE FILE SYSTEM \_ \_ \_ DRIVER** (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

ADS \_ SERVICE \_ OWN \_ PROCESS** (0x00000010)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

ADS \_ SERVICE \_ SHARE \_ PROCESS** (0x00000020)


</dt> <dd></dd> </dl> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ServiceType(
  [out] LONG* plServiceType
);
HRESULT put_ServiceType(
  [in] LONG lServiceType
);
```


</dt> </dl> </dd> <dt>

**Starttyp**
</dt> <dd> <dl>

Bestimmt, wie der Dienst gestartet wird. Im Folgenden finden Sie gültige Werte für diese Eigenschaft.

<dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>ADS \_ SERVICE \_ BOOT \_ START**


</dt> <dd>

Der Dienst ist ein Gerätetreiber, der vom Systemlader gestartet wird. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>ADS \_ SERVICE \_ SYSTEM \_ START**


</dt> <dd>

Der Dienst ist ein Gerätetreiber, der von der **IoInitSystem-Funktion gestartet** wird. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>ADS \_ SERVICE \_ AUTO \_ START**


</dt> <dd>

Der Dienst wird automatisch vom Dienststeuerungs-Manager während des Systemstarts gestartet.

</dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>ADS \_ SERVICE \_ DEMAND \_ START**


</dt> <dd>

Der Dienst wird vom Dienststeuerungs-Manager gestartet, wenn ein Prozess die [**StartService-Funktion**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) aufruft.

</dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>ADS \_ SERVICE \_ DISABLED**


</dt> <dd>

Der Dienst kann nicht gestartet werden. Versuche, den Dienst zu starten, führen zum Fehlercode **ERROR \_ SERVICE \_ DISABLED**.

</dd> </dl> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartType(
  [out] LONG* plStartType
);
HRESULT put_StartType(
  [in] LONG lStartType
);
```


</dt> </dl> </dd> <dt>

**StartupParameters**
</dt> <dd> <dl>

Parameter, die beim Start an den Dienst übergeben werden.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StartupParameters(
  [out] BSTR* pbstrStartupParameters
);
HRESULT put_StartupParameters(
  [in] BSTR bstrStartupParameters
);
```


</dt> </dl> </dd> <dt>

**Version**
</dt> <dd> <dl>

Version des Diensts.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skriptdatentyp: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Version(
  [out] BSTR* pbstrVersion
);
HRESULT put_Version(
  [in] BSTR bstrVersion
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Beispiele

Das folgende Codebeispiel zeigt, wie alle verfügbaren Systemdienste, die auf dem Hostcomputer "myMachine" ausgeführt werden, zusammen mit dem Speicherort zum Suchen der ausführbaren Dateien der Dienste aufgeführt werden.


```VB
Dim cp As IADsComputer
On Error GoTo Cleanup

Set cp = GetObject("WinNT://myMachine,computer")
If (IsEmpty(cp) = False) Then
    cp.Filter = Array("Service")
    For Each service In cp
        MsgBox service.Name & " @" & service.path
    Next
End if

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set cp = Nothing
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsService ist als 68AF66E0-31CA-11CF-A98A-00AA006BC149 definiert.<br/>          |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[Schnittstelleneigenschaftsmethoden](interface-property-methods.md)
</dt> </dl>

 

