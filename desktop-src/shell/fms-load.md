---
description: Enthält Informationen, die der Datei-Manager verwendet, um ein benutzerdefiniertes Menü hinzuzufügen, das von einer Datei-Manager-Erweiterungs-DLL bereitgestellt wird. Die -Struktur bietet auch einen Deltawert, den die Erweiterungs-DLL verwenden kann, um das benutzerdefinierte Menü zu bearbeiten, nachdem der Datei-Manager das Menü geladen hat.
title: FMS_LOAD -Struktur (Wfext.h)
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
ms.openlocfilehash: efd1777704c775db84c7dabf54b9e06c81535fb4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842191"
---
# <a name="fms_load-structure"></a>FMS \_ LOAD-Struktur

Enthält Informationen, die der Datei-Manager verwendet, um ein benutzerdefiniertes Menü hinzuzufügen, das von einer Datei-Manager-Erweiterungs-DLL bereitgestellt wird. Die -Struktur bietet auch einen Deltawert, den die Erweiterungs-DLL verwenden kann, um das benutzerdefinierte Menü zu bearbeiten, nachdem der Datei-Manager das Menü geladen hat.

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

Die Länge der -Struktur in Bytes.

</dd> <dt>

**szMenuName**
</dt> <dd>

Typ: **TCHAR \[ MENU TEXT \_ \_ LEN \]**

</dd> <dd>

Ein mit NULL beendeter Name für ein Menüelement, das in der Menüleiste im Datei-Manager angezeigt wird.

</dd> <dt>

**Hmenu**
</dt> <dd>

Typ: **HMENU**

</dd> <dd>

Der Bezeichner des Popupmenüs, das der Menüleiste im Datei-Manager hinzugefügt wurde.

</dd> <dt>

**wMenuDelta**
</dt> <dd>

Typ: **UINT**

</dd> <dd>

Der Deltawert des Menüelements. Um Konflikte mit eigenen Menüelementen zu vermeiden, nummeriert der Datei-Manager die Menüelementbezeichner im Popupmenü, das vom **hMenu-Element** identifiziert wird, neu, indem dieser Deltawert jedem Bezeichner hinzugefügt wird. Eine Erweiterungs-DLL, die ein Menüelement ändern muss, muss das Element identifizieren, indem der Deltawert dem Bezeichner des Menüelements hinzugefügt wird. Der Wert dieses Members kann von Sitzung zu Sitzung variieren.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




