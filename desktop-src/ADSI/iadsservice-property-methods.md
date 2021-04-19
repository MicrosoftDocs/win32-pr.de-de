---
title: Iadsservice-Eigenschaften Methoden (IADs. h)
description: Lesen und schreiben Sie die in diesem Thema beschriebenen Eigenschaften.
ms.assetid: ff05ab0c-b4fe-4c67-8894-9ac8427ce5b8
ms.tgt_platform: multiple
keywords:
- Iadsservice-Eigenschaften Methoden ADSI
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
ms.openlocfilehash: 9b0e0d8b09618c7346280697843281ca74536c11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341793"
---
# <a name="iadsservice-property-methods"></a>Iadsservice-Eigenschaften Methoden

Die Eigenschaften Methoden der [**iadsservice**](/windows/desktop/api/Iads/nn-iads-iadsservice) -Schnittstelle lesen und schreiben die in diesem Thema beschriebenen Eigenschaften. Weitere Informationen finden Sie unter [Interface Property Methods](interface-property-methods.md).

## <a name="properties"></a>Eigenschaften

<dl> <dt>

**Abhängigkeiten**
</dt> <dd> <dl>

Array von **BSTR** -Namen für Dienste oder lade Gruppen, die geladen werden müssen, damit dieser Dienst geladen wird. Die Syntax für den Eintrag lautet "Service:", gefolgt vom Dienstnamen oder "Group:" gefolgt vom Namen der Ladegruppe.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Variant**
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

Der Anzeige Name des Dienstanbieter.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
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

Die Aktion, die ausgeführt werden soll, wenn dieser Dienst beim Starten fehlschlägt. Die folgenden Werte sind für diese Eigenschaft gültig.

<dt>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>

<span id="ADS_SERVICE_ERROR_IGNORE"></span><span id="ads_service_error_ignore"></span>ADS- \_ Dienst \_ Fehler \_ ignorieren * * * *


</dt> <dd>

Der Fehler wird vom Start Programm protokolliert, aber der Startvorgang wird fortgesetzt.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>

<span id="ADS_SERVICE_ERROR_NORMAL"></span><span id="ads_service_error_normal"></span>Anzeige \_ Dienst \_ Fehler \_ Normal * * * *


</dt> <dd>

Das Start Programm protokolliert den Fehler und zeigt ein Meldungs Feld an, setzt den Startvorgang jedoch fort.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>

<span id="ADS_SERVICE_ERROR_SEVERE"></span><span id="ads_service_error_severe"></span>ADS- \_ Dienst \_ Fehler \_ schwerwiegender * * * *


</dt> <dd>

Das Start Programm protokolliert den Fehler. Wenn die zuletzt bekannte, gute Konfiguration gestartet wurde, wird der Startvorgang fortgesetzt. Andernfalls wird das System mit der zuletzt bekannten, guten Konfiguration neu gestartet.

</dd> <dt>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>

<span id="ADS_SERVICE_ERROR_CRITICAL"></span><span id="ads_service_error_critical"></span>Anzeige \_ Dienst \_ Fehler \_ kritisch * * * *


</dt> <dd>

Das Start Programm protokolliert den Fehler, sofern möglich. Wenn die zuletzt bekannte, gute Konfiguration gestartet wird, tritt beim Startvorgang ein Fehler auf. Andernfalls wird das System mit der letzten als funktionierend bekannten Konfiguration neu gestartet.

</dd> </dl> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

**Host Computer**
</dt> <dd> <dl>

Die ADsPath-Zeichenfolge des Hosts dieses Diensts.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
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

Name der Gruppe der Lade Reihenfolge, in der dieser Dienst Mitglied ist.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
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

**Pfad**
</dt> <dd> <dl>

Pfad und Dateiname für die ausführbare Datei dieses Dienstanbieter.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
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

Der Name des Kontos, das dieser Dienst verwendet, um sich beim Start zu authentifizieren.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
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

**Serviceaccountpath**
</dt> <dd> <dl>

