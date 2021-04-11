---
title: Win32_SessionDirectoryServer-Klasse
description: Stellt Eigenschaften zum Anzeigen der Eigenschaften eines Remotedesktopverbindung Broker-Servers (RD-Verbindungsbroker) bereit.
ms.assetid: 73017b71-eff9-4ef6-aba0-71ddb969491f
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryServer-Klasse Remotedesktopdienste
- Win32_SessionDirectoryServer Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryServer
- Win32_SessionDirectoryServer.ServerName
- Win32_SessionDirectoryServer.ServerIPAddress
- Win32_SessionDirectoryServer.ClusterName
- Win32_SessionDirectoryServer.NumberOfSessions
- Win32_SessionDirectoryServer.SingleSessionMode
- Win32_SessionDirectoryServer.ServerWeight
- Win32_SessionDirectoryServer.NumPendRedir
- Win32_SessionDirectoryServer.LoadIndicator
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9e96efb19e4db56e582cd44d05f3e9865e5282c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949735"
---
# <a name="win32_sessiondirectoryserver-class"></a>Win32 \_ sessiondirectoryserver-Klasse

Stellt Eigenschaften zum Anzeigen der Eigenschaften eines Remotedesktopverbindung Broker-Servers (RD-Verbindungsbroker) bereit.

> [!Note]  
> In Windows Server 2008 R2 wurde der Name des Terminal Dienste-Sitzungs Brokers (TS-Sitzungs Broker) in "RD-Verbindungsbroker" geändert. Diese Eigenschaften gelten für alle unterstützten Betriebssysteme, sofern nicht anders angegeben.

 

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSERVER_Prov"), AMENDMENT]
class Win32_SessionDirectoryServer
{
  string ServerName;
  string ServerIPAddress;
  string ClusterName;
  uint32 NumberOfSessions;
  uint32 SingleSessionMode;
  uint32 ServerWeight;
  uint32 NumPendRedir;
  uint32 LoadIndicator;
};
```

## <a name="members"></a>Member

Die Win32-Klasse " **\_ sessiondirectoryserver** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die Win32-Klasse " **\_ sessiondirectoryserver** " verfügt über diese Eigenschaften.

<dl> <dt>

**ClusterName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Name der Farm, in der der Server enthalten ist.

</dd> <dt>

**Loadindicator**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine relative Zahl, die die RD-Sitzungshost Serverlast darstellt, wenn der standardmäßige Lasten Ausgleichs Algorithmus verwendet wird. Der *loadindicator* -Eigenschafts Wert basiert auf der Anzahl der Sitzungen, der Anzahl ausstehender Umleitungs Anforderungen und dem Server Gewichtungswert.

</dd> <dt>

**Anzahl von Sitzungen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Sitzungen auf dem RD-Verbindungsbroker Server.

</dd> <dt>

**Numloydredir**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der ausstehenden Umleitungs Anforderungen.

</dd> <dt>

**ServerIPAddress**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die IP-Adresse des RD-Verbindungsbroker Servers. Wenn der Server sowohl für IPv4-als auch für IPv6-Adressen konfiguriert ist, enthält dieser die IPv4-Adresse.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der Name des RD-Verbindungsbroker Servers.

</dd> <dt>

**Serverweight**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Server Gewichtungswert, der beim Lastenausgleich verwendet wird.

</dd> <dt>

**Singlesessionmode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Einstellung für den einzelsitzungmodus des RD-Verbindungsbroker Servers.

<dt>

0
</dt> <dd>

Die Farm befindet sich nicht im Einzel Sitzungs Modus.

</dd> <dt>

1
</dt> <dd>

Die Farm in befindet sich im Einzel Sitzungs Modus.

</dd> </dl>

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

[**Win32 \_ sessiondirectoriysession**](win32-sessiondirectorysession.md)
</dt> </dl>

 

