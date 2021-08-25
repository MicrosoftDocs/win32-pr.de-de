---
title: Win32_SessionBrokerServiceProperties-Klasse
description: Definiert die Abfrage für einen Sitzungsbrokerdienst.
ms.assetid: fe7a0317-8b52-4685-9d0d-2f81058b4561
ms.tgt_platform: multiple
keywords:
- Win32_SessionBrokerServiceProperties-Klassen-Remotedesktopdienste
- Win32_SessionBrokerServiceProperties-Klasse Remotedesktopdienste beschrieben
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
ms.openlocfilehash: 3f095272ee0d836e77542e20badbe5bb1169206cc6b0e87d742e3fbd235acd52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656180"
---
# <a name="win32_sessionbrokerserviceproperties-class"></a>Win32 \_ SessionBrokerServiceProperties-Klasse

Definiert die Abfrage für einen Sitzungsbrokerdienst.

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

Die **Win32 \_ SessionBrokerServiceProperties-Klasse** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](/windows)

### <a name="methods"></a>Methoden

Die **Win32 \_ SessionBrokerServiceProperties-Klasse** verfügt über diese Methoden.



| Methode                                                                                                | Beschreibung                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DeleteSBDbConnectionString**](win32-sessionbrokerserviceproperties-deletesbdbconnectionstring.md) | Löscht Datenbankverbindungszeichenfolgen (primär und sekundär) aus der Registrierung.<br/> **Windows Server 2012 R2, Windows Server 2012 und Windows Server 2008 R2:** Diese Methode ist vor Windows Server 2016 nicht verfügbar.<br/> |
| [**InstallBrokerDatabase**](win32-sessionbrokerserviceproperties-installbrokerdatabase.md)           | Installiert rd connection broker db on central SQL Server<br/>                                                                                                                                                                    |
| [**IsDbReachable**](win32-sessionbrokerserviceproperties-isdbreachable.md)                           | Überprüft, ob die Datenbank erreichbar ist.<br/>                                                                                                                                                                                                 |
| [**SetBrokerHAMode**](win32-sessionbrokerserviceproperties-setbrokerhamode.md)                       | Migriert Daten von der lokalen WID-Datenbank zur neuen SQL Server-basierten Datenbank. Außerdem wird der Brokerserver für die Verwendung des zentralen SQL Server<br/>                                                                                        |
| [**SetBrokerNonHAMode**](win32-sessionbrokerserviceproperties-setbrokernonhamode.md)                 | Migriert Daten von zentralen SQL Server zur lokalen Datenbank. Außerdem wird der Brokerserver für die Verwendung der lokalen Datenbank konfiguriert.<br/>                                                                                                              |
| [**SetSBDbConnectionStrings**](win32-sessionbrokerserviceproperties-setsbdbconnectionstrings.md)     | Speichert Datenbankverbindungszeichenfolgen (primär und sekundär) in der Registrierung.<br/> **Windows Server 2012 R2, Windows Server 2012 und Windows Server 2008 R2:** Diese Methode ist vor Windows Server 2016 nicht verfügbar.<br/>     |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ SessionBrokerServiceProperties-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**SBDbConnectionString**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Vom Sitzungsbrokerdienst verwendete Datenbankverbindungszeichenfolge.

**Windows Server 2008 R2:** Diese Eigenschaft ist vor Windows Server 2012 nicht verfügbar.

</dd> <dt>

**SBDbSecondaryConnectionString**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Optional. Verbindungszeichenfolge der sekundären Datenbank, die vom Sitzungsbrokerdienst zur Unterstützung des Kennwortablaufs verwendet wird.

**Windows Server 2012 R2, Windows Server 2012 und Windows Server 2008 R2:** Diese Eigenschaft ist vor Windows Server 2016 nicht verfügbar.

</dd> <dt>

**SBNetworkName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der vom Sitzungsbrokerdienst verwendete Netzwerkname.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                      |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



 

