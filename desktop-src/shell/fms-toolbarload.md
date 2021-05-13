---
description: Enthält Informationen zu benutzerdefinierten Schaltflächen, die der Symbolleiste des Datei-Managers hinzugefügt werden sollen. Die Schaltflächen werden von einer Dateierweiterungs-DLL bereitgestellt.
title: FMS_TOOLBARLOAD-Struktur (Wfext.h)
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
ms.openlocfilehash: 3a993312b9e365561018459c43dab87afbd3c2b2
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842161"
---
# <a name="fms_toolbarload-structure"></a>FMS \_ TOOLBARLOAD-Struktur

Enthält Informationen zu benutzerdefinierten Schaltflächen, die der Symbolleiste des Datei-Managers hinzugefügt werden sollen. Die Schaltflächen werden von einer Dateierweiterungs-DLL bereitgestellt.

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

Die Größe der -Struktur in Bytes. Der Datei-Manager legt die Größe fest, bevor die Erweiterung aufgerufen wird, und überprüft die Größe, nachdem die Erweiterungsprozedur zurückgegeben wurde.

</dd> <dt>

**lpButtons**
</dt> <dd>

Typ: **LPEXT \_ BUTTON**

</dd> <dd>

Die Adresse eines Arrays von [**EXT \_ BUTTON-Strukturen.**](ext-button.md)

</dd> <dt>

**cButtons**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Anzahl der [**EXT \_ BUTTON-Strukturen**](ext-button.md) im Array, auf die der **lpButtons-Member** zeigt. Diese Zahl entspricht der Anzahl der Schaltflächen und Trennzeichen, die der Symbolleiste hinzugefügt werden sollen.

</dd> <dt>

**cBitmaps**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Anzahl von Schaltflächen, die durch die angegebene Bitmap dargestellt werden.

</dd> <dt>

**idBitmap**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Der Bezeichner einer Bitmapressource in der ausführbaren Datei für die Erweiterungs-DLL. Die Bitmapressource enthält Bilder für die Anzahl von Schaltflächen, die von **cBitmaps angegeben werden.** Der Datei-Manager lädt die Bitmapressource und verwendet sie dann, um die Schaltflächen anzuzeigen.

</dd> <dt>

**hBitmap**
</dt> <dd>

Typ: **HBITMAP**

</dd> <dd>

Ein Handle für eine Bitmap, die der Datei-Manager verwendet, um Schaltflächenbilder zu erhalten und anzuzeigen, wenn **idBitmap** 0 ist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FMEVENT \_ TOOLBARLOAD**](fmevent-toolbarload.md)
</dt> </dl>

 

 




