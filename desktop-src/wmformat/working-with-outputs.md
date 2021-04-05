---
title: Arbeiten mit Ausgaben
description: Arbeiten mit Ausgaben
ms.assetid: e2e14e88-dddc-496d-8087-1455da0821e3
keywords:
- Windows Media-Format-SDK, arbeiten mit Ausgaben
- Advanced Systems Format (ASF), arbeiten mit Ausgaben
- ASF (Advanced Systems Format), arbeiten mit Ausgaben
- Advanced Systems Format (ASF), Ausgabe Nummern und Formate
- ASF (Advanced Systems Format), Ausgabe Nummern und Formate
- ausgabezahlen und Formate, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d089a645838a295e07eb740927d75238473cc4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723456"
---
# <a name="working-with-outputs"></a>Arbeiten mit Ausgaben

Standardmäßig wird jedes Beispiel, das Sie von einem Leser Objekt erhalten, einer Ausgabe Nummer zugeordnet. Jede Ausgabe Nummer entspricht einem Stream in der ASF-Datei. Der Reader weist den Streams in der Dateiausgabe Nummern zu, wenn die Datei geöffnet wird. Normalerweise gibt es eine Ausgabe für jeden Stream in einer Datei. Wenn die Datei jedoch den gegenseitigen Ausschluss verwendet, wird jeder Gruppe von sich gegenseitig ausschließenden Streams eine einzelne Ausgabe Nummer zugewiesen. Der Stream, der der Ausgabe Nummer der sich gegenseitig exklusiven Datenströme entspricht, wird entweder vom Reader, bei MBR-Dateien (Multiple Bitrate) oder von der Anwendung bestimmt, wenn Sie die manuelle Datenstrom Auswahl verwenden.

Da der im Profil festgelegte Verbindungs Name nicht in der Datei persistent gespeichert wird, erstellt der Reader einen Standard Verbindungs Namen für jede Ausgabe, bei der es sich einfach um eine Zeichen folgen Darstellung der Ausgabe Nummer handelt, z. b. "1", "2", "3" usw. Mit den Verbindungs Namen können Anwendungen und der Reader selbst Ausgaben mit Streams korrelieren. In einer Datei mit mehreren Bitraten haben mehrere Streams einen Verbindungs Namen gemeinsam. Dies ist für den Reader nicht von Bedeutung, da die Ausgabe Eigenschaften für jeden MBR-Datenstrom identisch sind.

Jede Ausgabe verfügt über ein oder mehrere unterstützte Ausgabeformate. Ein Ausgabeformat ist das Format, das von den vom Reader bereitgestellten nicht komprimierten Beispielen verwendet wird. Wenn der Reader eine Datei öffnet, wird das Format der einzelnen Ausgaben auf den Standardwert für den Medien Untertyp festgelegt. Die Anzahl und der Typ der unterstützten Ausgabeformate werden vom Codec bestimmt, der die Mediendaten dekomprimiert.

In den folgenden Themen wird erläutert, wie Sie mit Ausgaben arbeiten:

-   [So identifizieren Sie Ausgabe Nummern](to-identify-output-numbers.md)
-   [Zuweisen von Ausgabeformaten](assigning-output-formats.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Iwmsynkreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> </dl>

 

 




