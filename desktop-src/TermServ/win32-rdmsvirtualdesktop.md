---
title: Win32_RDMSVirtualDesktop-Klasse
description: Stellt einen virtuellen Desktop dar.
ms.assetid: e2952ec0-38d0-4a1c-b423-3ae1fbc701b3
ms.tgt_platform: multiple
keywords:
- Win32_RDMSVirtualDesktop-Klasse Remotedesktopdienste
- Win32_RDMSVirtualDesktop Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop
- Win32_RDMSVirtualDesktop.Name
- Win32_RDMSVirtualDesktop.HostName
- Win32_RDMSVirtualDesktop.Status
- Win32_RDMSVirtualDesktop.CollectionAlias
- Win32_RDMSVirtualDesktop.SessionState
- Win32_RDMSVirtualDesktop.SessionUserName
- Win32_RDMSVirtualDesktop.UserName
- Win32_RDMSVirtualDesktop.UserDomain
- Win32_RDMSVirtualDesktop.VMState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 247c49c7ad069b4feff3469ac21ec803ebc9f741
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337732"
---
# <a name="win32_rdmsvirtualdesktop-class"></a>Win32 \_ rdmsvirtualdesktop-Klasse

Stellt einen virtuellen Desktop dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktop
{
  string Name;
  string HostName;
  uint32 Status;
  string CollectionAlias;
  string SessionState;
  string SessionUserName;
  string UserName;
  string UserDomain;
  uint32 VMState;
};
```

## <a name="members"></a>Member

Die **Win32 \_ rdmsvirtualdesktop-** Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ rdmsvirtualdesktop-** Klasse verfügt über diese Methoden.



| Methode                                                                                              | BESCHREIBUNG                                                                                            |
|:----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------|
| [**Getuserzuweisung**](getuserassignment-win32-rdmsvirtualdesktop.md)                             | Ruft den Benutzernamen und den Domänen Namen des Benutzers ab, der dem virtuellen Desktop zugewiesen ist.<br/> |
| [**Getvirtualdesktopassignetdtouser**](getvirtualdesktopassignedtouser-win32-rdmsvirtualdesktop.md) | Ruft den virtuellen Desktop ab, der dem angegebenen Benutzer zugewiesen ist.<br/>                       |
| [**Getvirtualdesktopdetails**](getvirtualdesktopdetails-win32-rdmsvirtualdesktop.md)               | Ruft die zusätzlichen Informationen zum virtuellen Desktop ab.<br/>                             |
| [**Getvirtualdesktopstate**](getvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | Ruft den Zustand des virtuellen Desktops ab.<br/>                                                 |
| [**Removeuserzuweisung**](removeuserassignment-win32-rdmsvirtualdesktop.md)                       | Entfernt die Benutzer Zuweisung vom virtuellen Desktop.<br/>                                       |
| [**Setuserzuweisung**](setuserassignment-win32-rdmsvirtualdesktop.md)                             | Weist einem Benutzer einen virtuellen Desktop zu.<br/>                                                        |
| [**Setvirtualdesktopstate**](setvirtualdesktopstate-win32-rdmsvirtualdesktop.md)                   | Aktualisiert den Zustand des virtuellen Desktops.<br/>                                                   |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ rdmsvirtualdesktop-** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Collectionalias**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ruft den Alias der virtuellen Desktop Sammlung ab, die den virtuellen Computer verwaltet.

</dd> <dt>

**HostName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Namen des Computers ab, auf dem der virtuelle Computer gehostet wird.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ruft den Namen des virtuellen Computers ab.

</dd> <dt>

**SessionState**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ruft den Status der virtuellen Desktop Sitzung ab.

</dd> <dt>

**Sessionusername**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ruft den Benutzernamen des Benutzers ab, der bei der virtuellen Desktop Sitzung angemeldet ist.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Status des virtuellen Computers ab.

</dd> <dt>

**UserDomain**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ruft den Domänen Namen des Benutzers ab, der dem virtuellen Desktop zugewiesen ist.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ruft den Benutzernamen des Benutzers ab, der dem virtuellen Desktop zugewiesen ist.

</dd> <dt>

**VMState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ruft den Zustand des virtuellen Desktops ab.

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

 

