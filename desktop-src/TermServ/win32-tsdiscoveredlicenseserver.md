---
title: Win32_TSDiscoveredLicenseServer-Klasse
description: Enthält Details zum ermittelten Remotedesktop-Lizenzserver.
ms.assetid: 88523f30-26ad-4f78-a214-f54b7bc1c676
ms.tgt_platform: multiple
keywords:
- Win32_TSDiscoveredLicenseServer-Klasse Remotedesktopdienste
- Win32_TSDiscoveredLicenseServer Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSDiscoveredLicenseServer
- Win32_TSDiscoveredLicenseServer.LicenseServer
- Win32_TSDiscoveredLicenseServer.HowDiscovered
- Win32_TSDiscoveredLicenseServer.IsLSAvailable
- Win32_TSDiscoveredLicenseServer.IsAdminOnLS
- Win32_TSDiscoveredLicenseServer.IssuingCALs
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d633031df533068f2cf5da65f2f6820a93c78513
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478825"
---
# <a name="win32_tsdiscoveredlicenseserver-class"></a>Win32-Klasse "-Klasse (Klasse)" \_

Enthält Details zum ermittelten Remotedesktop-Lizenzserver.

## <a name="syntax"></a>Syntax

``` syntax
[abstract, AMENDMENT]
class Win32_TSDiscoveredLicenseServer
{
  string LicenseServer;
  uint32 HowDiscovered;
  uint32 IsLSAvailable;
  uint32 IsAdminOnLS;
  uint32 IssuingCALs;
};
```

## <a name="members"></a>Member

Die Win32-Klasse " **\_ zdiscoveredlicenseserver** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_** -Klasse "TS-Klasse" hat diese Eigenschaften.

<dl> <dt>

**Howentdeckt**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Diese Eigenschaft wird nicht mehr unterstützt.

**Windows Server 2008:** Die Remotedesktop-Lizenzserver-Ermittlungsmethode.

<dt>

<span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>

<span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**Grouppolicykonfigurierte** (0)


</dt> <dd>

Der Lizenzserver wurde mithilfe der Gruppenrichtlinie ermittelt.

</dd> <dt>

<span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>

<span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**Registrykonfigurierte** (1)


</dt> <dd>

Der Lizenzserver wurde mithilfe einer Registrierungs Einstellung ermittelt.

</dd> <dt>

<span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>

<span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**Workgroupdiscovery** (2)


</dt> <dd>

Der Lizenzserver wurde mithilfe des Arbeitsgruppen-Ermittlungs Bereichs erkannt.

</dd> <dt>

<span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>

<span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**Domaindiscovery** (3)


</dt> <dd>

Der Lizenzserver wurde mit dem Domänen Ermittlungs Bereich ermittelt.

</dd> <dt>

<span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>

<span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**Enterpriseediscovery** (4)


</dt> <dd>

Der Lizenzserver wurde mithilfe des Bereichs der Gesamtstruktur Ermittlung ermittelt.

</dd> </dl>

</dd> <dt>

**Isadminonls**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das Konto, das zum Ausführen des Skripts oder der exe-Datei verwendet wird, das die **Win32 \_ tsdiscoveredlicenseserver** -Klasse verwendet, über Administrator Zugriff auf den Lizenzserver verfügt.

<dt>

<span id="No"></span><span id="no"></span><span id="NO"></span>

<span id="No"></span><span id="no"></span><span id="NO"></span>**Nein** (0)


</dt> <dd>

Das verwendete Konto hat keinen Administrator Zugriff auf den Lizenzserver.

</dd> <dt>

<span id="Yes"></span><span id="yes"></span><span id="YES"></span>

<span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Ja** (1)


</dt> <dd>

Das verwendete Konto hat Administrator Zugriff auf den Lizenzserver.

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>Nicht **bekannt** (2)


</dt> <dd>

Es kann nicht bestimmt werden, ob das verwendete Konto über Administrator Zugriff auf den Lizenzserver verfügt.

</dd> </dl>

</dd> <dt>

**Islsavailable**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Lizenzserver verfügbar ist (ob eine RPC-Verbindung des Remote Prozedur Aufrufs \[ \] zum Server hergestellt werden kann).

<dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Nicht verfügbar** (0)


</dt> <dd>

Der Lizenzserver ist nicht verfügbar.

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Verfügbar** (1)


</dt> <dd>

Der Lizenzserver ist verfügbar.

</dd> </dl>

</dd> <dt>

**Issuingcals**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Lizenzserver Remotedesktopdienste Client Zugriffs Lizenzen (RDS-CALs) für den RD-Sitzungshost Server ausgeben darf.

<dt>

<span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Nicht zulässig** (0)


</dt> <dd>

Der Lizenzserver darf keine RDS-CALs für den RD-Sitzungshost Server ausgeben.

</dd> <dt>

<span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>

<span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Zulässig** (1)


</dt> <dd>

Der Lizenzserver kann RDS-CALs für den RD-Sitzungshost Server ausgeben.

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>Nicht **bekannt** (2)


</dt> <dd>

Es kann nicht bestimmt werden, ob der Lizenzserver RDS-CALs für den RD-Sitzungshost Server ausgeben darf.

</dd> </dl>

</dd> <dt>

**Licenseserver**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Name des ermittelten Remotedesktop Lizenzservers.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Zum Herstellen einer Verbindung mit dem \\ root \\ CIMV2 \\ TerminalServices-Namespace muss die Authentifizierungs Ebene den Datenschutz für das Paket enthalten. Bei C/C++-aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene der **RPC- \_ c- \_ authn- \_ Ebene \_ Pkt \_ Privacy**. Bei Visual Basic-und Skript aufrufen handelt es sich hierbei um eine Authentifizierungs Ebene von **wbemauthenticationlevelpzprivacy** oder "PKTPRIVACY" mit einem Wert von 6. Im folgenden Visual Basic Scripting Edition (VBScript)-Beispiel wird gezeigt, wie eine Verbindung mit einem Remote Computer mit Paket Datenschutz hergestellt wird.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



 

