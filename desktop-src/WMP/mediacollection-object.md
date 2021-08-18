---
title: MediaCollection-Objekt
description: Das MediaCollection-Objekt bietet eine Möglichkeit, eine große Sammlung von Medienelementen zu organisieren. Es kann abgefragt werden, um Wiedergabelisten automatisch zu generieren.
ms.assetid: afcb2c51-3ecb-4529-8f3e-56aa6d0ec2b4
keywords:
- MediaCollection-Objekt Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e529bec203b836f1f1022793a18320a7612cb242de58407ddb998c7410a47cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996250"
---
# <a name="mediacollection-object"></a>MediaCollection-Objekt

Das **MediaCollection-Objekt** bietet eine Möglichkeit, eine große Sammlung von Medienelementen zu organisieren. Es kann abgefragt werden, um Wiedergabelisten automatisch zu generieren.

Das **MediaCollection-Objekt** unterstützt die folgenden Methoden.



| Methode                                                                           | BESCHREIBUNG                                                                                                                                                    |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [add](mediacollection-add.md)                                                   | Fügt der Bibliothek ein neues Medienelement oder eine neue Wiedergabeliste hinzu.                                                                                                              |
| [Createquery](mediacollection-createquery.md)                                   | Erstellt ein neues [Query-Objekt.](query-object.md)                                                                                                                |
| [getAll](mediacollection-getall.md)                                             | Ruft ein [Wiedergabelistenobjekt](playlist-object.md) ab, das alle Medienelemente in der Bibliothek enthält.                                                                  |
| [getAttributeStringCollection](mediacollection-getattributestringcollection.md) | Ruft ein [StringCollection-Objekt](stringcollection-object.md) ab, das den Satz aller Werte für ein angegebenes Attribut innerhalb eines angegebenen Medientyps darstellt. |
| [getBy Einmal](mediacollection-getbyalbum.md)                                     | Ruft ein [Wiedergabelistenobjekt](playlist-object.md) ab, das Medienelemente aus dem angegebenen Album enthält.                                                            |
| [getByAttribute](mediacollection-getbyattribute.md)                             | Ruft ein [Wiedergabelistenobjekt](playlist-object.md) ab, das Medienelemente mit dem angegebenen Attribut mit dem angegebenen Wert enthält.                             |
| [getByAttributeAndMediaType](mediacollection-getbyattributeandmediatype.md)     | Ruft ein [Wiedergabelistenobjekt](playlist-object.md) ab, das [Medienobjekte](media-object.md) mit dem angegebenen Attribut und Medientyp enthält.                 |
| [getByAuthor](mediacollection-getbyauthor.md)                                   | Ruft ein [Wiedergabelistenobjekt](playlist-object.md) ab, das Medienelemente des angegebenen Autors enthält.                                                             |
| [getByGenre](mediacollection-getbygenre.md)                                     | Ruft ein [Wiedergabelistenobjekt](playlist-object.md) ab, das Medienelemente mit dem angegebenen Genre enthält.                                                            |
| [getByName](mediacollection-getbyname.md)                                       | Ruft ein [Wiedergabelistenobjekt](playlist-object.md) ab, das Medienelemente mit dem angegebenen Namen enthält.                                                             |
| [getMediaAtom](mediacollection-getmediaatom.md)                                 | Ruft den Index ab, an dem sich eine angegebene Eigenschaft innerhalb des Satzes verfügbarer Eigenschaften befindet.                                                              |
| [getPlaylistByQuery](mediacollection-getplaylistbyquery.md)                     | Ruft ein [Wiedergabelistenobjekt](playlist-object.md) ab, das [Medienobjekte](media-object.md) enthält, die den Abfragebedingungen entsprechen.                               |
| [getStringCollectionByQuery](mediacollection-getstringcollectionbyquery.md)     | Ruft ein [StringCollection-Objekt](stringcollection-object.md) ab, das Zeichenfolgen enthält, die den Abfragebedingungen entsprechen.                                         |
| [isDeleted](mediacollection-isdeleted.md)                                       | Ruft einen Wert ab, der angibt, ob sich das angegebene Medienelement im Ordner für gelöschte Elemente befindet.                                                                  |
| [remove](mediacollection-remove.md)                                             | Entfernt ein Element aus der Medienauflistung.                                                                                                                     |
| [setDeleted](mediacollection-setdeleted.md)                                     | Verschiebt das angegebene Medienelement in den Ordner für gelöschte Elemente.                                                                                                    |



 

Auf das **MediaCollection-Objekt** wird über die folgende Eigenschaft zugegriffen.



| Object                      | Eigenschaft                                      |
|-----------------------------|-----------------------------------------------|
| [Player](player-object.md) | [mediaCollection](player-mediacollection.md) |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Objektmodellreferenz für Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




