---
title: Formate
description: Formate
ms.assetid: 7c602643-f1fc-4fbd-a739-4296dc758bc9
keywords:
- SDK für Windows Media-Format, Eingaben
- Windows Media-Format-SDK, Streams
- Windows Media-Format-SDK, Ausgaben
- Windows Media-Format-SDK, Formate
- Advanced Systems Format (ASF), Eingaben
- ASF (Advanced Systems Format), Eingaben
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- Advanced Systems Format (ASF), Ausgaben
- ASF (Advanced Systems Format), Ausgaben
- Advanced Systems Format (ASF), Formate
- ASF (Advanced Systems Format), Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e7895c27af3eb99e96d7009b79ea8df0011208
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310784"
---
# <a name="formats"></a>Formate

Die Informationen in einem Format beschreiben alles, was Sie über einen bestimmten Medientyp wissen müssen. Jedes Format weist einen Haupttyp auf, wie z. b. Audiodaten oder Video, und kann einen Untertyp aufweisen. Formate enthalten unterschiedliche Informationen auf Grundlage des Haupt Typs. Audioformate und Videoformate erfordern wesentlich mehr Informationen als andere Typen.

Ebenso wie die Objekte des Windows Media SDK-SDK zwischen Eingabe Zahlen, streamnummern und Ausgabe Nummern (siehe [Eingaben, Streams und Ausgaben](inputs-streams-and-outputs.md)) unterscheiden, gibt es wichtige Unterschiede zwischen Eingabe Formaten, streamformaten und Ausgabeformaten. Diese Unterschiede werden hier beschrieben:

## <a name="input-formats"></a>Eingabeformate

Ein Eingabeformat beschreibt die digitalen Medien, die Sie an das Writer-Objekt übergeben. Wenn ein Datenstrom in einer ASF-Datei mit einem Codec komprimiert wird, unterstützt der Codec nur bestimmte Eingabeformate. Wenn Sie die Windows Media Audio-und Video Codecs verwenden, können Sie die unterstützten Eingabeformate mithilfe des Writer-Objekts auflisten. Beim Schreiben einer Datei sind Sie dafür verantwortlich, ein Eingabeformat auszuwählen, das mit den Eingabemedien übereinstimmt.

Obwohl das Eingabemedien Format vom Codec unterstützt werden muss, mit dem die Daten komprimiert werden, müssen einige Eingabeformat Einstellungen nicht dem Streamformat entsprechen. Beispielsweise kann das Eingabeformat für einen Videostream eine Frame Größe aufweisen, die sich von der im Streamformat definierten Frame Größe unterscheidet. Der Codec führt Konvertierungen in diesen Fällen aus.

## <a name="stream-formats"></a>Streamformate

Ein Streamformat beschreibt das Formular des Mediums, das in der ASF-Datei gespeichert ist. Das Datenstrom Format ist das im Profil beschriebene Format und kann mit dem Eingabeformat und dem Ausgabeformat identisch sein. Wenn ein Codec zum Komprimieren der Daten in einem Stream verwendet wird, unterscheidet sich das Streamformat von den Eingabe-und Ausgabeformaten.

Wenn Sie die Windows Media Audio-und Video Codecs verwenden, müssen Sie eine Liste der unterstützten Streamformate vom Codec abrufen, um sicherzustellen, dass Sie nicht versuchen, ein Format anzugeben, das der Code nicht unterstützt. Einige Format Einstellungen (z. b. die Größe und die Farbtiefe eines Video Frames) müssen manuell konfiguriert werden, nachdem das Codec-Format abgerufen wurde.

## <a name="output-formats"></a>Ausgabeformate

In einem Ausgabeformat werden die digitalen Medien beschrieben, die der Reader (oder der synchrone Reader) an die Anwendung übermittelt. Wenn ein Datenstrom in einer ASF-Datei mit einem Codec komprimiert wird, unterstützt der Codec nur bestimmte Ausgabeformate. Wenn Sie die Windows Media Audio-und Video Codecs verwenden, können Sie die unterstützten Ausgabeformate mithilfe des Reader-Objekts auflisten. Jedes der Windows Media-Codecs verfügt über ein Standardausgabeformat, aber Sie können ein beliebiges unterstütztes Ausgabeformat für die Beispiel Übermittlung auswählen.

Obwohl das Ausgabemedien Format vom Codec unterstützt werden muss, der die Daten komprimiert, müssen einige Ausgabe Formateinstellungen nicht dem Streamformat entsprechen. Das Ausgabeformat für einen Videostream kann z. b. eine Frame Größe aufweisen, die sich von der im Streamformat definierten Frame Größe unterscheidet. Der Codec führt Konvertierungen in diesen Fällen aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](concepts.md)
</dt> </dl>

 

 




