---
title: Win32_TSDiscoveredLicenseServer-Klasse
description: Stellt Details zum ermittelten Remotedesktop Lizenzserver bereit.
ms.assetid: 88523f30-26ad-4f78-a214-f54b7bc1c676
ms.tgt_platform: multiple
keywords:
- Win32_TSDiscoveredLicenseServer-Klassen-Remotedesktopdienste
- Win32_TSDiscoveredLicenseServer -Klasse Remotedesktopdienste beschrieben
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
ms.openlocfilehash: 8ea5698083f0a639b0cd955126418f5024906d4f140dc22c54aacf1460f24c0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126998"
---
# <a name="win32_tsdiscoveredlicenseserver-class"></a>Win32 \_ TSDiscoveredLicenseServer-Klasse

Stellt Details zum ermittelten Remotedesktop Lizenzserver bereit.

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

Die **Win32 \_ TSDiscoveredLicenseServer-Klasse** verfügt über folgende Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ TSDiscoveredLicenseServer-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**HowDiscovered**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **VERALTET**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Diese Eigenschaft wird nicht mehr unterstützt.

**Windows Server 2008:** Die Remotedesktop Lizenzserver-Ermittlungsmethode.

<dt>

<span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>

<span id="GroupPolicyConfigured"></span><span id="grouppolicyconfigured"></span><span id="GROUPPOLICYCONFIGURED"></span>**GroupPolicyConfigured** (0)


</dt> <dd>

Der Lizenzserver wurde mithilfe von Gruppenrichtlinien ermittelt.

</dd> <dt>

<span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>

<span id="RegistryConfigured"></span><span id="registryconfigured"></span><span id="REGISTRYCONFIGURED"></span>**RegistryConfigured** (1)


</dt> <dd>

Der Lizenzserver wurde mithilfe einer Registrierungseinstellung ermittelt.

</dd> <dt>

<span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>

<span id="WorkgroupDiscovery"></span><span id="workgroupdiscovery"></span><span id="WORKGROUPDISCOVERY"></span>**WorkgroupDiscovery** (2)


</dt> <dd>

Der Lizenzserver wurde mithilfe des Ermittlungsbereichs der Arbeitsgruppe ermittelt.

</dd> <dt>

<span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>

<span id="DomainDiscovery"></span><span id="domaindiscovery"></span><span id="DOMAINDISCOVERY"></span>**DomainDiscovery** (3)


</dt> <dd>

Der Lizenzserver wurde mithilfe des Domänenermittlungsbereichs ermittelt.

</dd> <dt>

<span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>

<span id="EnterpriseDiscovery"></span><span id="enterprisediscovery"></span><span id="ENTERPRISEDISCOVERY"></span>**EnterpriseDiscovery** (4)


</dt> <dd>

Der Lizenzserver wurde mithilfe des Gesamtstrukturermittlungsbereichs ermittelt.

</dd> </dl>

</dd> <dt>

**IsAdminOnLS**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob das Konto, das zum Ausführen des Skripts oder .exe Datei verwendet wird, die die **Win32 \_ TSDiscoveredLicenseServer-Klasse** verwendet, Administratorzugriff auf den Lizenzserver hat.

<dt>

<span id="No"></span><span id="no"></span><span id="NO"></span>

<span id="No"></span><span id="no"></span><span id="NO"></span>**Nein** (0)


</dt> <dd>

Das verwendete Konto hat keinen Administratorzugriff auf den Lizenzserver.

</dd> <dt>

<span id="Yes"></span><span id="yes"></span><span id="YES"></span>

<span id="Yes"></span><span id="yes"></span><span id="YES"></span>**Ja** (1)


</dt> <dd>

Das verwendete Konto hat Administratorzugriff auf den Lizenzserver.

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Nicht bekannt** (2)


</dt> <dd>

Es kann nicht ermittelt werden, ob das verwendete Konto Administratorzugriff auf den Lizenzserver hat.

</dd> </dl>

</dd> <dt>

**IsLSAvailable**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Lizenzserver verfügbar ist (ob eine \[ Remoteprozeduraufruf-RPC-Verbindung \] mit dem Server hergestellt werden kann).

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

**AusstellendeCALs**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Lizenzserver Remotedesktopdienste Clientzugriffslizenzen (RDS CALs) an den RD-Sitzungshost Server ausstellen darf.

<dt>

<span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

<span id="Not_Allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>**Nicht zulässig** (0)


</dt> <dd>

Der Lizenzserver darf keine RDS-CALs für den RD-Sitzungshost Server ausstellen.

</dd> <dt>

<span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>

<span id="Allowed"></span><span id="allowed"></span><span id="ALLOWED"></span>**Zulässig** (1)


</dt> <dd>

Der Lizenzserver kann RDS-CALs an den RD-Sitzungshost Server ausstellen.

</dd> <dt>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>

<span id="Dont_know"></span><span id="dont_know"></span><span id="DONT_KNOW"></span>**Nicht bekannt** (2)


</dt> <dd>

Es kann nicht bestimmt werden, ob der Lizenzserver RDS-CALs an den RD-Sitzungshost Server ausstellen darf.

</dd> </dl>

</dd> <dt>

**LicenseServer**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Name des ermittelten Remotedesktop Lizenzservers.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Um eine Verbindung mit dem \\ \\ CIMV2 \\ TerminalServices-Stammnamespace herzustellen, muss die Authentifizierungsebene Paketdatenschutz enthalten. Bei C/C++-Aufrufen ist dies eine Authentifizierungsebene von **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Bei Visual Basic- und Skriptaufrufen ist dies die Authentifizierungsebene **WbemAuthenticationLevelPktPrivacy** oder "pktPrivacy" mit dem Wert 6. Das folgende Beispiel Visual Basic Scripting Edition (VBScript) zeigt, wie Sie eine Verbindung mit einem Remotecomputer mit Paketschutz herstellen.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



 