Der Pfad des Kontos, das durch die **serviceaccountpath** -Eigenschaft angegeben wird.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
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

Die Beschreibung, wie sich ein Dienst auf dem Host Computer darstellt. Diese Eigenschaft kann NULL sein oder eine Kombination aus einem oder mehreren der folgenden Werte aufweisen.

<dt>

<span id="ADS_SERVICE_KERNEL_DRIVER"></span><span id="ads_service_kernel_driver"></span>

ADS \_ \_ -Dienst Kernel \_ Treiber * * * * (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_FILE_SYSTEM_DRIVER"></span><span id="ads_service_file_system_driver"></span>

ADS- \_ Dienst \_ Datei \_ System \_ Treiber * * * * (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_OWN_PROCESS"></span><span id="ads_service_own_process"></span>

Eigener Prozess des ADS- \_ Dienstanbieter \_ \_ * * * * (0x00000010)


</dt> <dd></dd> <dt>

<span id="ADS_SERVICE_SHARE_PROCESS"></span><span id="ads_service_share_process"></span>

ADS- \_ Dienst \_ Freigabe \_ Prozess * * * * (0x00000020)


</dt> <dd></dd> </dl> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

Bestimmt, wie der Dienst gestartet wird. Die folgenden Werte sind für diese Eigenschaft gültig.

<dt>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>

<span id="ADS_SERVICE_BOOT_START"></span><span id="ads_service_boot_start"></span>Start des ADS- \_ Dienst \_ \_ Starts * * * *


</dt> <dd>

Der Dienst ist ein Gerätetreiber, der vom System Lade Modul gestartet wurde. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>

<span id="ADS_SERVICE_SYSTEM_START"></span><span id="ads_service_system_start"></span>Anzeigen des \_ Dienst \_ System \_ Starts * * * *


</dt> <dd>

Der Dienst ist ein Gerätetreiber, der von der **IoInitSystem** -Funktion gestartet wurde. Dieses Wert ist nur für Treiberdienste gültig.

</dd> <dt>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>

<span id="ADS_SERVICE_AUTO_START"></span><span id="ads_service_auto_start"></span>Automatischer Start des ADS- \_ Dienstanbieter \_ \_ * * * *


</dt> <dd>

Der Dienst wird automatisch vom Dienststeuerungs-Manager beim Systemstart gestartet.

</dd> <dt>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>

<span id="ADS_SERVICE_DEMAND_START"></span><span id="ads_service_demand_start"></span>Start des ADS \_ Service \_ Demand \_ * * * *


</dt> <dd>

Der Dienst wird vom Dienststeuerungs-Manager gestartet, wenn ein Prozess die [**Start Service**](/windows/desktop/api/winsvc/nf-winsvc-startservicea) -Funktion aufruft.

</dd> <dt>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>

<span id="ADS_SERVICE_DISABLED"></span><span id="ads_service_disabled"></span>ADS- \_ Dienst \_ deaktiviert * * * * *


</dt> <dd>

Der Dienst kann nicht gestartet werden. Der Versuch, den Dienst zu starten, führt dazu, dass der Fehlercode **Fehler \_ Dienst \_ deaktiviert** ist.

</dd> </dl> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **Long**
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

Parameter, die beim Start an den Dienst übermittelt werden.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
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

Version des Dienstanbieter.

<dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Skript Datentyp: **BSTR**
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

Im folgenden Codebeispiel wird gezeigt, wie alle verfügbaren Systemdienste, die auf dem Host Computer ausgeführt werden, "MyMachine", sowie der Speicherort für die ausführbaren Dateien der Dienste aufgelistet werden.


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
| Header<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ iadsservice ist als 68af66e0-31ca-11CF-a98a-00aa006bc149 definiert.<br/>          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iadsservice**](/windows/desktop/api/Iads/nn-iads-iadsservice)
</dt> <dt>

[Schnittstelleneigenschaften Methoden](interface-property-methods.md)
</dt> </dl>

 

