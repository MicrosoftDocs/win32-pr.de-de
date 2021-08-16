---
title: Verwenden von Dateisenken
description: Verwenden von Dateisenken
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- Advanced Systems Format (ASF), Dateisenken
- ASF (Advanced Systems Format), Dateisenken
- Advanced Systems Format (ASF), Senken
- ASF (Advanced Systems Format), Senken
- senken,Dateisenken
- Dateisenken, Informationen
- Dateisenken, erstellen
- Dateisenken,Beenden
- Dateisenken, starten
- Dateisenken, schließen
- Senken, Statistiken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f94bd6698ca30a645957da36cf3b81a84f9d3e7c8ce6c598be2c39f8ac766db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196173"
---
# <a name="using-file-sinks"></a>Verwenden von Dateisenken

Unter normalen Umständen können Sie dem Writer einfach mithilfe der [**IWMWriter::SetOutputFilename-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) einen Ausgabedateinamen übergeben, und das Writer-Objekt schreibt die Datei automatisch auf den Datenträger. In diesem Fall erstellt und steuert der Writer tatsächlich ein Writer-Dateisenkenobjekt, das das Schreiben der Datei auf den Datenträger verarbeitet. Ein Writerdatei-Senkenobjekt steuert den Datenfluss vom Writer-Objekt zu einer einzelnen Datei.

Sie können eigene Dateisenken erstellen, um mehr Kontrolle darüber zu erhalten, wie die Senke die Datei schreibt. Sie können auch auf die Standard-Writerdateisenke zugreifen, die vom Writer als Reaktion auf einen Aufruf von **SetOutputFilename** erstellt wurde.

## <a name="creating-file-sinks"></a>Erstellen von Dateisenken

Führen Sie die folgenden Schritte aus, um eine Dateisenke zu erstellen und sie dem Writer hinzuzufügen.

1.  Erstellen Sie eine neue Senke, indem Sie die [**WMCreateWriterFileSink-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) aufrufen.
2.  Geben Sie einen Dateinamen für die Senke an, indem [**Sie IWMWriterFileSink::Open aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open)
3.  Fügen Sie dem Writer die Dateisenke hinzu, indem [**Sie IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink)aufrufen.
4.  Führen Sie das Schreiben auf die übliche Weise durch.
5.  Nachdem das Schreiben abgeschlossen ist, schließt die Senke die Datei automatisch.

## <a name="stopping-and-starting-file-sinks"></a>Beenden und Starten von Dateisenken

Nach Beginn der Schreibvorgänge können Sie das Schreiben in eine Dateisenke beenden, indem Sie [**IWMWriterFileSink2::Stop aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop)

Es gibt viele mögliche Gründe, warum Sie das Schreiben in eine Senke beenden möchten. Wenn Sie z. B. eine Aufzeichnung aus einer Livequelle erstellen, sind Sie möglicherweise nur an einem Teil des Inhalts interessiert.

Sie können das Schreiben in eine Dateisenke fortsetzen, indem [**Sie IWMWriterFileSink2::Start aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start) Sowohl **Stop** als auch **Start** verwenden Präsentationszeiten, um ungefähr zu steuern, wann der Befehl ausgeführt wird. Sie können die [**IWMWriterFileSink3-Methoden**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) verwenden, um mehr Kontrolle über Start- und Stoppzeiten zu erhalten.

## <a name="closing-file-sinks"></a>Schließen von Dateisenken

Normalerweise wird eine Dateisenke automatisch geschlossen. Wenn Sie das Schreiben in eine Senke abgeschlossen haben, aber die Schreibvorgänge in andere Senken fortgesetzt werden, sollten Sie die Senke explizit schließen, um Ressourcen zu sparen. Um eine Dateisenke zu schließen, rufen [**Sie IWMWriterFileSink2::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close)auf.

## <a name="getting-sink-statistics"></a>Abrufen von Senkenstatistiken

Sie können die Dateigröße und -dauer für eine geöffnete Senke abrufen, indem Sie [**IWMWriterFileSink2::GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) bzw. [**IWMWriterFileSink2::GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMWriterFileSink-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)
</dt> <dt>

[**IWMWriterFileSink2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)
</dt> <dt>

[**IWMWriterFileSink3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)
</dt> <dt>

[**Writer-Dateisenke (Objekt)**](writer-file-sink-object.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




