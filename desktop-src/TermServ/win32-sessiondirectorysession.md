---
title: Win32_SessionDirectorySession-Klasse
description: Stellt Eigenschaften zum Anzeigen der Eigenschaften einer Remotedesktopverbindung Broker-Sitzung (RD-Verbindungsbroker) bereit.
ms.assetid: 34b5a898-3952-493c-ba62-dd0d298b0600
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectorySession-Klassen-Remotedesktopdienste
- Win32_SessionDirectorySession-Klasse Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionDirectorySession
- Win32_SessionDirectorySession.ServerName
- Win32_SessionDirectorySession.SessionID
- Win32_SessionDirectorySession.UserName
- Win32_SessionDirectorySession.DomainName
- Win32_SessionDirectorySession.ServerIPAddress
- Win32_SessionDirectorySession.TSProtocol
- Win32_SessionDirectorySession.ApplicationType
- Win32_SessionDirectorySession.ResolutionWidth
- Win32_SessionDirectorySession.ResolutionHeight
- Win32_SessionDirectorySession.ColorDepth
- Win32_SessionDirectorySession.CreateTime
- Win32_SessionDirectorySession.DisconnectTime
- Win32_SessionDirectorySession.SessionState
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0a7d883d3b356713f2f9c3d2b1f9de76676e845020b211ee8a600604a674c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118848194"
---
# <a name="win32_sessiondirectorysession-class"></a>Win32 \_ SessionDirectorySession-Klasse

Stellt Eigenschaften zum Anzeigen der Eigenschaften einer Remotedesktopverbindung Broker-Sitzung (RD-Verbindungsbroker) bereit.

> [!Note]  
> In Windows Server 2008 R2 wurde der Name von Terminal Services Session Broker (TS Session Broker) in RD-Verbindungsbroker geändert. Diese Eigenschaften gelten für alle unterstützten Betriebssysteme, sofern nicht anders angegeben.

 

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSESSION_Prov"), AMENDMENT]
class Win32_SessionDirectorySession
{
  string   ServerName;
  uint32   SessionID;
  string   UserName;
  string   DomainName;
  string   ServerIPAddress;
  uint32   TSProtocol;
  string   ApplicationType;
  uint32   ResolutionWidth;
  uint32   ResolutionHeight;
  uint32   ColorDepth;
  DateTime CreateTime;
  DateTime DisconnectTime;
  uint32   SessionState;
};
```

## <a name="members"></a>Member

Die **Win32 \_ SessionDirectorySession-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ SessionDirectorySession-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ApplicationType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anwendung wurde mit dieser Sitzung gestartet. Dies entspricht der **StartProgram-Eigenschaft** von [**IMsTscSecuredSettings.**](imstscsecuredsettings-interface.md)

</dd> <dt>

**ColorDepth**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Farbtiefe der Sitzung, gemessen in Bits pro Pixel.

</dd> <dt>

**CreateTime**
</dt> <dd> <dl> <dt>

Datentyp: **DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datum und Uhrzeit der Erstellung der Sitzung. Dieser Wert wird nicht zurückgesetzt, wenn eine Sitzung getrennt und erneut verbunden wird.

</dd> <dt>

**DisconnectTime**
</dt> <dd> <dl> <dt>

Datentyp: **DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datum und Uhrzeit der Trennung der Sitzung (falls zutreffend).

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Domänenname des Benutzers, der bei dieser Sitzung angemeldet ist.

</dd> <dt>

**ResolutionHeight**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Höhe der Sitzung in Pixel für diese Sitzung.

</dd> <dt>

**ResolutionWidth**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Breite der Sitzung in Pixel für diese Sitzung.

</dd> <dt>

**ServerIPAddress**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

IP-Adresse des RD-Verbindungsbrokerservers für diese Sitzung.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Name des RD-Verbindungsbrokerservers für diese Sitzung.

</dd> <dt>

**Sessionid**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Sitzungs-ID für diese Sitzung.

</dd> <dt>

**Sessionstate**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Status dieser Sitzung.

<dt>

0
</dt> <dd>

Die Sitzung ist aktiv.

</dd> <dt>

1
</dt> <dd>

Die Sitzung wird getrennt.

</dd> </dl>

</dd> <dt>

**TSProtocol**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Protokoll für diese Sitzung.

<dt>

0
</dt> <dd>

Diese Sitzung wird auf einer physischen Konsole ausgeführt.

</dd> <dt>

1
</dt> <dd>

Für diese Sitzung wird ein proprietäres Drittanbieterprotokoll verwendet.

</dd> <dt>

2
</dt> <dd>

Remotedesktopprotokoll (RDP) wird für diese Sitzung verwendet.

</dd> </dl>

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Benutzername des Benutzers, der bei dieser Sitzung angemeldet ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows Management Instrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ SessionDirectoryCluster**](win32-sessiondirectorycluster.md)
</dt> <dt>

[**Win32 \_ SessionDirectoryServer**](win32-sessiondirectoryserver.md)
</dt> </dl>

 

