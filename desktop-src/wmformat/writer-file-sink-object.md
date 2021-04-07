---
title: Writer-Dateisenke (Objekt)
description: Writer-Dateisenke (Objekt)
ms.assetid: 93f44579-fb2d-498e-a271-5bc91d6f0321
keywords:
- Windows Media-Format-SDK, Writer File Sink Objects
- Advanced Systems Format (ASF), Writer File Sink Objects
- ASF (Advanced Systems Format), Writer File Sink Objects
- Objekte, Senke-Objekte von Writer-Dateien
- Writer-Datei-Sink-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82009e5be74cfc23e687001a2a81cd4546812af9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104038688"
---
# <a name="writer-file-sink-object"></a>Writer-Dateisenke (Objekt)

Das writerdatei-Sink-Objekt wird beim Schreiben der Windows Media-Ausgabe in eine Datei verwendet.

Das Writer File Sink-Objekt wird von der [**wmkreateschreiterfilesink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)-Funktion erstellt, die einen Zeiger auf eine **iwmschreiterfilesink** -Schnittstelle festlegt. Die anderen Schnittstellen des Writer-Datei-Senkenobjekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.

Die folgenden Schnittstellen werden vom Writer-Datei-senksobjekt unterstützt.



| Schnittstelle                                          | BESCHREIBUNG                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmregistercallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Ermöglicht es der Anwendung, Statusmeldungen aus dem-Objekt zu erhalten.                                                                 |
| [**Iwmschreibfilesink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)     | Öffnet eine Datei, in die das Writer-Objektdaten schreiben kann.                                                                         |
| [**IWMWriterFileSink2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)   | Ermöglicht die Erweiterte Verwaltung eines dateisink-Objekts. Erbt alle Methoden von **iwmschreiterfilesink**.                       |
| [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)   | Bietet zusätzliche Optionen zum Schreiben von Dateien. Erbt alle Methoden von **iwmschreiterfilesink** und **IWMWriterFileSink2**. |
| [**Iwmschreibsink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Weist Arbeitsspeicher zu, bestimmt, ob die Senke in Echtzeit ausgeführt wird, und verarbeitet mehrere Rückruf Funktionen.                |



 

Die folgende Rückruf Schnittstelle sollte von der Anwendung implementiert werden, um den Fortschritt eines Writer-Datei-Sink-Objekts zu verfolgen.



| Schnittstelle                                      | BESCHREIBUNG                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**Iwmstatus Callback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Erforderlich, wenn Statusinformationen an die Host Anwendung übermittelt werden müssen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Arbeiten mit Writer-senken**](working-with-writer-sinks.md)
</dt> </dl>

 

 




