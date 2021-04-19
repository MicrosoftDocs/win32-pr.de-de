---
title: Player. mediacollectionattributestringchanged-Ereignis
description: Das mediacollectionattributestringchanged-Ereignis tritt auf, wenn ein Attribut Wert in der Bibliothek geändert wird. | Player. mediacollectionattributestringchanged-Ereignis
ms.assetid: 9bc81cf2-50a9-41cf-8eff-25c9395dfdac
keywords:
- Media Player für mediacollectionattributestringchanged-Ereignisfenster
- Mediacollectionattributestringchanged-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, mediacollectionattributestringchanged-Ereignis
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
ms.openlocfilehash: f92eba7f0f585b9bbff7a8eb52ab13ec0d74aaa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360347"
---
# <a name="playermediacollectionattributestringchanged-event"></a>Player. mediacollectionattributestringchanged-Ereignis

Das **mediacollectionattributestringchanged** -Ereignis tritt auf, wenn ein Attribut Wert in der Bibliothek geändert wird.

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

*bstrattribname* 
</dt> <dd>

**Zeichenfolge** , die den Namen des Attributs angibt. Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.

</dd> <dt>

*bstroldattribval* 
</dt> <dd>

Eine **Zeichenfolge** , die den alten Wert des Attributs angibt.

</dd> <dt>

*bstraunetwattribval* 
</dt> <dd>

Eine **Zeichenfolge** , die den neuen Wert des Attributs angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieses Ereignis gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn ein Benutzer Bibliotheks Metadaten ändert, wird das **mediacollection** -Objekt aktualisiert, und dieses Ereignis wird für jedes geänderte Attribut ausgelöst.

Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich. Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.

**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Mediacollection-Objekt**](mediacollection-object.md)
</dt> <dt>

[**Player-Objekt**](player-object.md)
</dt> <dt>

[**Player. mediacollection**](player-mediacollection.md)
</dt> </dl>

 

 





