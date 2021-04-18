---
title: Mediacollection-Objekt
description: Das mediacollection-Objekt bietet eine Möglichkeit, eine große Sammlung von Medien Elementen zu organisieren. Sie kann abgefragt werden, um Wiedergabelisten automatisch zu generieren.
ms.assetid: afcb2c51-3ecb-4529-8f3e-56aa6d0ec2b4
keywords:
- Mediacollection-Objekt, Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2232e3590acd371039494b31c5d592c2e00f0199
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341281"
---
# <a name="mediacollection-object"></a>Mediacollection-Objekt

Das **mediacollection** -Objekt bietet eine Möglichkeit, eine große Sammlung von Medien Elementen zu organisieren. Sie kann abgefragt werden, um Wiedergabelisten automatisch zu generieren.

Das **mediacollection** -Objekt unterstützt die folgenden Methoden.



| Methode                                                                           | BESCHREIBUNG                                                                                                                                                    |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [add](mediacollection-add.md)                                                   | Fügt der Bibliothek ein neues Medien Element oder eine neue Wiedergabeliste hinzu.                                                                                                              |
| [createQuery](mediacollection-createquery.md)                                   | Erstellt ein neues [Abfrage](query-object.md) Objekt.                                                                                                                |
| ["GetAll"](mediacollection-getall.md)                                             | Ruft ein [Wiedergabe](playlist-object.md) Listen Objekt ab, das alle Medienelemente in der Bibliothek enthält.                                                                  |
| [getAttributeStringCollection](mediacollection-getattributestringcollection.md) | Ruft ein [StringCollection](stringcollection-object.md) -Objekt ab, das den Satz aller Werte für ein angegebenes Attribut innerhalb eines angegebenen Medientyps darstellt. |
| [getbyalbum](mediacollection-getbyalbum.md)                                     | Ruft ein [Wiedergabe](playlist-object.md) Listen Objekt ab, das Medienelemente aus dem angegebenen Album enthält.                                                            |
| [getbyattribute](mediacollection-getbyattribute.md)                             | Ruft ein [Wiedergabe](playlist-object.md) Listen Objekt ab, das Medienelemente mit dem angegebenen-Wert mit dem angegebenen-Wert enthält.                             |
| [getbyattributeandmediatype](mediacollection-getbyattributeandmediatype.md)     | Ruft ein [Wiedergabe](playlist-object.md) Listen Objekt ab, das [Medien](media-object.md) Objekte mit dem angegebenen Attribut und Medientyp enthält.                 |
| [getbyauthor](mediacollection-getbyauthor.md)                                   | Ruft ein [Wiedergabe](playlist-object.md) Listen Objekt ab, das Medienelemente vom angegebenen Autor enthält.                                                             |
| [getByGenre](mediacollection-getbygenre.md)                                     | Ruft ein [Wiedergabe](playlist-object.md) Listen Objekt ab, das Medienelemente mit dem angegebenen Genre enthält.                                                            |
| [getByName](mediacollection-getbyname.md)                                       | Ruft ein [Wiedergabe](playlist-object.md) Listen Objekt ab, das Medienelemente mit dem angegebenen Namen enthält.                                                             |
| [getmediaatom](mediacollection-getmediaatom.md)                                 | Ruft den Index ab, an dem sich eine angegebene Eigenschaft innerhalb des Satzes verfügbarer Eigenschaften befindet.                                                              |
| [getplaylistbyquery](mediacollection-getplaylistbyquery.md)                     | Ruft ein [Wiedergabe](playlist-object.md) Listen Objekt ab, das [Media](media-object.md) -Objekte enthält, die den Abfragebedingungen entsprechen.                               |
| [getstringcollectionbyquery](mediacollection-getstringcollectionbyquery.md)     | Ruft ein [StringCollection](stringcollection-object.md) -Objekt ab, das Zeichen folgen enthält, die den Abfragebedingungen entsprechen.                                         |
| [isDeleted](mediacollection-isdeleted.md)                                       | Ruft einen Wert ab, der angibt, ob sich das angegebene Medien Element im Ordner "Gelöschte Elemente" befindet.                                                                  |
| [remove](mediacollection-remove.md)                                             | Entfernt ein Element aus der Medien Auflistung.                                                                                                                     |
| [SetDeleted](mediacollection-setdeleted.md)                                     | Verschiebt das angegebene Medien Element in den Ordner "Gelöschte Elemente".                                                                                                    |



 

Der Zugriff auf das **mediacollection** -Objekt erfolgt über die folgende Eigenschaft.



| Object                      | Eigenschaft                                      |
|-----------------------------|-----------------------------------------------|
| [Player](player-object.md) | [mediacollection](player-mediacollection.md) |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodell Referenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




