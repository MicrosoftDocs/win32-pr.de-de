---
title: Player.MediaCollectionAttributeStringAdded-Ereignis
description: Das MediaCollectionAttributeStringAdded-Ereignis tritt auf, wenn der Bibliothek ein Attributwert hinzugefügt wird. | Player.MediaCollectionAttributeStringAdded-Ereignis
ms.assetid: 0a7fd61f-0429-4c1c-8790-d2f0e7f41d44
keywords:
- MediaCollectionAttributeStringAdded-Ereignis Windows Media Player
- MediaCollectionAttributeStringAdded-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , MediaCollectionAttributeStringAdded-Ereignis
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d01bd86cb3004cb3f481222f392ba47bd1c47373f55c37ee8f0e7ded57a3d268
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995870"
---
# <a name="playermediacollectionattributestringadded-event"></a>Player.MediaCollectionAttributeStringAdded-Ereignis

Das **MediaCollectionAttributeStringAdded-Ereignis** tritt auf, wenn der Bibliothek ein Attributwert hinzugefügt wird.

## <a name="syntax"></a>Syntax


```JScript
Player.MediaCollectionAttributeStringAdded(
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

Wenn der Bibliothek ein Medienelement hinzugefügt wird, werden dessen Metadaten dem **MediaCollection-Objekt** hinzugefügt, und dieses Ereignis wird für jedes hinzugefügte Attribut ausgelöst.

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens in einer importierten JScript-Datei auf eine Methode zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt eingegeben werden, einschließlich Der Groß-/Großschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MediaCollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player.mediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





