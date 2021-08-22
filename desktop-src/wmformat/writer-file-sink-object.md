---
title: Writer-Dateisenke (Objekt)
description: Writer-Dateisenke (Objekt)
ms.assetid: 93f44579-fb2d-498e-a271-5bc91d6f0321
keywords:
- Windows Medienformat-SDK, Writerdatei-Senkenobjekte
- Advanced Systems Format (ASF),Writer-Dateisenkeobjekte
- ASF (Advanced Systems Format), Writer-Dateisenkeobjekte
- Objekte,Writer-Dateisenkenobjekte
- Writerdatei-Senkenobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08efb5c404a822b0c30747864bdc01f57cb1a0618eed3f7ad26bd92f158ba625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083644"
---
# <a name="writer-file-sink-object"></a>Writer-Dateisenke (Objekt)

Das Writer-Dateisenkenobjekt wird beim Schreiben Windows Medienausgabe in eine Datei verwendet.

Das Writer-Dateisenkenobjekt wird von der [**Funktion WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)erstellt, die einen Zeiger auf eine **IWMWriterFileSink-Schnittstelle** legt. Die anderen Schnittstellen des Writer-Dateisenkenobjekts können durch Aufrufen der **QueryInterface-Methode ermittelt** werden.

Die folgenden Schnittstellen werden vom Writer-Dateisenkenobjekt unterstützt.



| Schnittstelle                                          | Beschreibung                                                                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) | Ermöglicht es der Anwendung, Statusmeldungen aus dem -Objekt zu erhalten.                                                                 |
| [**IWMWriterFileSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)     | Öffnet eine Datei, in die das Writerobjekt Daten schreiben kann.                                                                         |
| [**IWMWriterFileSink2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)   | Ermöglicht die erweiterte Verwaltung eines Dateisenkenobjekts. Erbt alle Methoden von **IWMWriterFileSink.**                       |
| [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)   | Stellt zusätzliche Optionen zum Schreiben von Dateien zur Verfügung. Erbt alle Methoden von **IWMWriterFileSink** und **IWMWriterFileSink2.** |
| [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)             | Weist Arbeitsspeicher zu, bestimmt, ob die Senke in Echtzeit ausgeführt wird, und verarbeitet mehrere Rückruffunktionen.                |



 

Die folgende Rückrufschnittstelle sollte von der Anwendung implementiert werden, um den Fortschritt eines Writerdatei-Senkenobjekts nachverfolgung zu können.



| Schnittstelle                                      | Beschreibung                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Erforderlich, wenn Statusinformationen an die Hostanwendung übermittelt werden müssen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Arbeiten mit Writer-Senken**](working-with-writer-sinks.md)
</dt> </dl>

 

 




