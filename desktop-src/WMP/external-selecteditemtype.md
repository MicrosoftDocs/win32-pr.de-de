---
title: External.selectedItemType
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | External.selectedItemType
ms.assetid: f566e41e-127b-4596-99e6-bb07fc97249e
keywords:
- External.selectedItemType Windows Media Player
topic_type:
- apiref
api_name:
- External.selectedItemType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb58b13f1486bb30a79cd20e2f43f715df694f661c7b56e5eadd29f0c5c06c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648416"
---
# <a name="externalselecteditemtype"></a>External.selectedItemType

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **selectedItemType-Eigenschaft** ruft den Typ des Medienelements ab, das derzeit in der Windows Media Player.

## <a name="syntax"></a>Syntax

window.external.selectedItemType()

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge,** die eine der [Bibliotheksspeicherortkonst constants enthält.](library-location-constants.md)

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird in Kombination mit der **External.selectedItemID-Eigenschaft** verwendet. Wenn z. B. **selectedItemType** gleich CPTrackID ist, ist **selectedItemID** die ID der ausgewählten Spur. Weitere Informationen dazu, wie Windows Media Player Ansichten von Onlineshopinhalten kennzeichnet, finden Sie unter [Speicherort und Ausgewähltes Element.](location-and-selected-item.md)

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

[**External.selectedItemID**](external-selecteditemid.md)
</dt> <dt>

[**Speicherort und ausgewähltes Element**](location-and-selected-item.md)
</dt> </dl>

 

 





