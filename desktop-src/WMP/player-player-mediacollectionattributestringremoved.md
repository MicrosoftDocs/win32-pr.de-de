---
title: Player. mediacollectionattributestraningrebewegereignis
description: Das Ereignis mediacollectionattributestraningrebewegt tritt auf, wenn ein Attribut Wert aus der Bibliothek entfernt wird. | Player. mediacollectionattributestraningrebewegereignis
ms.assetid: f1253996-10d1-42fa-89f9-1e52ca830aea
keywords:
- Ereignisfenster für mediacollectionattributestraningrebewesfenster Media Player
- Mediacollectionattributestraningrebewegereignis-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player der Player-Klasse, mediacollectionattributestraningrebewegereignis
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
ms.openlocfilehash: b1b85dfd566c507f6ae5557134ac95544e42d688
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364038"
---
# <a name="playermediacollectionattributestringremoved-event"></a>Player. mediacollectionattributestraningrebewegereignis

Das Ereignis **mediacollectionattributestraningrebewegt** tritt auf, wenn ein Attribut Wert aus der Bibliothek entfernt wird.

## <a name="syntax"></a>Syntax


```JScript
Player.MediaCollectionAttributeStringRemoved(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrattribname* 
</dt> <dd>

**Zeichenfolge** , die den Namen des Attributs angibt. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.

</dd> <dt>

*bstrattribval* 
</dt> <dd>

Eine **Zeichenfolge** , die den Wert des Attributs angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn ein Medien Element aus der Bibliothek entfernt wird, werden die zugehörigen Metadaten aus dem **mediacollection** -Objekt entfernt, und dieses Ereignis wird für jedes entfernte Attribut ausgelöst.

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mediacollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player. mediacollection**](player-mediacollection.md)
</dt> </dl>

 

 





