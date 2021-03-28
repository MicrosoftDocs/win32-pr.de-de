---
description: Enthält Informationen, die der Datei-Manager zum Hinzufügen eines benutzerdefinierten Menüs verwendet, das von einer Datei-Manager-Erweiterungs-DLL Die Struktur bietet auch einen Delta Wert, den die Erweiterungs-DLL verwenden kann, um das benutzerdefinierte Menü zu bearbeiten, nachdem der Datei-Manager das Menü geladen hat.
title: FMS_LOAD-Struktur (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0e76bcc5-76c2-4ec0-8ddb-4042cb5ffa7d
ms.openlocfilehash: 1745c4e34ac124e9990602350db6479ce287be8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977088"
---
# <a name="fms_load-structure"></a>Struktur zum \_ Laden von Strukturen

Enthält Informationen, die der Datei-Manager zum Hinzufügen eines benutzerdefinierten Menüs verwendet, das von einer Datei-Manager-Erweiterungs-DLL Die Struktur bietet auch einen Delta Wert, den die Erweiterungs-DLL verwenden kann, um das benutzerdefinierte Menü zu bearbeiten, nachdem der Datei-Manager das Menü geladen hat.

## <a name="syntax"></a>Syntax


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a>Member

<dl> <dt>

**dwSize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Länge der-Struktur in Bytes.

</dd> <dt>

**szmenuname**
</dt> <dd>

Typ: **TCHAR \[ - \_ Menü \_ Text \] len**

</dd> <dd>

Ein mit NULL endender Name für ein Menü Element, das in der Menüleiste im Datei-Manager angezeigt wird.

</dd> <dt>

**HMENU**
</dt> <dd>

Typ: **HMENU**

</dd> <dd>

Der Bezeichner des Popup Menüs, das der Menüleiste im Datei-Manager hinzugefügt wird.

</dd> <dt>

**wmenudelta**
</dt> <dd>

Typ: **uint**

</dd> <dd>

Der Delta Wert des Menü Elements. Um Konflikte mit den eigenen Menü Elementen zu vermeiden, benennt der Datei-Manager die Menü Element Bezeichner in dem Popup Menü um, das durch den **HMENU** -Member identifiziert wird, indem dieser Delta Wert den einzelnen Bezeichnern hinzugefügt wird. Eine Erweiterungs-DLL, die ein Menü Element ändern muss, muss das Element identifizieren, indem der Delta Wert dem Bezeichner des Menü Elements hinzugefügt wird. Der Wert dieses Members kann von Sitzung zu Sitzung abweichen.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WF. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**"F"**](fmextensionproc.md)
</dt> </dl>

 

 




