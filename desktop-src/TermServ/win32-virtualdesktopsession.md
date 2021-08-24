---
title: Win32_VirtualDesktopSession-Klasse
description: Verwaltet eine virtuelle Desktopsitzung.
ms.assetid: a5a0d2a4-6e19-42ac-988c-2d3787946325
ms.tgt_platform: multiple
keywords:
- Win32_VirtualDesktopSession-Klassen-Remotedesktopdienste
- Win32_VirtualDesktopSession-Klasse Remotedesktopdienste beschrieben
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession.VMHostName
- Win32_VirtualDesktopSession.SessionId
- Win32_VirtualDesktopSession.VMName
- Win32_VirtualDesktopSession.ConnectState
- Win32_VirtualDesktopSession.UserName
- Win32_VirtualDesktopSession.DomainName
- Win32_VirtualDesktopSession.CollectionId
- Win32_VirtualDesktopSession.ClientMachineName
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e039df658ded4534e3e2582f08ba4e5f5a04530d810349fff5633730a84332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137423"
---
# <a name="win32_virtualdesktopsession-class"></a>Win32 \_ VirtualDesktopSession-Klasse

Verwaltet eine virtuelle Desktopsitzung.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_VirtualDesktopSession
{
  string VMHostName;
  uint32 SessionId;
  string VMName;
  uint32 ConnectState;
  string UserName;
  string DomainName;
  string CollectionId;
  string ClientMachineName;
};
```

## <a name="members"></a>Member

Die **Win32 \_ VirtualDesktopSession-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ VirtualDesktopSession-Klasse** verfügt über diese Methoden.



| Methode                                                         | BESCHREIBUNG                                                                |
|:---------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**Trennen**](disconnect-win32-virtualdesktopsession.md)   | Trennt die Sitzung des virtuellen Desktops.<br/>                        |
| [**Abmelden**](logoff-win32-virtualdesktopsession.md)           | Meldet den Benutzer von der Sitzung des virtuellen Desktops ab.<br/>             |
| [**SendMessage**](sendmessage-win32-virtualdesktopsession.md) | Senden Sie eine Nachricht über die Virtuelle Desktopsitzung an den Benutzer.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ VirtualDesktopSession-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ClientMachineName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Namen des Clientcomputers ab, der mit der Sitzung verbunden ist.

</dd> <dt>

**CollectionId**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Namen der virtuellen Desktopauflistung ab, die den virtuellen Computer hostet.

</dd> <dt>

**ConnectState**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zustand der Verbindung mit der Sitzung ab.

</dd> <dt>

**DomainName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Domänennamen des Benutzers ab.

</dd> <dt>

**SessionId**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft die ID der Sitzung des virtuellen Desktops ab.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Namen des Benutzerkontos ab, das der Sitzung zugewiesen ist.

</dd> <dt>

**VMHostName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den Namen des Remotedesktop Virtualisierungshostservers ab, der den virtuellen Computer hostet.

</dd> <dt>

**VMName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Namen des virtuellen Computers ab, der der Sitzung zugewiesen ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | Root \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Remotedesktop Management Services-Anbieter](rdms-api-reference.md)
</dt> </dl>

 

