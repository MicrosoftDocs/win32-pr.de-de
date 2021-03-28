---
description: Enthält Informationen über benutzerdefinierte Schaltflächen, die der Datei-Manager-Symbolleiste hinzugefügt werden. Die Schaltflächen werden von einer Datei-Manager-Erweiterungs-DLL bereitgestellt.
title: FMS_TOOLBARLOAD-Struktur (WF. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 7185f9e5-10c6-43cc-b85b-cd077378338f
ms.openlocfilehash: 8e123c759a827adddf5fd00eaf33193ebca0dbf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979696"
---
# <a name="fms_toolbarload-structure"></a>Struktur von "f. \_ toolbarload"

Enthält Informationen über benutzerdefinierte Schaltflächen, die der Datei-Manager-Symbolleiste hinzugefügt werden. Die Schaltflächen werden von einer Datei-Manager-Erweiterungs-DLL bereitgestellt.

## <a name="syntax"></a>Syntax


```C++
typedef struct _FMS_TOOLBARLOAD {
  DWORD        dwSize;
  LPEXT_BUTTON lpButtons;
  WORD         cButtons;
  WORD         cBitmaps;
  WORD         idBitmap;
  HBITMAP      hBitmap;
} FMS_TOOLBARLOAD;
```



## <a name="members"></a>Member

<dl> <dt>

**dwSize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Größe der-Struktur in Bytes. Der Datei-Manager legt die Größe vor dem Aufrufen der Erweiterung fest und überprüft die Größe nach der Rückgabe der Erweiterungs Prozedur.

</dd> <dt>

**lpButtons**
</dt> <dd>

Typ: **lpext- \_ Schaltfläche**

</dd> <dd>

Die Adresse eines Arrays von [**Ext- \_ Schalt**](ext-button.md) Flächen Strukturen.

</dd> <dt>

**cbuttons**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Anzahl der [**Ext- \_ Schalt**](ext-button.md) Flächen Strukturen im Array, auf die durch den **lpButtons** -Member verwiesen wird. Diese Zahl entspricht der Anzahl von Schaltflächen und Trennzeichen, die der Symbolleiste hinzugefügt werden sollen.

</dd> <dt>

**cbitmaps**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Anzahl der Schaltflächen, die durch die angegebene Bitmap dargestellt werden.

</dd> <dt>

**idbitmap**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Der Bezeichner einer Bitmap-Ressource in der ausführbaren Datei für die Erweiterungs-DLL. Die Bitmap-Ressource enthält Bilder für die Anzahl von Schaltflächen, die von **cbitmaps** angegeben werden. Der Datei-Manager lädt die Bitmap-Ressource und verwendet diese dann zum Anzeigen der Schaltflächen.

</dd> <dt>

**HBITMAP**
</dt> <dd>

Typ: **hBitmap**

</dd> <dd>

Ein Handle für eine Bitmap, die der Datei-Manager zum Abrufen und Anzeigen von Schaltflächen Bildern verwendet, wenn **idbitmap** den Wert 0 hat.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WF. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**"Tool barload" von "f" \_**](fmevent-toolbarload.md)
</dt> </dl>

 

 




