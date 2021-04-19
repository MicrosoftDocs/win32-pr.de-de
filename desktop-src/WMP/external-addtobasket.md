---
title: Extern. adddebasket-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. adddebasket-Methode
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- adddebasket-Methode, Windows Media Player
- adddebasket-Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, adddebasket-Methode
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
ms.openlocfilehash: d2e2fab549dec9e24b0c5bbe61f5511e375c4c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361997"
---
# <a name="externaladdtobasket-method"></a>Extern. adddebasket-Methode

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **adddebasket** -Methode fügt dem Listen Bereich (auch als Warenkorb bezeichnet) in Windows Media Player Medienelemente hinzu.

## <a name="syntax"></a>Syntax


```JScript
External.addToBasket(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ViewType* \[ in\]
</dt> <dd>

Eine **Zeichenfolge** , die den Typ des Elements angibt, das dem Listen Bereich hinzugefügt wird. Der Aufrufer muss diesen Parameter auf eine der folgenden [Bibliotheks Speicherort Konstanten](library-location-constants.md)festlegen:

Cplistid

Cptrackid

Cpalbumid

Cpartist

Cpgenreid

Cpalbumsubgenreid

Cpradioid

</dd> <dt>

*Viewids* \[ in\]
</dt> <dd>

**Zeichenfolge** , die die durch Semikolons getrennten IDs der Elemente enthält, die dem Listen Bereich hinzugefügt werden sollen.

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

[**Externalobject für Typ 1 Online Stores**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Extern. baskettitle**](external-baskettitle.md)
</dt> </dl>

 

 





