---
title: Extern. selecteditemid
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. selecteditemid
ms.assetid: 150aaa38-d4fe-493e-bda1-e5b0a27fccf7
keywords:
- Extern. selecteditemid-Fenster Media Player
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
ms.openlocfilehash: 768387c9e20082ef47cb0f502a2c4572bf462f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369544"
---
# <a name="externalselecteditemid"></a>Extern. selecteditemid

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **selecteditemid** -Eigenschaft ruft den Bezeichner des Medien Elements ab, das derzeit in Windows Media Player ausgewählt ist.

## <a name="syntax"></a>Syntax

``` syntax
window.external.selectedItemID
```

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird in Kombination mit der Eigenschaft [extern. selecteditemtype](external-selecteditemtype.md) verwendet. Wenn **selecteditemtype** beispielsweise cptrackid entspricht, ist **selecteditemid** die ID des ausgewählten Titels. Weitere Informationen zur kennzeichnen von Ansichten von Online Store-Inhalten durch Windows Media Player finden Sie unter [Standort und ausgewähltes Element](location-and-selected-item.md).

Bestimmte Sichten in Windows Media Player ein bestimmtes Medien Element, das ausgewählt ist. Nehmen wir beispielsweise an, dass die aktuelle Ansicht ein Album darstellt. Ein Album ist ein Container von Spuren, weshalb **selecteditemtype** gleich cptrackid und **selecteditemid** die ID des ausgewählten Titels ist. Andere Sichten verfügen über kein ausgewähltes Medien Element. Wenn der Benutzer z. b. auf den Stamm Knoten des Online Stores im Strukturansicht-Steuerelement klickt, zeigt Windows Media Player eine vom Online Store bereitgestellte Ermittlungs Seite an. Der Player zeigt in der Benutzeroberfläche des Players keinen Container von Medien Elementen an. In diesem Fall ist **selecteditemtype** gleich unknownlocation, und **selecteditemid** ist gleich der leeren Zeichenfolge.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Extern. selecteditemtype**](external-selecteditemtype.md)
</dt> <dt>

[**Speicherort und ausgewähltes Element**](location-and-selected-item.md)
</dt> </dl>

 

 





