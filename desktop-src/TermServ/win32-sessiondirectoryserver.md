---
title: Win32_SessionDirectoryServer-Klasse
description: Stellt Eigenschaften zum Anzeigen der Eigenschaften eines Remotedesktopverbindung Broker-Servers (RD-Verbindungsbroker) zur Seite.
ms.assetid: 73017b71-eff9-4ef6-aba0-71ddb969491f
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryServer-Remotedesktopdienste
- Win32_SessionDirectoryServer klasse Remotedesktopdienste , beschrieben
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
ms.openlocfilehash: 702b56a9cf8aee2ab38ad9d6b3a0f2d270b2128ea46934cc1beb720c77400d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127070"
---
# <a name="win32_sessiondirectoryserver-class"></a>Win32 \_ SessionDirectoryServer-Klasse

Stellt Eigenschaften zum Anzeigen der Eigenschaften eines Remotedesktopverbindung Broker-Servers (RD-Verbindungsbroker) zur Seite.

> [!Note]  
> In Windows Server 2008 R2 wurde der Name von Terminal Services Session Broker (TS Session Broker) in RD-Verbindungsbroker geändert. Diese Eigenschaften gelten für alle unterstützten Betriebssysteme, sofern nicht anders angegeben.

 

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

Die **Win32 \_ SessionDirectoryServer-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ SessionDirectoryServer-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ClusterName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Name der Farm, die den Server enthält.

</dd> <dt>

**LoadIndicator**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine relative Zahl, die die RD-Sitzungshost Serverauslastung darstellt, wenn der Standardalgorithmus für den Lastenausgleich verwendet wird. Der *LoadIndicator-Eigenschaftswert* basiert auf der Anzahl der Sitzungen, der Anzahl ausstehender Umleitungsanforderungen und dem Servergewichtungswert.

</dd> <dt>

**NumberOfSessions**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Sitzungen auf dem RD-Verbindungsbrokerserver.

</dd> <dt>

**NumPendRedir**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl ausstehender Umleitungsanforderungen.

</dd> <dt>

**ServerIPAddress**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

IP-Adresse des RD-Verbindungsbrokerservers. Wenn der Server sowohl für IPv4- als auch für IPv6-Adressen konfiguriert ist, enthält dieser die IPv4-Adresse.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Name des RD-Verbindungsbrokerservers.

</dd> <dt>

**ServerWeight**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Servergewichtungswert, der beim Lastenausgleich verwendet wird.

</dd> <dt>

**SingleSessionMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Einstellung für den Einzelsitzungsmodus des RD-Verbindungsbrokerservers.

<dt>

0
</dt> <dd>

Die Farm befindet sich nicht im Einzelsitzungsmodus.

</dd> <dt>

1
</dt> <dd>

Die Farm in befindet sich im Einzelsitzungsmodus.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Hinweise

Managed Object Format -Dateien (MOF) enthalten die Definitionen für Windows WMI-Klassen (Management Instrumentation). MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert. Sie werden auf dem Server installiert, wenn Sie die zugeordnete Rolle mithilfe der Server-Manager. Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ SessionDirectoryCluster**](win32-sessiondirectorycluster.md)
</dt> <dt>

[**Win32 \_ SessionDirectorySession**](win32-sessiondirectorysession.md)
</dt> </dl>

 

