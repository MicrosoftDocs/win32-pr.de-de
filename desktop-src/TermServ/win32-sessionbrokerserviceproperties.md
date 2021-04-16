---
title: Win32_SessionBrokerServiceProperties-Klasse
description: Definiert die Abfrage für einen Sitzungs Broker Dienst.
ms.assetid: fe7a0317-8b52-4685-9d0d-2f81058b4561
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerServiceProperties-Klasse Remotedesktopdienste
- Win32_SessionBrokerServiceProperties Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties.SBNetworkName
- Win32_SessionBrokerServiceProperties.SBDbConnectionString
- Win32_SessionBrokerServiceProperties.SBDbSecondaryConnectionString
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 507c4211b9506e0635966e9541167d24495735ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518980"
---
# <a name="win32_sessionbrokerserviceproperties-class"></a>Win32 \_ sessionbrokerserviceproperties-Klasse

Definiert die Abfrage für einen Sitzungs Broker Dienst.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, singleton, provider("Win32_WIN32_SESSIONBROKERSERVICEPROPERTIES_Prov"), AMENDMENT]
class Win32_SessionBrokerServiceProperties
{
  string SBNetworkName;
  string SBDbConnectionString;
  string SBDbSecondaryConnectionString;
};
```

## <a name="members"></a>Member

Die **Win32 \_ sessionbrokerserviceproperties** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](/windows)

### <a name="methods"></a>Methoden

Die **Win32 \_ sessionbrokerserviceproperties** -Klasse verfügt über diese Methoden.



| Methode                                                                                                | BESCHREIBUNG                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Delta-bdbconnectionstring**](win32-sessionbrokerserviceproperties-deletesbdbconnectionstring.md) | Löscht DB-Verbindungs Zeichenfolgen (Primär und sekundär) aus der Registrierung.<br/> **Windows Server 2012 R2, Windows Server 2012 und Windows Server 2008 R2:** Diese Methode ist vor Windows Server 2016 nicht verfügbar.<br/> |
| [**Installbrokerdatabase**](win32-sessionbrokerserviceproperties-installbrokerdatabase.md)           | Installiert RD-Verbindungsbroker DB auf Central SQL Server<br/>                                                                                                                                                                    |
| [**Isdbreachable**](win32-sessionbrokerserviceproperties-isdbreachable.md)                           | Prüft, ob DB erreichbar ist.<br/>                                                                                                                                                                                                 |
| [**Setbrokerhamode**](win32-sessionbrokerserviceproperties-setbrokerhamode.md)                       | Migriert Daten von der lokalen wid-Datenbank zum neuen SQL Server basierten DB. Außerdem wird der Broker Server für die Verwendung des zentralen SQL Server konfiguriert.<br/>                                                                                        |
| [**Setbrokernonhamode**](win32-sessionbrokerserviceproperties-setbrokernonhamode.md)                 | Migriert Daten von der zentralen SQL Server zur lokalen Datenbank. Außerdem wird der Broker Server für die Verwendung der lokalen Datenbank konfiguriert.<br/>                                                                                                              |
| [**"Menbdbconnectionstrings"**](win32-sessionbrokerserviceproperties-setsbdbconnectionstrings.md)     | Speichert DB-Verbindungs Zeichenfolgen (Primär und sekundär) in der Registrierung.<br/> **Windows Server 2012 R2, Windows Server 2012 und Windows Server 2008 R2:** Diese Methode ist vor Windows Server 2016 nicht verfügbar.<br/>     |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ sessionbrokerserviceproperties** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Sbdbconnectionstring**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Vom Sitzungs Broker Dienst verwendete Daten bankverbindungs Zeichenfolge.

**Windows Server 2008 R2:** Diese Eigenschaft ist vor Windows Server 2012 nicht verfügbar.

</dd> <dt>

**Sbdbsecondaryconnectionstring**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Dies ist optional. Verbindungs Zeichenfolge der sekundären Datenbank, die vom Sitzungs Broker Dienst zur Unterstützung des Kennworts verwendet wird

**Windows Server 2012 R2, Windows Server 2012 und Windows Server 2008 R2:** Diese Eigenschaft ist vor Windows Server 2016 nicht verfügbar.

</dd> <dt>

**Sbnetworkname**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der vom Sitzungs Broker Dienst verwendete Netzwerkname.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>"Tssdwmi. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

