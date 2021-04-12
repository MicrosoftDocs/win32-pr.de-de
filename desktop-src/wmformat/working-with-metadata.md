---
title: Arbeiten mit Metadaten
description: Arbeiten mit Metadaten
ms.assetid: 15d835c2-e227-4e69-a8b2-9b1c6d671022
keywords:
- Windows Media-Format-SDK, Übersicht über Metadaten
- Advanced Systems Format (ASF), Übersicht über Metadaten
- ASF (Advanced Systems Format), Übersicht über Metadaten
- Metadaten, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050336d18947059373ddccf3f18e5d4295834293
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104390064"
---
# <a name="working-with-metadata"></a>Arbeiten mit Metadaten

Metadatenunterstützung wird durch das Writer-Objekt, das Reader-und das synchrone Reader-Objekt und das Metadaten-Editor-Objekt bereitgestellt. Allgemeine Informationen zu Metadaten finden Sie unter [Metadaten](metadata.md). Informationen zu den Funktionen, die Metadaten im Windows Media Format SDK unterstützen, finden Sie unter [Metadatenfeatures](metadata-features.md).

Die Schnittstelle für die Metadatenbearbeitung ist [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3). Diese können Sie abrufen, indem Sie die **QueryInterface** -Methode einer beliebigen Schnittstelle in einem der oben aufgeführten Objekte aufrufen. **IWMHeaderInfo3** erbt die Methoden von " [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) " und " [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)". Die Methoden von **IWMHeaderInfo3** , die sich mit Metadatenattributen befassen, stellen einen anderen Ansatz für den Zugriff auf Metadaten dar als die, die von den Methoden von **iwmheaderinfo** verwendet werden. Die neueren Methoden sollten immer verwendet werden.

Metadaten in einer ASF-Datei werden durch einen Index und eine streamnummer identifiziert. Attributen auf Dateiebene wird eine streamnummer von 0 zugewiesen. In früheren Versionen des SDK für den Windows Media-Format konnten Attribute anhand des Namens identifiziert werden. Da Sie nun jedoch Attributnamen innerhalb eines Streams duplizieren können, ist dies nicht mehr möglich. Stattdessen können Sie alle Indizes abrufen, die mit einem Namen übereinstimmen. Weitere Informationen finden Sie unter [Abrufen von Metadatenattributen](retrieving-metadata-attributes.md).

Um das Auffinden von Attributen zu erleichtern, können Sie eine spezielle streamnummer (0xFFFF) verwenden. Verwenden Sie diese streamnummer, um die Datei als Ganzes zu identifizieren, anstatt einen bestimmten Stream oder die Attribute auf Dateiebene. Die Objekte des Windows Media Format SDK behalten separate Indizes für jeden Stream und die Attribute auf Dateiebene. Wenn Sie Stream 0xFFFF verwenden, unterscheiden sich die Indizes von den Indizes, die Sie beim Angeben eines bestimmten Datenstroms verwenden. Beispielsweise ist das-Attribut, das Index 0 für Stream 0 ist, nicht mit dem-Attribut identisch, das Index 0 für Stream 0xFFFF ist.

In den folgenden Abschnitten wird die Verwendung von Metadaten ausführlicher beschrieben.



| `Section`                                                                    | BESCHREIBUNG                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [Abrufen von Metadatenattributen](retrieving-metadata-attributes.md)       | Beschreibt, wie Metadatenattribute aus einem Dateiheader gelesen werden.                     |
| [Festlegen von Metadatenattributen](setting-metadata-attributes.md)             | Beschreibt das Hinzufügen neuer Metadatenattribute zu einem Dateiheader.                    |
| [Bearbeiten von Metadatenattributen](editing-metadata-attributes.md)             | Beschreibt, wie vorhandene Metadatenattribute bearbeitet werden.                               |
| [Entfernen von Metadatenattributen](removing-metadata-attributes.md)           | Beschreibt, wie vorhandene Metadatenattribute entfernt werden.                             |
| [Verwenden komplexer Metadatenattribute](using-complex-metadata-attributes.md) | Beschreibt, wie Sie mit Attributen arbeiten, deren Werte durch-Strukturen dargestellt werden. |



 

Einige der Beispielanwendungen zeigen, wie Metadaten abgerufen und bearbeitet werden. Lesen Sie insbesondere das MetadataEdit-Beispiel, das sowohl in der C++-als auch in der c#-Version verfügbar ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Attribute**](attributes.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> <dt>

[**Beispielanwendungen**](sample-applications.md)
</dt> </dl>

 

 




