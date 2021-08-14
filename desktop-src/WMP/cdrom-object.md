---
title: Come-Objekt
description: Das Cbetreiber-Objekt bietet eine Möglichkeit, auf eine CD oder DVD in seinem Laufwerk zu zugreifen.
ms.assetid: 9045b130-3e08-4880-a4e7-79b704c4c1f9
keywords:
- Come-Windows Media Player
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
# <a name="cdrom-object"></a>Come-Objekt

Das **Cbetreiber-Objekt** bietet eine Möglichkeit, auf eine CD oder DVD in seinem Laufwerk zu zugreifen.

Das **Ckrony-Objekt** unterstützt die folgenden Eigenschaften.



| Eigenschaft                                   | BESCHREIBUNG                                                                                                                                             |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [driveSpecifier](cdrom-drivespecifier.md) | Ruft den Cd- oder DVD-Laufwerkbuchstaben ab.                                                                                                                   |
| [Playlist](cdrom-playlist.md)             | Ruft ein [Playlist-Objekt](playlist-object.md) ab, das die Titel auf der CD darstellt, die sich derzeit auf dem CD-Laufwerk befindet, oder die Titeleinträge auf Stammebene für DVD. |



 

Das **Ckrony-Objekt** unterstützt die folgende Methode.



| Methode                   | BESCHREIBUNG                          |
|--------------------------|--------------------------------------|
| [Auswerfen](cdrom-eject.md) | Wirft die CD oder DVD vom Laufwerk aus. |



 

Der Zugriff auf das **Ckrony-Objekt** erfolgt über die folgende Methode.



| Object                                        | Methode                           |
|-----------------------------------------------|----------------------------------|
| [Ccollection](cdromcollection-object.md) | [item](cdromcollection-item.md) |



 

Zur Veranschaulichung wird player.c syntax.item(*index*) in den Referenzsyntaxabschnitten verwendet.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Objektmodellreferenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




