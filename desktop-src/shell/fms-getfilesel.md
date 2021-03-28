---
description: Enthält Informationen zu einer ausgewählten Datei im aktiven Datei-Manager-Fenster (im Verzeichnis Fenster oder im Fenster "Suchergebnisse").
title: FMS_GETFILESEL-Struktur (WF. h)
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
ms.openlocfilehash: e7ae92350e88e050b1208eed6e08f8faba811fee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958644"
---
# <a name="fms_getfilesel-structure"></a>Fims \_ getfilesel-Struktur

Enthält Informationen zu einer ausgewählten Datei im aktiven Datei-Manager-Fenster (im Verzeichnis Fenster oder im Fenster "Suchergebnisse").

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

**fttime**
</dt> <dd>

Typ: **FILETIME**

</dd> <dd>

Das Datum und die Uhrzeit, zu der die Datei erstellt wurde.

</dd> <dt>

**dwSize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Größe der Datei in Bytes.

</dd> <dt>

**battr**
</dt> <dd>

Type: **Byte**

</dd> <dd>

Die Attribute der Datei.

</dd> <dt>

**szName**
</dt> <dd>

Typ: **TCHAR**

</dd> <dd>

Der durch Null beendete vollständige Pfad und Dateiname der ausgewählten Datei.

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

 

 




