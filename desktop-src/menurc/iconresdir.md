---
title: Iconresdir-Struktur
description: Enthält die Dimensionen und das Farb Format eines einzelnen Symbol Bilds in einer Ressourcengruppe. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: 4c727369-2e90-40ad-85af-96d7e060b97a
keywords:
- Iconresdir-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- ICONRESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: de3d15bf250685e0b0cad935cd5e8094b2f2ceee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338343"
---
# <a name="iconresdir-structure"></a>Iconresdir-Struktur

Enthält die Dimensionen und das Farb Format eines einzelnen Symbol Bilds in einer Ressourcengruppe. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  BYTE Width;
  BYTE Height;
  BYTE ColorCount;
  BYTE reserved;
} ICONRESDIR;
```



## <a name="members"></a>Member

<dl> <dt>

**Width**
</dt> <dd>

Type: **Byte**

</dd> <dd>

Die Breite des Symbols in Pixel. Zulässige Werte sind 16, 32 und 64.

</dd> <dt>

**Height**
</dt> <dd>

Type: **Byte**

</dd> <dd>

Die Höhe des Symbols in Pixel. Zulässige Werte sind 16, 32 und 64.

</dd> <dt>

**Colorcount**
</dt> <dd>

Type: **Byte**

</dd> <dd>

Die Anzahl der Farben im Symbol. Zulässige Werte sind 2, 8 und 16.

</dd> <dt>

**bleiben**
</dt> <dd>

Type: **Byte**

</dd> <dd>

Bleiben muss auf denselben Wert festgelegt werden wie der des reservierten Felds im Header der Symbol Datei.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **iconresdir** -Struktur wird in der [**resdir**](resdir.md) -Struktur übermittelt, wenn die **resdir** -Struktur ein Symbol beschreibt.

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

 

 





