---
title: Media. getiteminfobyatom-Methode
description: Die getiteminfobyatom-Methode ruft den Wert des Attributs mit der angegebenen Indexnummer ab.
ms.assetid: 6e2dea0c-c722-4737-9e8e-f5cb74156cea
keywords:
- getiteminfobyatom-Methode, Windows Media Player
- getiteminfobyatom-Methode, Windows Media Player, Medienklasse
- Medienklasse, Windows Media Player, getiteminfobyatom-Methode
topic_type:
- apiref
api_name:
- Media.getItemInfoByAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf54d2ae177a65e1a71b5726090bba90f4ee4e5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372462"
---
# <a name="mediagetiteminfobyatom-method"></a>Media. getiteminfobyatom-Methode

Die **getiteminfobyatom** -Methode ruft den Wert des Attributs mit der angegebenen Indexnummer ab.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = Media.getItemInfoByAtom(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ in\]
</dt> <dd>

**Number** (**Long**), der den Index angibt, an dem sich ein bestimmtes Attribut innerhalb des Satzes verfügbarer Attribute befindet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** zurück, die den Wert des angegebenen Attributs darstellt. Bei Attributen, deren zugrunde liegender Wert **boolescher** Wert ist, wird die Zeichenfolge "true" oder "false" zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode kann verwendet werden, um Metadaten für ein bestimmtes digitales Medien Element mithilfe einer Attribut Indexnummer abzurufen. Die **AttributeCount** -Eigenschaft kann verwendet werden, um die Anzahl der für das Medien Element verfügbaren Attribute zu bestimmen.

Die **getmediaatom** -Methode des **mediacollection** -Objekts kann auch verwendet werden, um den Index eines bestimmten Attributs abzurufen. Diese Technik ist im Allgemeinen effizienter als die **getiteminfo** -Methode oder die **getItemInfoByType** -Methode bei der Arbeit mit großen Wiedergabelisten.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

Informationen zu den Attributen, die von Windows Media Player unterstützt werden, finden Sie in der [Referenz](attribute-reference.md)zu Windows Media Player-Attributen.

**Windows Media Player 10 Mobile:** Attribute für ein Medien Element sind nur während der Wiedergabe verfügbar, es sei denn, Sie werden über die Medien Auflistung aus dem Element abgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Media. AttributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. getiteminfo**](media-getiteminfo.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**"Media. mentiteminfo"**](media-setiteminfo.md)
</dt> <dt>

[**Mediacollection. getmediaatom**](mediacollection-getmediaatom.md)
</dt> <dt>

[**Lesen von Attributwerten**](reading-attribute-values.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





