---
title: Direntry-Struktur
description: Enthält eine eindeutige Ordinalzahl, die eine einzelne Schriftart in der Schriftarten Ressourcengruppe identifiziert. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: 4afc561e-bc98-4968-9a00-5002870b0c5e
keywords:
- Direntry-Struktur Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- DIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caed8f05a92abbeda39084b99b6806c2e28777a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742032"
---
# <a name="direntry-structure"></a>Direntry-Struktur

Enthält eine eindeutige Ordinalzahl, die eine einzelne Schriftart in der Schriftarten Ressourcengruppe identifiziert. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD fontOrdinal;
} DIRENTRY;
```



## <a name="members"></a>Member

<dl> <dt>

**fontorion**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Ein eindeutiger ordinalbezeichner für eine einzelne Schriftart in einer Schriftart Ressourcengruppe.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [**fontdirentry**](fontdirentry.md) -Struktur für die angegebene Schriftart folgt direkt der **direntry** -Struktur für diese Schriftart.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Fontdirentry**](fontdirentry.md)
</dt> <dt>

[**Fontgrouphdr**](fontgrouphdr.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Ressourcen](resources.md)
</dt> </dl>

 

 





