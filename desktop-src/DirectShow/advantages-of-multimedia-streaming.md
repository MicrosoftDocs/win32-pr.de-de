---
description: Vorteile von Multimedia Streaming
ms.assetid: 01020ad5-430d-4b4d-8de3-bcc81270e132
title: Vorteile von Multimedia Streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd907d9b8e91cb61709479a2d600323d6d420958
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132157"
---
# <a name="advantages-of-multimedia-streaming"></a>Vorteile von Multimedia Streaming

> [!Note]  
> Diese APIs sind veraltet. Anwendungen sollten den [**Beispiel-Grabber**](sample-grabber-filter.md) Filter verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filter Diagramm zu erhalten.

 

Wenn Entwickler in Ihren Anwendungen multimediastreaming verwenden, wird die Menge der erforderlichen Format spezifischen Programmierung erheblich reduziert. In der Regel muss eine Anwendung, die Mediendaten aus einer Datei oder Hardware Quelle abrufen muss, alles über das Datenformat und das Hardware Gerät wissen. Die Anwendung muss die Verbindung, die Übertragung von Daten, die erforderliche Datenkonvertierung und das tatsächliche Daten Rendering oder den Dateispeicher verarbeiten. Da sich jedes Format und jedes Gerät geringfügig unterscheiden, ist dieser Prozess häufig komplex und mühsam. Das Multimedia-Streaming hingegen aushandiert die Übertragung und Konvertierung von Daten aus der Quelle in die Anwendung automatisch. Die streamingschnittstellen stellen eine einheitliche und vorhersagbare Methode des Datenzugriffs und-Steuer Elements bereit, die es einer Anwendung erleichtert, die Daten unabhängig von ihrer ursprünglichen Quelle oder Ihrem ursprünglichen Format wiederzugeben.

Die folgenden Schritte zeigen, wie Streaming von einem Hardware Gerät zur gerenderten Wiedergabe implementiert wird.

1.  Eine Quelle von Videodaten, z. b. DirectShow, macht die streamingschnittstellen verfügbar.
2.  Der Anwendungsentwickler verwendet die Multimedia-streamingschnittstellen zum Verarbeiten der Datenformat Konvertierung.
3.  Der Anwendungsentwickler verwendet die DirectDraw-Schnittstellen, um die resultierenden Daten zu erzeugen.

Die Spezifikation für Multimedia-Streams besteht aus mehreren Schnittstellen. jede Schnittstelle enthält Methoden, die einen bestimmten Aspekt des streamingprozesses Steuern oder einen bestimmten Datentyp verarbeiten. Weitere Informationen finden Sie [in der Liste der multimediastreaming-Schnittstellen](list-of-multimedia-streaming-interfaces.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur multimediastreamingarchitektur](about-the-multimedia-streaming-architecture.md)
</dt> </dl>

 

 



