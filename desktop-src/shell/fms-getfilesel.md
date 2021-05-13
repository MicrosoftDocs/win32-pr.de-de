---
description: Enthält Informationen zu einer ausgewählten Datei im aktiven Datei-Manager-Fenster (Verzeichnisfenster oder Suchergebnisfenster).
title: FMS_GETFILESEL -Struktur (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d8339f87-ba05-40bf-b7d1-a9de29eb15a4
ms.openlocfilehash: b1188840299a101081c5c29d0e5658963ca7a72e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842221"
---
# <a name="fms_getfilesel-structure"></a>FMS \_ GETFILESEL-Struktur

Enthält Informationen zu einer ausgewählten Datei im aktiven Datei-Manager-Fenster (Verzeichnisfenster oder Suchergebnisfenster).

## <a name="syntax"></a>Syntax


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a>Member

<dl> <dt>

**ftTime**
</dt> <dd>

Typ: **FILETIME**

</dd> <dd>

Die Uhrzeit und das Datum, zu dem die Datei erstellt wurde.

</dd> <dt>

**dwSize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Größe der Datei in Bytes.

</dd> <dt>

**bAttr**
</dt> <dd>

Typ: **BYTE**

</dd> <dd>

Die Attribute der Datei.

</dd> <dt>

**Szname**
</dt> <dd>

Typ: **TCHAR**

</dd> <dd>

Der auf NULL beendete vollständige Pfad und Dateiname der ausgewählten Datei.

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

 

 




