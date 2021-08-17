---
description: 'TAGREF: Enthält den Index eines Eintrags und seine TAG-Informationen in einer Shimdatenbank.'
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf5a9de8da025e8278ab0bca7ccbe16d70d16b782591181f6ce6ce74a010a39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075775"
---
# <a name="tagref"></a>TAGREF

Enthält den Index eines Eintrags und seine TAG-Informationen in einer Shimdatenbank.


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a>Hinweise

Ein **TAGREF** ist spezifisch für eine Shimdatenbank und für mehrere Datenbanken gültig. Dies kann ein ganzzahliger Wert sein, der den Index darstellt, oder einer der folgenden Werte:

<dl> <dt>

<span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ NULL (0)
</dt> <dd>

Das **TAGREF** ist nicht vorhanden. Dieser Wert wird von einer Funktion zurückgegeben, wenn er kein gültiges **TAGREF** zurückgeben kann.

</dd> <dt>

<span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF \_ ROOT (0)
</dt> <dd>

Gibt ein Tag der Stammliste an, das als übergeordnetes Element verwendet werden kann, um ein untergeordnetes **TAGREF** abzurufen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



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

 

 




