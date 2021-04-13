---
title: Metadaten
description: Metadaten sind für dieses SDK Informationen, die eine ASF-Datei oder den Inhalt der Datei beschreiben.
ms.assetid: 4ccca0c3-52c5-4291-bdab-354705db9b10
keywords:
- Windows Media-Format-SDK, Übersicht über Metadaten
- Advanced Systems Format (ASF), Übersicht über Metadaten
- ASF (Advanced Systems Format), Übersicht über Metadaten
- Metadaten, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552e968ab4a5908ec1a2a80012ecba3a5b959c6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311250"
---
# <a name="metadata"></a>Metadaten

Metadaten sind für dieses SDK Informationen, die eine ASF-Datei oder den Inhalt der Datei beschreiben. Der Header Abschnitt einer ASF-Datei enthält alle Metadaten, die mit dieser Datei verknüpft sind. Einzelne Elemente von Metadaten in einer ASF-Datei werden als Attribute bezeichnet. Jedes Attribut verfügt über einen Namen und einen Wert. In dieser Dokumentation werden globale Konstanten verwendet, um Attribute zu identifizieren. Beispielsweise wird der Titel einer ASF-Datei im **g \_ wszwmtitle** -Attribut gespeichert.

Eine Reihe von Attributen werden im Windows Media-Format-SDK definiert, um die gängigsten Metadatenanforderungen zu verarbeiten. Außerdem können Sie eigene Attribute erstellen. Wenn Sie benutzerdefinierte Attribute benennen, sollten Sie jedoch darauf achten, dass andere Anwendungsentwickler dieselben Namen verwenden können und Konflikte auftreten können.

Einige Attribute werden vom SDK festgelegt und können nicht manuell geändert werden. Wenn Sie z. b. eine ASF-Datei indizieren, legt das SDK das **g \_ wszwmseekable** -Attribut fest, um anzuzeigen, dass die Datei jetzt von einem beliebigen angegebenen Punkt gelesen werden kann.

Andere Attribute sind reine Informations Informationen und müssen manuell festgelegt werden. Wenn Sie z. b. den Autor einer Datei nachverfolgen möchten, sollten Sie **g \_ wszwmauthor** festlegen.

Das Windows Media-Format-SDK bietet Unterstützung für Attribute, die auf die gesamte Datei angewendet werden, sowie Attribute, die auf einzelne Streams angewendet werden.

Sie können das SDK für den Windows Media-Format verwenden, um die Metadaten in MP3-Dateien zu bearbeiten. Sie sollten jedoch immer die in MP3-Dateien kompatiblen Attribute verwenden, um die Kompatibilität mit anderen MP3-Bearbeitungsprogrammen aufrechtzuerhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](concepts.md)
</dt> <dt>

[**Metadata Editor-Objekt**](metadata-editor-object.md)
</dt> <dt>

[**Metadatenfeatures**](metadata-features.md)
</dt> <dt>

[**Arbeiten mit Metadaten**](working-with-metadata.md)
</dt> </dl>

 

 




