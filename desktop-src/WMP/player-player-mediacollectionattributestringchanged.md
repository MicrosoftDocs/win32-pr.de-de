---
title: Player.MediaCollectionAttributeStringChanged-Ereignis
description: Das MediaCollectionAttributeStringChanged-Ereignis tritt auf, wenn ein Attributwert in der Bibliothek geändert wird. | Player.MediaCollectionAttributeStringChanged-Ereignis
ms.assetid: 9bc81cf2-50a9-41cf-8eff-25c9395dfdac
keywords:
- MediaCollectionAttributeStringChanged-Ereignis Windows Media Player
- MediaCollectionAttributeStringChanged-Ereignis Windows Media Player , Player-Klasse
- Player-Klasse Windows Media Player , MediaCollectionAttributeStringChanged-Ereignis
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringChanged
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9435be90761abf88927789fad4380172f0ef6f31427848195d3aa14ea4112cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747396"
---
# <a name="playermediacollectionattributestringchanged-event"></a>Player.MediaCollectionAttributeStringChanged-Ereignis

Das **MediaCollectionAttributeStringChanged-Ereignis** tritt auf, wenn ein Attributwert in der Bibliothek geändert wird.

## <a name="syntax"></a>Syntax


```JScript
Player.MediaCollectionAttributeStringChanged(
  bstrAttribName,
  bstrOldAttribVal,
  bstrNewAttribVal
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrAttribName* 
</dt> <dd>

**Eine Zeichenfolge,** die den Namen des Attributs angibt. Informationen zu den attributes, die von Windows Media Player unterstützt werden, finden Sie in der Windows Media Player [Attribute Reference](attribute-reference.md).

</dd> <dt>

*bstrOldAttribVal* 
</dt> <dd>

**Eine Zeichenfolge,** die den alten Wert des Attributs angibt.

</dd> <dt>

*bstrNewAttribVal* 
</dt> <dd>

**Eine Zeichenfolge,** die den neuen Wert des Attributs angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn ein Benutzer Bibliotheksmetadaten ändert, wird das **MediaCollection-Objekt** aktualisiert, und dieses Ereignis wird für jedes geänderte Attribut angezeigt.

Der Wert von Ereignisparametern wird von Windows Media Player angegeben und kann mithilfe des angegebenen Parameternamens auf eine Methode in einer importierten JScript-Datei zugegriffen oder an diese übergeben werden. Dieser Parametername muss genau wie gezeigt typisieren, einschließlich Groß- und Groß-/Schreibanforderungen.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MediaCollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player.mediaCollection**](player-mediacollection.md)
</dt> </dl>

 

 





