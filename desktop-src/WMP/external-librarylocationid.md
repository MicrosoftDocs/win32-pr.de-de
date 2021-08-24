---
title: External.libraryLocationID
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | External.libraryLocationID
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- External.libraryLocationID-Windows Media Player
topic_type:
- apiref
api_name:
- External.libraryLocationID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65119db42e8a4d6a06414f1c7790fb8716c0f9423391ed0a58f74a6913cb3b8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649130"
---
# <a name="externallibrarylocationid"></a>External.libraryLocationID

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **libraryLocationID-Eigenschaft** ruft den Bezeichner des jeweiligen Medienelements ab, das derzeit in der Ansicht des Players angezeigt wird.

``` syntax
window.external.libraryLocationID
      
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge.**

## <a name="remarks"></a>Hinweise

Diese Eigenschaft funktioniert in Kombination mit der [External.libraryLocationType-Eigenschaft.](external-librarylocationtype.md) Angenommen, **libraryLocationType** ist gleich CP CpuID und **libraryLocationID** gleich 3. Das bedeutet, dass die aktuelle Ansicht in Windows Media Player das Album mit der ID 3 zeigt. Weitere Informationen dazu, wie Windows Media Player Ansichten von Onlineshopinhalten kennzeichnet, finden Sie unter [Speicherort und Ausgewähltes Element.](location-and-selected-item.md)

Bestimmte Ansichten in Windows Media Player einem bestimmten Medienelement zugeordnet. Wenn die aktuelle Ansicht beispielsweise ein einzelnes Album darstellt, **ist libraryLocationType** gleich CP CpuID, und **libraryLocationID** ist die ID des Albums. Andere Ansichten sind mit einem bestimmten Medienelement nicht verknüpft. Wenn die aktuelle Ansicht z. B. alle Albums darstellt, **ist libraryLocationType** gleich AllCPTeriIDs, aber es gibt keinen sinnvollen Wert, der **libraryLocationID zugewiesen werden kann.** In Fällen, in denen **die libraryLocationID-Eigenschaft** keinen sinnvollen Wert hat, entspricht sie der leeren Zeichenfolge.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für Onlinespeicher vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**Speicherort und ausgewähltes Element**](location-and-selected-item.md)
</dt> </dl>

 

 





