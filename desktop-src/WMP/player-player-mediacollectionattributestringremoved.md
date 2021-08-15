---
title: Player.MediaCollectionAttributeStringRemoved-Ereignis
description: Das MediaCollectionAttributeStringRemoved-Ereignis tritt auf, wenn ein Attributwert aus der Bibliothek entfernt wird. | Player.MediaCollectionAttributeStringRemoved-Ereignis
ms.assetid: f1253996-10d1-42fa-89f9-1e52ca830aea
keywords:
- MediaCollectionAttributeStringRemoved-Ereignis Windows Media Player
- MediaCollectionAttributeStringRemoved-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , MediaCollectionAttributeStringRemoved-Ereignis
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b89e46d4dbe86f185fb636b5c8de453e2addbf83c92d1231b5f067ce0b3b1d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747406"
---
# <a name="playermediacollectionattributestringremoved-event"></a>Player.MediaCollectionAttributeStringRemoved-Ereignis

Das **MediaCollectionAttributeStringRemoved-Ereignis** tritt auf, wenn ein Attributwert aus der Bibliothek entfernt wird.

## <a name="syntax"></a>Syntax


```JScript
Player.MediaCollectionAttributeStringRemoved(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrAttribName* 
</dt> <dd>

**Zeichenfolge,** die den Namen des Attributs angibt. Informationen zu den attributen, die von Windows Media Player unterstützt werden, finden Sie in der Windows Media Player [Attributreferenz.](attribute-reference.md)

</dd> <dt>

*bstrAttribVal* 
</dt> <dd>

**Zeichenfolge,** die den Wert des Attributs angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn ein Medienelement aus der Bibliothek entfernt wird, werden seine Metadaten aus dem **MediaCollection-Objekt** entfernt, und dieses Ereignis wird für jedes entfernte Attribut ausgelöst.

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens in einer importierten JScript-Datei auf eine Methode zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt eingegeben werden, einschließlich Der Groß-/Großschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MediaCollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player.mediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





