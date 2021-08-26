---
title: Arbeiten mit Metadaten
description: Arbeiten mit Metadaten
ms.assetid: 15d835c2-e227-4e69-a8b2-9b1c6d671022
keywords:
- Windows Media Format SDK, Übersicht über Metadaten
- Advanced Systems Format (ASF), Metadatenübersicht
- ASF (Advanced Systems Format), Metadatenübersicht
- metadata,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c001eed5330d3d90cdbf42cc52cfef3f048a25f7d8f72fe4402a48ccbb42480
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109880"
---
# <a name="working-with-metadata"></a>Arbeiten mit Metadaten

Metadatenunterstützung wird vom Writer-Objekt, dem Reader und den synchronen Readerobjekten sowie vom Metadaten-Editor-Objekt bereitgestellt. Allgemeine Informationen zu Metadaten finden Sie unter [Metadaten.](metadata.md) Informationen zu den Features, die Metadaten im Windows Media Format SDK unterstützen, finden Sie unter [Metadatenfeatures.](metadata-features.md)

Die Schnittstelle für die Metadatenbearbeitung ist [**IWMHeaderInfo3,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)die Sie durch Aufrufen der **QueryInterface-Methode** einer beliebigen Schnittstelle in einem der oben aufgeführten Objekte abrufen können. **IWMHeaderInfo3** erbt die Methoden von [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) und [**IWMHeaderInfo2.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) Die Methoden von **IWMHeaderInfo3,** die metadatenattribute behandeln, stellen einen anderen Ansatz für den Zugriff auf Metadaten dar als die methoden von **IWMHeaderInfo**. Sie sollten immer die neueren Methoden verwenden.

Metadaten in einer ASF-Datei werden durch einen Index und eine Streamnummer identifiziert. Attributen auf Dateiebene wird eine Streamnummer von 0 zugewiesen. In früheren Versionen des Windows Media Format SDK konnten Attribute anhand des Namens identifiziert werden. Da Sie jetzt Attributnamen in einem Stream duplizieren können, ist dies jedoch nicht mehr möglich. Stattdessen können Sie alle Indizes abrufen, die einem Namen entsprechen. Weitere Informationen finden Sie unter [Abrufen von Metadatenattributen.](retrieving-metadata-attributes.md)

Um die schnelle Suche nach Attributen zu unterstützen, können Sie eine spezielle Streamnummer 0xFFFF verwenden. Verwenden Sie diese Streamnummer, um die Datei als Ganzes anstelle eines bestimmten Streams oder der Attribute auf Dateiebene zu identifizieren. Die Objekte des Windows Media Format SDK verwalten separate Indizes für jeden Stream und für die Attribute auf Dateiebene. Wenn Sie Stream 0xFFFF verwenden, unterscheiden sich die Indizes von denen, die Sie beim Angeben eines bestimmten Streams verwenden. Beispielsweise ist das Attribut, das index 0 für Stream 0 ist, nicht dasselbe wie das Attribut, das Index 0 für stream 0xFFFF ist.

In den folgenden Abschnitten wird die Verwendung von Metadaten ausführlicher beschrieben.



| `Section`                                                                    | BESCHREIBUNG                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Abrufen von Metadatenattributen](retrieving-metadata-attributes.md)       | Beschreibt, wie Metadatenattribute aus einem Dateiheader gelesen werden.                     |
| [Festlegen von Metadatenattributen](setting-metadata-attributes.md)             | Beschreibt, wie einem Dateiheader neue Metadatenattribute hinzugefügt werden.                    |
| [Bearbeiten von Metadatenattributen](editing-metadata-attributes.md)             | Beschreibt, wie vorhandene Metadatenattribute bearbeitet werden.                               |
| [Entfernen von Metadatenattributen](removing-metadata-attributes.md)           | Beschreibt, wie vorhandene Metadatenattribute entfernt werden.                             |
| [Verwenden komplexer Metadatenattribute](using-complex-metadata-attributes.md) | Beschreibt die Arbeit mit Attributen, deren Werte durch Strukturen dargestellt werden. |



 

Mehrere Beispielanwendungen zeigen, wie Metadaten abgerufen und bearbeitet werden. Sehen Sie sich insbesondere das MetadataEdit-Beispiel an, das sowohl in C++- als auch in C#-Versionen enthalten ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Attribute**](attributes.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> <dt>

[**Beispielanwendungen**](sample-applications.md)
</dt> </dl>

 

 




