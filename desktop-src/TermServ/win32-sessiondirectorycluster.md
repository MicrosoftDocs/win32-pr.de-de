---
title: Win32_SessionDirectoryCluster-Klasse
description: Stellt Eigenschaften zum Anzeigen der Eigenschaften einer Farm in Remotedesktopverbindung Broker (RD-Verbindungsbroker) bereit.
ms.assetid: a4a924fd-88ea-46db-968e-378c3dc46cfc
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryCluster-Klassen-Remotedesktopdienste
- Win32_SessionDirectoryCluster-Klasse Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryCluster
- Win32_SessionDirectoryCluster.ClusterName
- Win32_SessionDirectoryCluster.NumberOfServers
- Win32_SessionDirectoryCluster.SingleSessionMode
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f1dba262ddb332f03c7f398c4f205e73a9c9e94054d4164fb94c8c01dc8b505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127080"
---
# <a name="win32_sessiondirectorycluster-class"></a>Win32 \_ SessionDirectoryCluster-Klasse

Stellt Eigenschaften zum Anzeigen der Eigenschaften einer Farm in Remotedesktopverbindung Broker (RD-Verbindungsbroker) bereit.

> [!Note]  
> In Windows Server 2008 R2 wurde der Name von Terminal Services Session Broker (TS Session Broker) in RD-Verbindungsbroker geändert. Diese Eigenschaften gelten für alle unterstützten Betriebssysteme, sofern nicht anders angegeben.

 

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYCLUSTER_Prov"), AMENDMENT]
class Win32_SessionDirectoryCluster
{
  string ClusterName;
  uint32 NumberOfServers;
  uint32 SingleSessionMode;
};
```

## <a name="members"></a>Member

Die **Win32 \_ SessionDirectoryCluster-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ SessionDirectoryCluster-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ClusterName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Name der Farm im RD-Verbindungsbroker.

</dd> <dt>

**NumberOfServers**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anzahl der Server in der Farm im RD-Verbindungsbroker.

</dd> <dt>

**SingleSessionMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Einzelsitzungsmodus der Farm im RD-Verbindungsbroker.

<dt>

0
</dt> <dd>

Die Farm im RD-Verbindungsbroker befindet sich nicht im Einzelsitzungsmodus.

</dd> <dt>

1
</dt> <dd>

Die Farm im RD-Verbindungsbroker befindet sich im Einzelsitzungsmodus.

</dd> </dl>

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ SessionDirectoryServer**](win32-sessiondirectoryserver.md)
</dt> <dt>

[**Win32 \_ SessionDirectorySession**](win32-sessiondirectorysession.md)
</dt> </dl>

 

