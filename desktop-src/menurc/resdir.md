---
title: Resdir-Struktur
description: Enthält Informationen zu einem einzelnen Symbol oder einer Cursor Komponente in einer Ressourcengruppe. Es gibt eine resdir-Struktur für jede Gruppen Komponente. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\introductiontoresources\resourcereference\resourcestructures\resdir.htm
keywords:
- Resdir-Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- RESDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b854a4af3367131f6a559e1fef5899fae8b81107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337303"
---
# <a name="resdir-structure"></a>Resdir-Struktur

Enthält Informationen zu einem einzelnen Symbol oder einer Cursor Komponente in einer Ressourcengruppe. Es gibt eine **resdir** -Struktur für jede Gruppen Komponente. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  ICONRESDIR Icon;
  CURSORDIR  Cursor;
  CURSORDIR  Planes;
  CURSORDIR  BitCount;
  CURSORDIR  BytesInRes;
  CURSORDIR  IconCursorId;
} RESDIR;
```



## <a name="members"></a>Member

<dl> <dt>

**Symbol:**
</dt> <dd>

Typ: **[ **iconresdir**](iconresdir.md)**

</dd> <dd>

Die Breite, Höhe und Farbzahl des Symbols.

</dd> <dt>

**Cursor**
</dt> <dd>

Typ: **[ **Cursor dir**](cursordir.md)**

</dd> <dd>

Die Breite und Höhe des Mauszeigers.

</dd> <dt>

**Back**
</dt> <dd>

Typ: **[ **Cursor dir**](cursordir.md)**

</dd> <dd>

Die Anzahl von Farbebenen in der Symbol-oder Cursor Bitmap.

</dd> <dt>

**BitCount**
</dt> <dd>

Typ: **[ **Cursor dir**](cursordir.md)**

</dd> <dd>

Die Anzahl der Bits pro Pixel in der Symbol-oder Cursor Bitmap.

</dd> <dt>

**Bytesinres**
</dt> <dd>

Typ: **[ **Cursor dir**](cursordir.md)**

</dd> <dd>

Die Größe der Ressource in Bytes.

</dd> <dt>

**Iconcurrd**
</dt> <dd>

Typ: **[ **Cursor dir**](cursordir.md)**

</dd> <dd>

Das Symbol oder der Cursor mit einem eindeutigen ordinalbezeichner.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine oder mehrere **resdir** -Strukturen folgen direkt der Struktur " [**netwheader**](newheader.md) " in der RES-Datei. Der **rescount** -Member der Struktur " **netwheader** " gibt die Anzahl der **resdir** -Strukturen an. Beachten Sie, dass die **resdir** -Struktur entweder aus einer [**iconresdir**](iconresdir.md) -Struktur oder aus einer [**Cursor dir**](cursordir.md) -Struktur besteht, gefolgt **von den** Membern, **bitCount**, **bytesinres** und **iconcurrsorid** . Wenn die **resdir** -Strukturinformationen über einen Cursor enthält, sind die ersten beiden **Wörter**, die der Ressourcen Compiler in die [RT- \_ Cursor](/windows/desktop/menurc/resource-types) Ressource schreibt, die **xhotspot** -und **yhotspot** -Elemente der [**localheader**](localheader.md) -Struktur.

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

[**Iconresdir**](iconresdir.md)
</dt> <dt>

[**Localheader**](localheader.md)
</dt> <dt>

[**"Nwheader"**](newheader.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

