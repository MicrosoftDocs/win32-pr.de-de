---
title: Win32_RDSHServer-Klasse
description: Verwaltet einen Remotedesktop-Sitzungshost -Server (RDSH).
ms.assetid: 2c2840d2-16aa-484a-979b-6dbb1a08bbcf
ms.tgt_platform: multiple
keywords:
- Win32_RDSHServer der Remotedesktopdienste
- Win32_RDSHServer klasse Remotedesktopdienste , beschrieben
topic_type:
- apiref
api_name:
- Win32_RDSHServer
- Win32_RDSHServer.Name
- Win32_RDSHServer.ConnectionBroker
- Win32_RDSHServer.CollectionAlias
- Win32_RDSHServer.ServerState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066cea4044330ab79122e9346f6f32999202f854245e5508448e40aea3521fe0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422600"
---
# <a name="win32_rdshserver-class"></a>Win32 \_ RDSHServer-Klasse

Verwaltet einen Remotedesktop-Sitzungshost -Server (RDSH).

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHServer
{
  string Name;
  string ConnectionBroker;
  string CollectionAlias;
  uint32 ServerState;
};
```

## <a name="members"></a>Member

Die **Win32 \_ RDSHServer-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ RDSHServer-Klasse** verfügt über diese Methoden.



| Methode                                                                          | Beschreibung                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetInt32Property**](getint32property-win32-rdshserver.md)                   | Ruft einen ganzzahligen Eigenschaftswert eines **Win32 \_ RDSHServer-Objekts** ab.<br/>                                                                                                 |
| [**GetPendingStartServerList**](win32-rdshserver-getpendingstartserverlist.md) | Ruft eine Liste der Server ab, die auf den Start warten.<br/>                                                                                                                           |
| [**GetStringProperty**](getstringproperty-win32-rdshserver.md)                 | Ruft einen Zeichenfolgeneigenschaftswert eines **Win32 \_ RDSHServer-Objekts** ab.<br/>                                                                                                   |
| [**SetInt32Property**](setint32property-win32-rdshserver.md)                   | Aktualisiert einen ganzzahligen Eigenschaftswert eines **Win32 \_ RDSHServer-Objekts.**<br/>                                                                                                   |
| [**SetStringProperty**](setstringproperty-win32-rdshserver.md)                 | Aktualisiert einen Zeichenfolgeneigenschaftswert eines **Win32 \_ RDSHServer-Objekts.**<br/>                                                                                                     |
| [**TestAndSetState**](win32-rdshserver-testandsetstate.md)                     | Vergleicht den aktuellen Zustand mit dem angegebenen Vergleich. Wenn die beiden übereinstimmen, wird der Zustand auf einen neuen Wert festgelegt. Unabhängig von der Übereinstimmung wird auch der aktuelle Zustand zurückgegeben.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ RDSHServer-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CollectionAlias**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ruft den Alias für die RDSH-Auflistung ab, der der RDSH-Server zugewiesen ist, und legt diesen fest.

</dd> <dt>

**ConnectionBroker**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft den Namen des RDCB (Remotedesktopverbindung Broker) ab, der den Benutzerzugriff auf den RDSH-Server verwaltet, und legt diesen fest.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den Namen des RDSH-Servers ab und legt den Namen fest.

</dd> <dt>

**ServerState**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Beschreibt den Status des Servers. Jeder andere Wert als **TARGET \_ RUNNING** (3) ist reserviert und sollte als ungültiger Zustand betrachtet werden.

Die möglichen Werte sind.

<dt>

<span id="TARGET_UNKNOWN"></span><span id="target_unknown"></span>

**TARGET \_ UNKNOWN** (1)


</dt> <dd></dd> <dt>

<span id="TARGET_RUNNING"></span><span id="target_running"></span>

**TARGET \_ RUNNING** (3)


</dt> <dd></dd> <dt>

<span id="TARGET_INVALID"></span><span id="target_invalid"></span>

**TARGET \_ UNGÜLTIG** (8)


</dt> <dd></dd> <dt>

<span id="TARGET_STARTING"></span><span id="target_starting"></span>

**TARGET \_ STARTING** (9)


</dt> <dd></dd> <dt>

<span id="TARGET_STOPPING"></span><span id="target_stopping"></span>

**TARGET \_ WIRD BEENDET** (10)


</dt> <dd></dd> </dl>

**Windows Server 2012 R2 und Windows Server 2012:** Diese Eigenschaft ist vor der Windows Server 2016.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | Root \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Remotedesktop Management Services Provider](rdms-api-reference.md)
</dt> </dl>

 

