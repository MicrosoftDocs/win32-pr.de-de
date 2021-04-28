---
description: 'TAGREF: Enthält den Index eines Eintrags und seine TAG-Informationen in einer Shimdatenbank.'
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e27a60847630e7bbd8e07ccf005dfd7b474d7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096628"
---
# <a name="tagref"></a>TAGREF

Enthält den Index eines Eintrags und seine TAG-Informationen in einer Shimdatenbank.


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a>Bemerkungen

Ein **TAGREF** ist spezifisch für eine Shimdatenbank und für mehrere Datenbanken gültig. Dies kann ein ganzzahliger Wert sein, der den Index darstellt, oder einer der folgenden Werte:

<dl> <dt>

<span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ NULL (0)
</dt> <dd>

Das **TAGREF** ist nicht vorhanden. Dieser Wert wird von einer Funktion zurückgegeben, wenn er kein gültiges **TAGREF** zurückgeben kann.

</dd> <dt>

<span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF \_ ROOT (0)
</dt> <dd>

Gibt ein Stammlisten-TAG an, das als übergeordnetes Element verwendet werden kann, um ein untergeordnetes **TAGREF** abzurufen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SdbTagRefToTagID**](sdbtagreftotagid.md)
</dt> <dt>

[**Etikett**](tag.md)
</dt> <dt>

[TAG-Typen](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> </dl>

 

 




