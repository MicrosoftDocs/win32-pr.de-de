---
title: Localheader-Struktur
description: Enthält die x-und y-Koordinaten eines Hotspots, der mit dem durch eine resdir-Struktur identifizierten Cursor verknüpft ist. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: 8cf74040-8b8f-447e-a881-1bcf05b151e2
keywords:
- Localheader-Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- LOCALHEADER
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7aa2ee51e1a9e456398a42d8190781b5dbec8d14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392007"
---
# <a name="localheader-structure"></a>Localheader-Struktur

Enthält die x-und y-Koordinaten eines Hotspots, der mit dem durch eine [**resdir**](resdir.md) -Struktur identifizierten Cursor verknüpft ist. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD xHotSpot;
  WORD yHotSpot;
} LOCALHEADER;
```



## <a name="members"></a>Member

<dl> <dt>

**xhotspot**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die x-Koordinate der Cursorposition in Pixel.

</dd> <dt>

**yhotspot**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die y-Koordinate der Cursorposition in Pixel.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **localheader** -Struktur ist die erste Daten, die in die [RT- \_ Cursor](/windows/desktop/menurc/resource-types) Ressource geschrieben werden, wenn eine [**resdir**](resdir.md) -Strukturinformationen über einen Cursor enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Cursor Verzeichnis**](cursordir.md)
</dt> <dt>

[**Resdir**](resdir.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

