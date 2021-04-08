---
title: Gegenseitiger Ausschluss
description: Gegenseitiger Ausschluss
ms.assetid: 3a3f6763-a241-4bbd-a6e8-62041b05622d
keywords:
- Windows Media-Format-SDK, gegenseitiger Ausschluss
- Advanced Systems Format (ASF), gegenseitiger Ausschluss
- ASF (Advanced Systems Format), gegenseitiger Ausschluss
- Windows Media-Format-SDK, gegenseitiger MBR-Ausschluss
- Advanced Systems Format (ASF), gegenseitiger MBR-Ausschluss
- ASF (Advanced Systems-Format), gegenseitiger MBR-Ausschluss
- Windows Media-Format-SDK, mehrfache Bitrate (MBR)
- Advanced Systems Format (ASF), mehrfache Bitrate (MBR)
- ASF (Advanced Systems Format), Multiple Bitrate (MBR)
- gegenseitiger Ausschluss, Informationen
- mehrfache Bitrate (MBR), gegenseitiger Ausschluss
- MBR (mehrfache Bitrate), gegenseitiger Ausschluss
- gegenseitiger Ausschluss, Bitrate
- gegenseitiger Ausschluss, Sprache
- gegenseitiger Ausschluss, Präsentation
- gegenseitiger Ausschluss, unbekannt
- gegenseitiger Ausschluss, Features
- gegenseitiger Ausschluss, erweiterte Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd00bf5bcb544d2541a6bc5465171fe9bacc1b9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856888"
---
# <a name="mutual-exclusion"></a>Gegenseitiger Ausschluss

Jede ASF-Datei enthält einen oder mehrere Streams, die jeweils digitale Mediendaten enthalten. Unter normalen Umständen ist jeder Stream einer einzelnen Ausgabe zugeordnet. Bei der Wiedergabe stellt das Reader-Objekt für jede Ausgabe Beispiele bereit. Standardmäßig wird jeder Stream in einer ASF-Datei vom Reader bei der Wiedergabe zugestellt.

Es gibt Situationen, in denen Sie nicht möchten, dass jeder Stream an den Client übermittelt wird. Wenn Sie z. b. eine Videodatei mit fünf Audiostreams erstellen, eine für jede von fünf Sprachen, soll jeweils nur eine bereitgestellt werden. Der gegenseitige Ausschluss ist eine Funktion des Windows Media SDK-SDKs, mit der Sie eine Reihe von sich gegenseitig ausschließenden Streams angeben können, die alle derselben Ausgabe entsprechen.

Der gegenseitige Ausschluss wird im Profil definiert, das zum Erstellen einer Datei verwendet wird. Sie konfigurieren den gegenseitigen Ausschluss in einem Profil mithilfe von gegenseitigen Ausschluss Objekten. Sie fügen Streams nacheinander zum gegenseitigen Ausschluss Objekt hinzu, legen den Typ fest und fügen das Objekt in das Profil ein.

Das SDK für den Windows Media-Format erkennt vier Typen von gegenseitigem Ausschluss:

-   Bitrate
-   Sprache
-   Präsentation
-   Unbekannt

## <a name="mutual-exclusion-by-bit-rate"></a>Gegenseitiger Ausschluss durch Bitrate

Der gegenseitige Ausschluss der Bitrate ist eine besondere Art von gegenseitigem Ausschluss und wird häufiger als MBR-gegenseitiger Ausschluss (Multiple Bitrate) bezeichnet. Ein MBR-gegenseitiger Ausschluss enthält eine Reihe von Streams, die alle aus derselben Eingabe stammen, aber mit unterschiedlichen Bitraten codiert sind. Wenn eine Datei mit MBR abgespielt wird, bestimmt der Reader basierend auf der verfügbaren Bandbreite den besten Stream, der verwendet werden soll.

Das Windows Media-Format-SDK unterstützt MBR für Audiodaten und Videodaten Ströme. Das SDK unterstützt auch eine besondere Art von MBR-Video mit dem Namen "Multiple Video size MBR". Dies ähnelt dem normalen MBR-Video, mit dem Unterschied, dass die einzelnen Streams verschiedene Frame Größen aufweisen können. Beispielsweise verfügen Sie möglicherweise über einige Streams mit der Standardgröße von 320 x 240 und einige andere mit höheren Bitraten und 640 x 480 Video Größen.

## <a name="mutual-exclusion-by-language"></a>Gegenseitiger Ausschluss nach Sprache

