---
title: External.selectedItemID
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | External.selectedItemID
ms.assetid: 150aaa38-d4fe-493e-bda1-e5b0a27fccf7
keywords:
- External.selectedItemID Windows Media Player
topic_type:
- apiref
api_name:
- External.selectedItemID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ea4b93656adc3fab25ab96e41fe417bde158035c5c11a0af9be84c5d555b153
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648430"
---
# <a name="externalselecteditemid"></a>External.selectedItemID

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **selectedItemID-Eigenschaft** ruft den Bezeichner des Medienelements ab, das derzeit in der Windows Media Player.

## <a name="syntax"></a>Syntax

``` syntax
window.external.selectedItemID
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge.**

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird in Kombination mit der [External.selectedItemType-Eigenschaft](external-selecteditemtype.md) verwendet. Wenn z. B. **selectedItemType** gleich CPTrackID ist, ist **selectedItemID** die ID der ausgewählten Spur. Weitere Informationen dazu, wie Windows Media Player Ansichten von Onlineshopinhalten kennzeichnet, finden Sie unter [Speicherort und Ausgewähltes Element.](location-and-selected-item.md)

Bestimmte Ansichten in Windows Media Player haben ein bestimmtes Medienelement, das ausgewählt ist. Angenommen, die aktuelle Ansicht stellt ein Album dar. Ein Album ist ein Container von Spuren, daher **ist selectedItemType** gleich CPTrackID, und **selectedItemID** ist die ID des ausgewählten Titels. Für andere Ansichten ist kein Medienelement ausgewählt. Wenn der Benutzer beispielsweise im Strukturansicht-Steuerelement auf den Stammknoten des Onlineshops klickt, zeigt Windows Media Player eine vom Onlineshop bereitgestellte Ermittlungsseite an. Der Player zeigt auf der Player-Benutzeroberfläche keinen Container mit Medienelementen an. In diesem Fall ist **selectedItemType** gleich UnknownLocation und **selectedItemID** gleich der leeren Zeichenfolge.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für Onlinespeicher vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.selectedItemType**](external-selecteditemtype.md)
</dt> <dt>

[**Speicherort und ausgewähltes Element**](location-and-selected-item.md)
</dt> </dl>

 

 





