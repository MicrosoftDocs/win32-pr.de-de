---
title: Win32_SessionDirectorySession-Klasse
description: Stellt Eigenschaften zum Anzeigen der Eigenschaften einer Remotedesktopverbindung Broker-Sitzung (RD-Verbindungsbroker) bereit.
ms.assetid: 34b5a898-3952-493c-ba62-dd0d298b0600
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectorySession-Klasse Remotedesktopdienste
- Win32_SessionDirectorySession Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: fba8fdbdffc764c3bdcc1a8f5bc53aa479f318d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391657"
---
# <a name="win32_sessiondirectorysession-class"></a>Win32 \_ sessiondirectorysession-Klasse

Stellt Eigenschaften zum Anzeigen der Eigenschaften einer Remotedesktopverbindung Broker-Sitzung (RD-Verbindungsbroker) bereit.

> [!Note]  
> In Windows Server 2008 R2 wurde der Name des Terminal Dienste-Sitzungs Brokers (TS-Sitzungs Broker) in "RD-Verbindungsbroker" geändert. Diese Eigenschaften gelten für alle unterstützten Betriebssysteme, sofern nicht anders angegeben.

 

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

Die Win32-Klasse " **\_ sessiondirectorysession** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ sessiondirectorysession** " verfügt über diese Eigenschaften.

<dl> <dt>

**ApplicationType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anwendung wurde mit dieser Sitzung gestartet. Dies entspricht der **Start Program** -Eigenschaft von [**imstscsecuredsettings**](imstscsecuredsettings-interface.md).

</dd> <dt>

**ColorDepth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Farbtiefe der Sitzung, gemessen in Bits pro Pixel.

</dd> <dt>

**CreateTime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datum und Uhrzeit der Erstellung der Sitzung. Dieser Wert wird nicht zurückgesetzt, wenn eine Sitzung getrennt und die Verbindung wieder hergestellt wird.

</dd> <dt>

**Disconnecttime**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Datum und Uhrzeit, zu der die Sitzung getrennt wurde (falls zutreffend).

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Domänen Name des Benutzers, der bei dieser Sitzung angemeldet ist.

</dd> <dt>

**Resolutionheight**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Höhe der Sitzung in Pixel für diese Sitzung.

</dd> <dt>

**Resolutionwidth**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Breite der Sitzung in Pixel für diese Sitzung.

</dd> <dt>

**ServerIPAddress**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die IP-Adresse des RD-Verbindungsbroker Servers für diese Sitzung.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Name des RD-Verbindungsbroker Servers für diese Sitzung.

</dd> <dt>

**SessionID**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Sitzungs-ID für diese Sitzung.

</dd> <dt>

**SessionState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Status dieser Sitzung.

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

**Tsproycol**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Protokoll für diese Sitzung.

<dt>

0
</dt> <dd>

Diese Sitzung wird in einer physischen Konsole ausgeführt.

</dd> <dt>

1
</dt> <dd>

Für diese Sitzung wird ein proprietäres Protokoll von Drittanbietern verwendet.

</dd> <dt>

2
</dt> <dd>

Für diese Sitzung wird Remotedesktopprotokoll (RDP) verwendet.

</dd> </dl>

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Benutzername des Benutzers, der bei dieser Sitzung angemeldet ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen. MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>"Tssdwmi. mof"</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ sessiondirectoriycluster**](win32-sessiondirectorycluster.md)
</dt> <dt>

[**Win32 \_ sessiondirectoriyserver**](win32-sessiondirectoryserver.md)
</dt> </dl>

 

