---
title: Extern. selecteditemtype
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. selecteditemtype
ms.assetid: f566e41e-127b-4596-99e6-bb07fc97249e
keywords:
- Extern. selecteditemtype Windows Media Player
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
ms.openlocfilehash: 9755f66dd00947f295bdd40ea6ab79e69d655d49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352830"
---
# <a name="externalselecteditemtype"></a>Extern. selecteditemtype

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **selecteditemtype** -Eigenschaft ruft den Typ des Medien Elements ab, das derzeit in Windows Media Player ausgewählt ist.

## <a name="syntax"></a>Syntax

Window. extern. selecteditemtype ()

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge** , die eine der [Bibliotheks Speicherort Konstanten](library-location-constants.md)enthält.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird in Kombination mit der **externen. selecteditemid** -Eigenschaft verwendet. Wenn **selecteditemtype** beispielsweise cptrackid entspricht, ist **selecteditemid** die ID des ausgewählten Titels. Weitere Informationen zur kennzeichnen von Ansichten von Online Store-Inhalten durch Windows Media Player finden Sie unter [Standort und ausgewähltes Element](location-and-selected-item.md).

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

[**Extern. selecteditemid**](external-selecteditemid.md)
</dt> <dt>

[**Speicherort und ausgewähltes Element**](location-and-selected-item.md)
</dt> </dl>

 

 





