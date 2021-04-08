---
title: Zählelement-Objekt (isysmon. h)
description: Verwenden Sie diese Klasse, um den Pfad und den Wert eines Zählers abzurufen und die Farbe anzugeben, die zum Diagramm des Zählers verwendet wird. Um dieses Objekt abzurufen, rufen Sie Counters. Item auf.
ms.assetid: 76b69395-efd8-4321-b7ed-63daa46e2636
keywords:
- Initialisiererobjekt-sysmon
- Objekt-sysmon, beschrieben
topic_type:
- apiref
api_name:
- CounterItem
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df999e327591309f015d8720f61643625eced4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741913"
---
# <a name="counteritem-object"></a>"Count"-Objekt

Verwenden Sie diese Klasse, um den Pfad und den Wert eines Zählers abzurufen und die Farbe anzugeben, die zum Diagramm des Zählers verwendet wird.

Um dieses Objekt abzurufen, rufen Sie [**Counters. Item**](counters-item.md)auf.

## <a name="members"></a>Member

Das **ratteritem** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **ratteritem** -Objekt verfügt über diese Methoden.



| Methode                                             | BESCHREIBUNG                                                                    |
|:---------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Getdataat**](counteritem-getdataat.md)         | Ruft die Daten des Zählers von einem bestimmten Punkt im Liniendiagramm ab.<br/> |
| [**Getstatistics**](counteritem-getstatistics.md) | Ruft die durchschnittlichen, maximalen und minimalen Werte für den Zählers ab.<br/> |
| [**GetValue**](counteritem-getvalue.md)           | Ruft den letzten Wert des Zählers ab.<br/>                            |



 

### <a name="properties"></a>Eigenschaften

Das **ratteritem** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                  | BESCHREIBUNG                                                                     |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**Farbe**](counteritem-color.md)<br/>             | Ruft die Farbe ab oder legt Sie fest, die zum Diagramm des Leistungsindikators verwendet wird.<br/>         |
| [**LineStyle**](counteritem-linestyle.md)<br/>     | Ruft den Linienstil zum Diagramm des Leistungsindikators ab oder legt diesen fest.<br/>    |
| [**ADS**](counteritem-path.md)<br/>               | Ruft den Pfad des Zählers ab.<br/>                                   |
| [**ScaleFactor**](counteritem-scalefactor.md)<br/> | Ruft den Skalierungsfaktor ab, mit dem der indikatorenwert dargestellt wird, oder legt ihn fest<br/>  |
| [**Ausgewählt**](counteritem-selected.md)<br/>       | Ruft einen Wert ab, der angibt, ob der Leistungsindikators ausgewählt ist, oder legt ihn fest<br/> |
| [**Wert**](counteritem-value.md)<br/>             | Ruft den aktuellen Wert des Zählers ab.<br/>                          |
| [**Sichtbar**](counteritem-visible.md)<br/>         | Ruft einen Wert ab, der angibt, ob der Leistungsindikators grafisch dargestellt wird, oder legt ihn fest.<br/>  |
| [**Breite**](counteritem-width.md)<br/>             | Ruft die Linienbreite ab, die zum Diagramm des Leistungsindikators verwendet wird, oder legt diese fest<br/>    |



 

## <a name="remarks"></a>Bemerkungen

[**Value**](counteritem-value.md) ist die Standard Eigenschaft von **count** Item.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                            |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Sysmon-Klassen](sysmon-classes.md)
</dt> </dl>

 

 





