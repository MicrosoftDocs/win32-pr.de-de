---
description: Enthält den Index eines Eintrags und seine TAG-Informationen in einer Shimdatenbank.
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TAGID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4c65183170c7304bf05a670b1eadb3a5953d6f33b1f6415210f12db8898760
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075783"
---
# <a name="tagid"></a>TAGID

Enthält den Index eines Eintrags und seine TAG-Informationen in einer Shimdatenbank.


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a>Hinweise

Eine **TAGID** ist spezifisch für eine Datenbank. Dies kann ein ganzzahliger Wert sein, der den Index darstellt, oder einer der folgenden Werte:

<dl> <dt>

<span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID \_ NULL (0)
</dt> <dd>

Die **TAGID** ist nicht vorhanden. Dieser Wert wird von einer Funktion zurückgegeben, wenn er keine gültige **TAGID** zurückgeben kann.

</dd> <dt>

<span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>TAGID \_ ROOT (0)
</dt> <dd>

Gibt ein Stammlisten-TAG an, das als übergeordnetes Element verwendet werden kann, um eine untergeordnete **TAGID** abzurufen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Etikett**](tag.md)
</dt> <dt>

[TAG-Typen](tag-types.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




