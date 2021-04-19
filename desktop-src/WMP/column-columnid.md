---
title: Column. ColumnID
description: Das ColumnID-Attribut gibt eine Spalten-ID im Wiedergabelisten-Steuerelement an oder ruft diese ab.
ms.assetid: c7b51f0b-e347-46be-a26d-aaa0bce83e0c
keywords:
- Column. ColumnID-Fenster Media Player
topic_type:
- apiref
api_name:
- COLUMN.columnID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4bc9aa6485443ae17486616b030b903a911a8e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352021"
---
# <a name="columncolumnid"></a>Column. ColumnID

Das **ColumnID** -Attribut gibt eine Spalten-ID im **Wiedergabe** Listen-Steuerelement an oder ruft diese ab.

``` syntax
        elementID.columnID
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Bei den **ColumnID** -Werten handelt es sich um dieselben Werte, die mit der **getiteminfo** -Methode für ein **Medien** Objekt verwendet werden. Eine Liste kann mithilfe der *Medien* abgerufen werden. **AttributeCount** -Eigenschaft, um die Anzahl der für ein bestimmtes **Medien** Objekt verfügbaren Attribute zu bestimmen. Index Nummern können dann mit den *Medien* verwendet werden. die **GetAttributeName** -Methode, um die Namen der Attribute zu bestimmen, die wiederum an *Medien* übermittelt werden können. **getiteminfo**. Die **ColumnID** -Eigenschaft kann nur auf diese Werte festgelegt werden, mit Ausnahme einiger Werte, die möglicherweise nicht von *Medien* zurückgegeben werden. **GetAttributeName**. Diese Werte sind unten aufgeführt.



| Wert     | BESCHREIBUNG                                                                        |
|-----------|------------------------------------------------------------------------------------|
| name      | Zeigt den Namen des **Medien** Objekts an.                                         |
| duration  | Zeigt die Dauer des **Medien** Objekts an.                                     |
| SourceURL | Zeigt die URL des **Medien** Objekts an.                                          |
| status    | Zeigt den Status zum Kopieren von Dateien an.                                              |
| Größe      | Zeigt die Größe der Datei an, die das **Medien** Objekt darstellt.                |
| Erweiterung | Zeigt die Dateinamenerweiterung der Datei an, die das **Medien** Objekt darstellt. |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Column-Element**](column-element.md)
</dt> <dt>

[**Medienobjekt**](media-object.md)
</dt> <dt>

[**Media. AttributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. GetAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media. getiteminfo**](media-getiteminfo.md)
</dt> </dl>

 

 





