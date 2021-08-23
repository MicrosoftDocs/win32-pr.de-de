---
title: External.libraryLocationType
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | External.libraryLocationType
ms.assetid: aaf20147-8331-40bd-a5cd-5ee9b8e2d022
keywords:
- External.libraryLocationType Windows Media Player
topic_type:
- apiref
api_name:
- External.libraryLocationType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54e254ce6258cf667884e2815508b413ed1455b1b6924bfebb4edc900da048c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736200"
---
# <a name="externallibrarylocationtype"></a>External.libraryLocationType

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **libraryLocationType-Eigenschaft** ruft eine Bibliotheksspeicherort-Konstante [ab,](library-location-constants.md) die den Typ der aktuellen Ansicht in der Windows Media Player.

``` syntax
window.external.libraryLocationType
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge,** die eine der Speicherortkonst constants der Bibliothek enthält.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft funktioniert in Kombination mit der [External.libraryLocationID-Eigenschaft.](external-librarylocationid.md) Angenommen, **libraryLocationType** ist gleich CP CpuID und **libraryLocationID** gleich 3. Das bedeutet, dass die aktuelle Ansicht in Windows Media Player das Album mit der ID 3 zeigt. Weitere Informationen dazu, wie Windows Media Player Ansichten von Onlineshopinhalten kennzeichnet, finden Sie unter [Speicherort und Ausgewähltes Element.](location-and-selected-item.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Externes Objekt für Onlinespeicher vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.libraryLocationID**](external-librarylocationid.md)
</dt> <dt>

[**Speicherort und ausgewähltes Element**](location-and-selected-item.md)
</dt> </dl>

 

 





