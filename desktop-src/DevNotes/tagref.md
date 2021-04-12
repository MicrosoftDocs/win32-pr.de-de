---
description: Enthält den Index eines Eintrags und seine Taginformationen in einer Shimdatenbank.
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: Tagref
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8631811f101850b68bdbad1097c19b9a41737bd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523152"
---
# <a name="tagref"></a>Tagref

Enthält den Index eines Eintrags und seine Taginformationen in einer Shimdatenbank.


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a>Bemerkungen

Eine **tagref** ist für eine Shimdatenbank spezifisch und über mehrere Datenbanken hinweg gültig. Dabei kann es sich um einen ganzzahligen Wert handeln, der den Index darstellt, oder um einen der folgenden Werte:

<dl> <dt>

<span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>Tagref \_ NULL (0)
</dt> <dd>

**Tagref** ist nicht vorhanden. Dieser Wert wird von einer Funktion zurückgegeben, wenn kein gültiger **tagref**-Wert zurückgegeben werden kann.

</dd> <dt>

<span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>Tagref-Stamm \_ (0)
</dt> <dd>

Gibt ein Stamm Listen-Tag an, das als übergeordnetes Element verwendet werden kann, um ein untergeordnetes **tagref** zu erhalten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbtagrebtotagid**](sdbtagreftotagid.md)
</dt> <dt>

[**Tag**](tag.md)
</dt> <dt>

[Tagtypen](tag-types.md)
</dt> <dt>

[**TagID**](tagid.md)
</dt> </dl>

 

 




