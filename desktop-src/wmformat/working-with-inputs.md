---
title: Arbeiten mit Eingaben
description: Arbeiten mit Eingaben
ms.assetid: 72daa7ca-4264-46bf-91ac-8b95fdbfd41c
keywords:
- Windows Media-Format-SDK, arbeiten mit Eingaben
- Advanced Systems Format (ASF), arbeiten mit Eingaben
- ASF (Advanced Systems Format), arbeiten mit Eingaben
- Profile, arbeiten mit Eingaben
- Streams, arbeiten mit Eingaben
- Codecs, arbeiten mit Eingaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7016b5304b0d77e130b68d9a9feef15ffe54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471116"
---
# <a name="working-with-inputs"></a>Arbeiten mit Eingaben

Ebenso wie die richtige Datenstrom Konfiguration im Profil erforderlich ist, um den Codec zum Komprimieren eines Streams zu erhalten, müssen Sie auch sicherstellen, dass der Typ der nicht komprimierten Medien, die Sie an den Writer übergeben, korrekt beschrieben wird. Jedem Windows Media-Codec ist ein Standard Eingabetyp zugeordnet, es werden jedoch mehrere Eingabetypen unterstützt. Sie können die unterstützten Eingaben überprüfen und den Eintrag auswählen, der Ihren Daten entspricht. Der Prozess der Arbeit mit Eingaben wird in den folgenden Schritten zusammengefasst:

1.  Wenn Sie ein Profil für den Writer laden, weist das Writer-Objekt für jede Verbindung im Profil eine Eingabe Nummer zu. Weitere Informationen zum Laden von Profilen für den Writer finden [Sie unter So verwenden Sie Profile mit dem Writer](to-use-profiles-with-the-writer.md). Es gibt eine Verbindung für jeden Stream, es sei denn, Sie verwenden den gegenseitigen Ausschluss mit der Bitrate. Datenströme, die sich durch die Bitrate gegenseitig ausschließen, haben eine einzelne Verbindung gemeinsam.
2.  Die Anwendung sollte die Eingabe Nummern für die Datei identifizieren. Weitere Informationen zum Identifizieren von Eingabe Nummern finden [Sie unter So identifizieren Sie Eingaben nach Nummer](to-identify-inputs-by-number.md).
3.  Für jede Eingabe sollten Sie sicherstellen, dass das Eingabeformat mit Ihren Daten übereinstimmt. Sie können die vom SDK unterstützten Eingabeformate auflisten. Weitere Informationen finden [Sie unter so zählen Sie Eingabeformate auf](to-enumerate-input-formats.md). Sie können die Eingabeformate von beliebigen Streams oder Streams, die bereits komprimiert sind, nicht aufzählen. Weitere Informationen zu diesen besonderen Fällen finden Sie unter [beliebige und vorkomprimierte streameingaben](arbitrary-and-precompressed-stream-inputs.md).
4.  Weisen Sie das richtige Eingabeformat für jede Verbindung zu. Weitere Informationen finden Sie unter [Zuweisen von Eingabe Formaten](assigning-input-formats.md).
5.  Einige Codec-und Writer-Funktionen werden zur Codierungs Zeit anstelle von im Profil konfiguriert. Zum Konfigurieren dieser Features müssen Sie die Eingabeeinstellungen verwenden. Weitere Informationen finden [Sie unter So legen Sie Eingabeeinstellungen fest](to-set-input-settings.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




