---
description: Die LockIT-Klasse ist eine interne Klasse, die den DMO sperrt und entsperrt.
ms.assetid: f516ce22-17ad-488e-a768-3f3849c56087
title: 'Imediaobjectimpl:: LockIT-Klasse (dmuimpl. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24fe896ea293ec5e60b038f908cab794274d26e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356390"
---
# <a name="imediaobjectimpllockit-class"></a>Imediaobjectimpl:: LockIT-Klasse

Bei der `LockIt` -Klasse handelt es sich um eine interne Klasse, die den DMO sperrt und entsperrt.

``` syntax
LockIt(
    _DERIVED_ *p
);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="p"></span><span id="P"></span>*cker*
</dt> <dd>

Zeiger auf das abgeleitete Objekt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der `LockIt` Konstruktor sperrt den DMO, und der Dekonstruktor entsperrt den DMO. Um das Objekt in der abgeleiteten Klasse zu sperren, deklarieren Sie eine lokale Variable vom Typ `LockIt` . Der DMO ist gesperrt, während das `LockIt` Objekt im Gültigkeitsbereich bleibt:


```C++
void SomeMethod()
{
    // The DMO is not locked.
    {
        LockIt dmoLock(this); // Locks the DMO.
        /* ... */
    } 
    // dmoLock goes out of scope, DMO is unlocked.
}
```



Die Methoden in **imediaobjectimpl** sperren den DMO automatisch.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Dmuimpl. h</dt> </dl>                                                                     |
| Bibliothek<br/> | <dl> <dt>Dmuguids. lib; </dt> <dt>Msdmo. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imediaobjectimpl-Klassen Vorlage**](imediaobjectimpl-class-template.md)
</dt> </dl>

 

 




