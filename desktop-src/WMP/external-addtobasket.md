---
title: External.addToBasket-Methode
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | External.addToBasket-Methode
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- addToBasket-Methode Windows Media Player
- addToBasket-Methode Windows Media Player , External-Klasse
- Externe Klasse Windows Media Player , addToBasket-Methode
topic_type:
- apiref
api_name:
- External.addToBasket
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17f51cfc3df641b02a5aa3a0869e810f318357dd70ba67acb3ec2310f8a5a355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650010"
---
# <a name="externaladdtobasket-method"></a>External.addToBasket-Methode

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **addToBasket-Methode** fügt medienbezogene Elemente zum Listenbereich (auch als Warenkorb bezeichnet) in Windows Media Player hinzu.

## <a name="syntax"></a>Syntax


```JScript
External.addToBasket(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ViewType* \[ In\]
</dt> <dd>

**Zeichenfolge,** die den Typ des Elements angibt, das dem Listenbereich hinzugefügt wird. Der Aufrufer muss diesen Parameter auf eine der folgenden [Speicherortkonstanten](library-location-constants.md)der Bibliothek festlegen:

CPListID

CPTrackID

CPIedID

CPArtist

CPGenreID

CPIedSubGenreID

CPRadioID

</dd> <dt>

*ViewIDs* \[ In\]
</dt> <dd>

**Zeichenfolge,** die die durch Semikolons getrennten IDs der Elemente enthält, die dem Listenbereich hinzugefügt werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ExternalObject für Onlineshops vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.basketTitle**](external-baskettitle.md)
</dt> </dl>

 

 





