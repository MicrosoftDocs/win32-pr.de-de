---
description: Enthält den Index eines Eintrags und seine Taginformationen in einer Shimdatenbank.
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TagID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7d8b8a25633d3505936d105b0eef7ed38746ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958253"
---
# <a name="tagid"></a>TagID

Enthält den Index eines Eintrags und seine Taginformationen in einer Shimdatenbank.


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a>Bemerkungen

Eine **TagID** ist für eine Datenbank spezifisch. Dabei kann es sich um einen ganzzahligen Wert handeln, der den Index darstellt, oder um einen der folgenden Werte:

<dl> <dt>

<span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TagID \_ NULL (0)
</dt> <dd>

Die **TagID** ist nicht vorhanden. Dieser Wert wird von einer Funktion zurückgegeben, wenn keine gültige **TagID** zurückgegeben werden kann.

</dd> <dt>

<span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>TagID-Stamm \_ (0)
</dt> <dd>

Gibt ein Stamm Listen-Tag an, das als übergeordnetes Element zum Abrufen einer untergeordneten **TagID** verwendet werden kann.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Tag**](tag.md)
</dt> <dt>

[Tagtypen](tag-types.md)
</dt> <dt>

[**Tagref**](tagref.md)
</dt> </dl>

 

 




