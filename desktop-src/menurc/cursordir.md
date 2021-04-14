---
title: Cursor dir-Struktur
description: Enthält die Dimensionen eines einzelnen Cursor Bilds in einer Ressourcengruppe. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: bc826fd6-74a2-470b-8d19-437cdeb0727d
keywords:
- Cursor-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- CURSORDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2434bdf90248c2f1d6c5edf9425f0f35d698cd45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392146"
---
# <a name="cursordir-structure"></a>Cursor dir-Struktur

Enthält die Dimensionen eines einzelnen Cursor Bilds in einer Ressourcengruppe. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD Width;
  WORD Height;
} CURSORDIR;
```



## <a name="members"></a>Member

<dl> <dt>

**Width**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Breite des Cursors in Pixel. Zulässige Werte sind 16, 32 und 64.

</dd> <dt>

**Height**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Höhe des Cursors in Pixel. Zulässige Werte sind 16, 32 und 64.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **cursordir** -Struktur wird in der [**resdir**](resdir.md) -Struktur übermittelt, wenn die **resdir** -Struktur einen Cursor beschreibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Resdir**](resdir.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

 





