---
title: Eingaben, Streams und Ausgaben
description: Eingaben, Streams und Ausgaben
ms.assetid: f9f979c4-a15c-4f2a-b63c-7fe776394fdd
keywords:
- SDK für Windows Media-Format, Eingaben
- Windows Media-Format-SDK, Streams
- Windows Media-Format-SDK, Ausgaben
- Advanced Systems Format (ASF), Eingaben
- ASF (Advanced Systems Format), Eingaben
- Advanced Systems Format (ASF), Streams
- ASF (Advanced Systems Format), Streams
- Advanced Systems Format (ASF), Ausgaben
- ASF (Advanced Systems Format), Ausgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84e6b6941a990b108c16b49648ec0d8d028a44d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342077"
---
# <a name="inputs-streams-and-outputs"></a>Eingaben, Streams und Ausgaben

Eine "Eingabe" in dieser Dokumentation ist ein beliebiger digitaler Mediendaten Strom (z. b. Audiodaten oder Videos), den Ihre Anwendung mithilfe entsprechender APIs an das Writer-Objekt übermittelt. Eingaben müssen in einem unterstützten Format übermittelt werden. Einige Standard-RGB-und YUV-Formate werden als Eingabe unterstützt, und die Audiocodecs unterstützen PCM. Wenn ein angegebenes Eingabeformat vom Codec nicht nativ unterstützt wird, instanziiert das Writer-Objekt entweder ein Audio-oder Video-Hilfsobjekt, das eine Vielzahl von Formaten in Formate, die der Codec annehmen kann, in Formate umwandelt. Bei Audioeingaben werden das Hilfsobjekt die Bittiefe, die Samplingrate und die Anzahl der Kanäle nach Bedarf anpassen. Bei Videoeingaben führt das videohilfsobjekt eine Farb Raum Konvertierung und eine Anpassung der Rechteck Größe durch. In einigen Fällen können komprimierte Audiodaten und Videodaten in einen Eingabestream übermittelt werden. Eine Eingabe kann ein anderer Medientyp neben Audiodaten und Videos sein, z. b. Text, Skript Befehle, weiterhin Bilder oder beliebige Datei Daten.

Eine "Ausgabe" in dieser Dokumentation bezieht sich auf Daten, die das Reader-Objekt zum Rendern an eine Anwendung übergibt. Eine Ausgabe entspricht einem einzelnen Stream zum Zeitpunkt der Wiedergabe. Wenn Sie den gegenseitigen Ausschluss verwenden, teilen sich alle gegenseitig ausschließenden Streams eine einzelne Ausgabe. In der Regel sind Ausgabedaten in Form von unkomprimierten Audiodaten oder Videodaten, obwohl Sie beliebige Datentypen enthalten können. Unterstützte Videoausgabe Formate sind an anderer Stelle in dieser Dokumentation aufgeführt.

Der Begriff "Stream" in dieser Dokumentation bezieht sich auf Daten in einer ASF-Datei im Gegensatz zu (1) den Eingabe Quelldaten, bevor Sie vom Writer-Objekt verarbeitet werden, und (2) der Ausgabedaten, nachdem Sie vom Reader-Objekt dekomprimiert wurden. Ein ASF-Datenstrom enthält Daten, die aus einer einzelnen Eingabe für das Writer-Objekt stammen, obwohl mehr als ein Stream aus derselben Eingabe erstellt werden kann. Ein Stream weist die gleichen Format-und Komprimierungs Einstellungen von Anfang bis Ende auf. Eine einfache ASF-Datei verfügt über zwei Streams: einen für Audiodaten und einen für Video. Eine komplexere Datei kann über zwei Audiostreams und mehrere Videostreams verfügen. Die Audiodatenströme verfügen möglicherweise über dieselben Komprimierungs Einstellungen, Sie enthalten jedoch unterschiedliche Inhalte, z. b. eine Erzählung in verschiedenen Sprachen. Die Videostreams enthalten möglicherweise denselben Inhalt, haben jedoch unterschiedliche Komprimierungs Einstellungen. Das Medienformat und die Komprimierungs Einstellungen, die das Writer-Objekt für jeden Stream anwendet, werden im Profil angegeben.