Der sprachbasierte gegenseitige Ausschluss ist für die Verwendung mit Inhalten (normalerweise Audiodaten) konzipiert, die in mehreren Sprachen aufgezeichnet wurden. Ein sprach basierter gegenseitiger Ausschluss umfasst mehrere Streams, die aus eindeutigen Eingaben stammen. Jede Eingabe ist derselbe Inhalt, jedoch in einer anderen Sprache.

Damit der gegenseitige Ausschluss nach Sprache funktioniert, muss die Leseanwendung Logik enthalten, um die entsprechende Sprache auszuwählen. Wenn Sie eine Anwendung für die Wiedergabe von ASF-Dateien schreiben und Dateien mit sprach basiertem gegenseitigem Ausschluss unterstützen möchten, sollten Sie den entsprechenden Stream vor Beginn der Wiedergabe auswählen.

## <a name="mutual-exclusion-by-presentation"></a>Gegenseitiger Ausschluss durch Präsentation

Präsentations basierter gegenseitiger Ausschluss wird bereitgestellt, um Videostreams zu unterstützen, die denselben Inhalt enthalten, der mit unterschiedlichen Seitenverhältnissen codiert ist Dies wird in der Regel verwendet, wenn Videos in einer Briefkasten Version (Seitenverhältnis 16:9) bereitgestellt werden und für Fernsehbildschirme (Seitenverhältnis 4:3) formatiert wird.

Die Auswahl einer Präsentation für die Wiedergabe wird am häufigsten vom Benutzer festgelegt. Wenn Sie eine Anwendung für die Wiedergabe von ASF-Dateien schreiben und Dateien mit dem Präsentations basierten gegenseitigen Ausschluss unterstützen möchten, sollten Sie dem Benutzer die Möglichkeit geben, einen Präsentationstypen für die Anzeige auszuwählen.

## <a name="unknown-mutual-exclusion"></a>Unbekannter gegenseitiger Ausschluss

Sie können den gegenseitigen Ausschluss basierend auf beliebigen Kriterien erstellen. Alle benutzerdefinierten Typen für den gegenseitigen Ausschluss sollten mit dem unbekannten Typ erstellt werden.

## <a name="advanced-mutual-exclusion-features"></a>Erweiterte Funktionen für den gegenseitigen Ausschluss

Sie können auch den gegenseitigen Ausschluss verwenden, um Datenströme anderen Gruppen zuzuweisen, die sich gegenseitig ausschließen. Beispielsweise können Sie Audiodatenströme in mehreren Sprachen haben und jedem einen anderen Videostream zuweisen. Sie verwenden den gegenseitigen Ausschluss, um jeden Audiostream mit dem entsprechenden Videostream zu gruppieren und alle Gruppen gegenseitig zu schließen.

Der Reader wählt automatisch Streams für alle gegenseitigen Ausschlüsse aus. Für alle Typen von gegenseitigem Ausschluss mit Ausnahme von MBR und einem sprachbasierten gegenseitigen Ausschluss wählt der Reader stets den Standardstream aus. Dies ist der erste Datenstrom, der dem gegenseitigen Ausschluss Objekt im Profil hinzugefügt wird. Für MBR wählt der Reader den Stream aus, der zum Zeitpunkt der Wiedergabe am besten der verfügbaren Bandbreite entspricht. Wenn Sie den Standardstream nicht verwenden möchten, können Sie die Streamauswahl auf "manuell" festlegen, bevor Sie mit dem Lesen einer Datei beginnen.

Die manuelle Datenstrom Auswahl gilt für die gesamte Datei. Es können Schwierigkeiten auftreten, wenn Sie gegenseitige Ausschlüsse verschiedener Typen in derselben Datei haben. Beispielsweise kann eine Datei sowohl Bitrate-basierten gegenseitigen Ausschluss als auch benutzerdefinierter gegenseitiger Ausschluss enthalten. Wenn Sie einen anderen Datenstrom als den Standardwert im benutzerdefinierten gegenseitigen Ausschluss auswählen möchten, müssen Sie die manuelle Datenstrom Auswahl verwenden. Wenn Sie jedoch die manuelle Datenstrom Auswahl verwenden, wählt der Reader den multibitrate-Stream nicht automatisch aus. Sie müssen diese Eventualität in der Anwendung planen, wenn Sie beabsichtigen, mehrere Typen von gegenseitigem Ausschluss in einer einzelnen Datei zu unterstützen. In der Regel bedeutet dies, dass Sie eigene streamauswahlroutinen für normalerweise automatische Typen von gegenseitigem Ausschluss erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen der ASF-Datei**](asf-file-features.md)
</dt> <dt>

[**Verwenden von gegenseitigem Ausschluss**](using-mutual-exclusion.md)
</dt> </dl>

 

 




