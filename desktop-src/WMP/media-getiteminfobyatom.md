---
title: Media.getItemInfoByAtom-Methode
description: Die getItemInfoByAtom-Methode ruft den Wert des Attributs mit der angegebenen Indexnummer ab.
ms.assetid: 6e2dea0c-c722-4737-9e8e-f5cb74156cea
keywords:
- getItemInfoByAtom-Methode Windows Media Player
- getItemInfoByAtom-Methode Windows Media Player , Media-Klasse
- Medienklasse Windows Media Player , getItemInfoByAtom-Methode
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
ms.openlocfilehash: 26db8e87a52c0d8c8236b5e4b8b5e7325fb3bb0a995dcbd81da668ea760df660
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135133"
---
# <a name="mediagetiteminfobyatom-method"></a>Media.getItemInfoByAtom-Methode

Die **getItemInfoByAtom-Methode** ruft den Wert des Attributs mit der angegebenen Indexnummer ab.

## <a name="syntax"></a>Syntax


```JScript
strRetVal = Media.getItemInfoByAtom(
  index
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Index* \[ In\]
</dt> <dd>

**Number** (**long**), die den Index angibt, an dem sich ein bestimmtes Attribut innerhalb des Satzes verfügbarer Attribute befindet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt eine **Zeichenfolge** zurück, die den Wert des angegebenen Attributs darstellt. Für Attribute, deren zugrunde liegender Wert **boolesch** ist, wird die Zeichenfolge "true" oder "false" zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode kann verwendet werden, um Metadaten für ein bestimmtes digitales Medienelement mithilfe einer Attributindexnummer abzurufen. Die **attributeCount-Eigenschaft** kann verwendet werden, um die Anzahl der für das Medienelement verfügbaren Attribute zu bestimmen.

Die **getMediaAtom-Methode** des **MediaCollection-Objekts** kann auch verwendet werden, um den Index eines bestimmten Attributs abzurufen. Diese Technik ist im Allgemeinen effizienter als die **getItemInfo-** oder **getItemInfoByType-Methoden** bei der Arbeit mit großen Wiedergabelisten.

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

Informationen zu den attributen, die von Windows Media Player unterstützt werden, finden Sie unter Windows Media Player [Attributverweis.](attribute-reference.md)

**Windows Media Player 10 Mobile:** Attribute für ein Medienelement sind nur während der Wiedergabe verfügbar, es sei denn, sie werden über die Medienauflistung aus dem Element abgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Media.attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media.getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Media.getItemInfoByType**](media-getiteminfobytype.md)
</dt> <dt>

[**Media.setItemInfo**](media-setiteminfo.md)
</dt> <dt>

[**MediaCollection.getMediaAtom**](mediacollection-getmediaatom.md)
</dt> <dt>

[**Lesen von Attributwerten**](reading-attribute-values.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