Die Beziehung zwischen Eingaben, Streams und Ausgaben kann aus drei grundlegenden Typen bestehen. In den folgenden drei Diagrammen werden die Beziehungen veranschaulicht.

In der grundlegendsten Beziehung, bei der es sich um ein Profil ohne gegenseitiger Ausschluss handelt, wird jede Eingabe vom Writer verarbeitet und als einzelner Stream in die ASF-Datei eingefügt. Bei der Wiedergabe liest der Reader den Stream und übergibt nicht komprimierte Beispiele als einzelne Ausgabe, wie im folgenden Diagramm dargestellt.

![das Diagramm zeigt die normale Beziehung zwischen Eingaben, Streams und Ausgaben.](images/formatsdk03.png)

Eine komplexere Beziehung tritt auf, wenn ein gegenseitiger Ausschluss der Bitrate verwendet wird. In diesem Fall wird eine einzelne Eingabe vom Writer verarbeitet und mit mehreren Bitraten codiert. Jede Codierung der Daten wird in der ASF-Datei als separater Stream eingefügt. Bei der Wiedergabe bestimmt der Reader basierend auf der verfügbaren Bandbreite, welcher Stream dekomprimiert werden soll. Der Reader liest dann den ausgewählten Stream und übergibt nicht komprimierte Beispiele als einzelne Ausgabe, wie im folgenden Diagramm dargestellt.

![das Diagramm zeigt die Beziehungen zwischen Eingaben, Streams und Ausgaben bei Verwendung des gegenseitigen Ausschlusses mehrerer Bitrate.](images/formatsdk04.png)

Der dritte Beziehungstyp kann auftreten, wenn ein sprach basierter oder benutzerdefinierter gegenseitiger Ausschluss verwendet wird. In dieser Beziehung werden mehrere Eingaben vom Reader verarbeitet, und jede wird als einzelner Stream in die ASF-Datei eingefügt. Bei der Wiedergabe wählt die Anwendung manuell aus, welcher Stream basierend auf der von Ihnen bereitgestellten Logik dekomprimiert werden soll. Der Reader liest dann den ausgewählten Stream und übergibt nicht komprimierte Beispiele als einzelne Ausgabe. Dieser Prozess kann zum Einschließen von Sound Spuren in mehreren Sprachen verwendet werden. Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.

![das Diagramm zeigt die Beziehungen zwischen Eingaben, Streams und Ausgaben bei Verwendung des benutzerdefinierten gegenseitigen Ausschlusses.](images/formatsdk02.png)

Es gibt einige Abweichungen in den zuvor beschriebenen Beziehungen. Eine Datei kann z. b. alle drei Beziehungen oder eine oder zwei Beziehungen enthalten. Es ist auch möglich, dass einige Eingaben komprimiert werden. in diesem Fall führt der Writer keine zusätzliche Komprimierung durch. Der Reader kann auch komprimierte Beispiele bereitzustellen. Wenn dies der Fall ist, müssen Sie über die streamnummer und nicht über die Ausgabe Nummer darauf zugreifen.

> [!Note]  
> Eingaben, Steams und Ausgaben sind alle mit den Objekten des Windows Media Format SDK zugewiesene Zahlen. Streams verfügen über eine streamnummer, die 1-basiert ist und die Sie im Profil definieren. Jedem Datenstrom wird auch ein Stream-Index für die Enumeration von Datenströmen in einem Profil zugewiesen. Keine dieser Zahlen ist gewährleistet, dass Sie konsistent zueinander sind. Das heißt, die Eingabe Nummer 1 entspricht möglicherweise nicht der Stream-Nummer 1, die streamnummer 1 entspricht möglicherweise nicht dem Stream-Index 1 usw.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konzepte**](concepts.md)
</dt> <dt>

[**Gegenseitiger Ausschluss**](mutual-exclusion.md)
</dt> </dl>

 

 




