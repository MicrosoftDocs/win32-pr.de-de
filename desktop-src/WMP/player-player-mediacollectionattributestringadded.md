---
title: Player. mediacollectionattributestringadded-Ereignis
description: Das mediacollectionattributestringadded-Ereignis tritt auf, wenn der Bibliothek ein Attribut Wert hinzugefügt wird. | Player. mediacollectionattributestringadded-Ereignis
ms.assetid: 0a7fd61f-0429-4c1c-8790-d2f0e7f41d44
keywords:
- Media Player für mediacollectionattributestringadded-Ereignisfenster
- Mediacollectionattributestringadded-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, mediacollectionattributestringadded-Ereignis
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
ms.openlocfilehash: 61ec30cf22b36fe97902d6eb6d6949daeb751f8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371285"
---
# <a name="playermediacollectionattributestringadded-event"></a>Player. mediacollectionattributestringadded-Ereignis

Das **mediacollectionattributestringadded** -Ereignis tritt auf, wenn der Bibliothek ein Attribut Wert hinzugefügt wird.

## <a name="syntax"></a>Syntax


```JScript
Player.MediaCollectionAttributeStringAdded(
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

Wenn der Bibliothek ein Medien Element hinzugefügt wird, werden die zugehörigen Metadaten dem **mediacollection** -Objekt hinzugefügt, und dieses Ereignis wird für jedes hinzugefügte Attribut ausgelöst.

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

 

 





