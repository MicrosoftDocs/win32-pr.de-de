---
title: Chole-Objekt
description: Das Chole-Objekt bietet eine Möglichkeit, auf eine CD oder DVD auf dem Laufwerk zuzugreifen.
ms.assetid: 9045b130-3e08-4880-a4e7-79b704c4c1f9
keywords:
- C Windows Media Player
topic_type:
- apiref
api_name:
- Cdrom Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 60c4e1081dec3e44107778e45fd911e0c4bb673d27b5e19874508ddbacb270ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342643"
---
# <a name="cdrom-object"></a>Chole-Objekt

Das **Chole-Objekt** bietet eine Möglichkeit, auf eine CD oder DVD auf dem Laufwerk zuzugreifen.

Das **C csv-Objekt** unterstützt die folgenden Eigenschaften.



| Eigenschaft                                   | BESCHREIBUNG                                                                                                                                             |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [driveSpecifier](cdrom-drivespecifier.md) | Ruft den Laufwerkbuchstaben der CD oder DVD ab.                                                                                                                   |
| [Playlist](cdrom-playlist.md)             | Ruft ein [Wiedergabelistenobjekt](playlist-object.md) ab, das die Titel auf der CD darstellt, die sich derzeit auf dem CD-Laufwerk befinden, oder die Titeleinträge auf Stammebene für die DVD. |



 

Das **C csv-Objekt** unterstützt die folgende Methode.



| Methode                   | BESCHREIBUNG                          |
|--------------------------|--------------------------------------|
| [Auswerfen](cdrom-eject.md) | Wirft die CD oder DVD vom Laufwerk aus. |



 

Der Zugriff auf das **C csv-Objekt** erfolgt über die folgende Methode.



| Object                                        | Methode                           |
|-----------------------------------------------|----------------------------------|
| [Ccollection](cdromcollection-object.md) | [item](cdromcollection-item.md) |



 

Zur Veranschaulichung wird player.ccollection.item(*index*) in den Abschnitten zur Verweissyntax verwendet.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Objektmodellreferenz für Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




