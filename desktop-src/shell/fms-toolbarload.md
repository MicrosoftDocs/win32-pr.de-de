---
description: Enthält Informationen zu benutzerdefinierten Schaltflächen, die der Datei-Manager-Symbolleiste hinzugefügt werden sollen. Die Schaltflächen werden von einer Datei-Manager-Erweiterungs-DLL bereitgestellt.
title: FMS_TOOLBARLOAD -Struktur (Wfext.h)
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
ms.openlocfilehash: 719e13e824778ec133ad761d09ccd3bd8f5846ae8cdb36c83ba4f85eca1c2408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224109"
---
# <a name="fms_toolbarload-structure"></a>\_FMS-SYMBOLLEISTELOAD-Struktur

Enthält Informationen zu benutzerdefinierten Schaltflächen, die der Datei-Manager-Symbolleiste hinzugefügt werden sollen. Die Schaltflächen werden von einer Datei-Manager-Erweiterungs-DLL bereitgestellt.

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

Die Größe der -Struktur in Bytes. Der Datei-Manager legt die Größe vor dem Aufruf der Erweiterung fest und überprüft die Größe, nachdem die Erweiterungsprozedur zurückgegeben wurde.

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

Die Anzahl der [**EXT \_ BUTTON-Strukturen**](ext-button.md) im Array, auf die das **lpButtons-Member zeigt.** Diese Zahl entspricht der Anzahl von Schaltflächen und Trennzeichen, die der Symbolleiste hinzugefügt werden.

</dd> <dt>

**cBitmaps**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Anzahl der Schaltflächen, die von der angegebenen Bitmap dargestellt werden.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FMEVENT \_ TOOLBARLOAD**](fmevent-toolbarload.md)
</dt> </dl>

 

 




