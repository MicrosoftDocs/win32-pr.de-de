---
title: Win32_RDSHServer-Klasse
description: Verwaltet einen Remotedesktop-Sitzungshost Server (RDSH).
ms.assetid: 2c2840d2-16aa-484a-979b-6dbb1a08bbcf
ms.tgt_platform: multiple
keywords:
- Win32_RDSHServer-Klasse Remotedesktopdienste
- Win32_RDSHServer Klasse Remotedesktopdienste, beschrieben
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
ms.openlocfilehash: 6434a4dfe6bc1a79fdaf4576a89ef552cebd5e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340718"
---
# <a name="win32_rdshserver-class"></a>Win32 \_ rdshserver-Klasse

Verwaltet einen Remotedesktop-Sitzungshost Server (RDSH).

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

Die **Win32 \_ rdshserver** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ rdshserver** -Klasse verfügt über diese Methoden.



| Methode                                                                          | BESCHREIBUNG                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetInt32Property**](getint32property-win32-rdshserver.md)                   | Ruft einen ganzzahligen Eigenschafts Wert eines **Win32- \_ rdshserver** -Objekts ab.<br/>                                                                                                 |
| [**Getpdingstartserverlist**](win32-rdshserver-getpendingstartserverlist.md) | Ruft eine Liste der Server ab, die auf den Start warten.<br/>                                                                                                                           |
| [**GetStringProperty**](getstringproperty-win32-rdshserver.md)                 | Ruft den Wert der Zeichen folgen Eigenschaft eines **Win32- \_ rdshserver** -Objekts ab.<br/>                                                                                                   |
| [**SetInt32Property**](setint32property-win32-rdshserver.md)                   | Aktualisiert einen ganzzahligen Eigenschafts Wert eines **Win32- \_ rdshserver** -Objekts.<br/>                                                                                                   |
| [**SetStringProperty**](setstringproperty-win32-rdshserver.md)                 | Aktualisiert den Wert der Zeichen folgen Eigenschaft eines **Win32- \_ rdshserver** -Objekts.<br/>                                                                                                     |
| [**Testandsetstate**](win32-rdshserver-testandsetstate.md)                     | Vergleicht den aktuellen Zustand mit dem angegebenen comparand. Wenn die beiden Stimmen, wird der Zustand auf einen neuen Wert festgelegt. Unabhängig von der Übereinstimmung wird der aktuelle Zustand ebenfalls zurückgegeben.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ rdshserver** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Collectionalias**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ruft den Alias für die RDSH-Auflistung ab, der der RDSH-Server zugewiesen ist, oder legt ihn fest.

</dd> <dt>

**Connectionbroker**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ruft den Namen des Remotedesktopverbindung Brokers (RDCB) ab, der den Benutzer Zugriff auf den RDSH-Server verwaltet, oder legt ihn fest.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den Namen des RDSH-Servers ab, oder legt ihn fest.

</dd> <dt>

**ServerState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Beschreibt den Status des Servers. Alle anderen Werte als das Ziel, das ausgeführt wird (3), sind reserviert und sollten einen ungültigen Status **\_ aufweisen** .

Mögliche Werte sind.

<dt>

<span id="TARGET_UNKNOWN"></span><span id="target_unknown"></span>

**Ziel \_ Unbekannt** (1)


</dt> <dd></dd> <dt>

<span id="TARGET_RUNNING"></span><span id="target_running"></span>

**Ziel \_ Wird ausgeführt** (3)


</dt> <dd></dd> <dt>

<span id="TARGET_INVALID"></span><span id="target_invalid"></span>

**Ziel \_ Ungültig** (8)


</dt> <dd></dd> <dt>

<span id="TARGET_STARTING"></span><span id="target_starting"></span>

**Ziel \_ Wird gestartet** (9)


</dt> <dd></dd> <dt>

<span id="TARGET_STOPPING"></span><span id="target_stopping"></span>

**Ziel \_ Wird beendet (10** )


</dt> <dd></dd> </dl>

**Windows Server 2012 R2 und Windows Server 2012:** Diese Eigenschaft ist vor Windows Server 2016 nicht verfügbar.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | Root \\ CIMV2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop Management Services-Anbieter](rdms-api-reference.md)
</dt> </dl>

 

