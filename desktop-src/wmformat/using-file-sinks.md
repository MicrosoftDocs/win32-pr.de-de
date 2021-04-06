---
title: Verwenden von Dateisenken
description: Verwenden von Dateisenken
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- Advanced Systems Format (ASF), Datei senken
- ASF (Advanced Systems Format), Datei senken
- Advanced Systems Format (ASF), senken
- ASF (Advanced Systems Format), senken
- senken, Datei senken
- Datei senken, Informationen zu
- Datei senken, erstellen
- Datei senken, beenden
- Datei senken, starten
- Datei senken, schließen
- senken, Statistiken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7a7f09a08788128719ea80a2a06d339f6398e6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101343"
---
# <a name="using-file-sinks"></a>Verwenden von Dateisenken

Normalerweise können Sie dem Writer einfach einen Ausgabe Dateinamen mithilfe der [**iwmwriter:: setoutputfilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) -Methode übergeben, und das Writer-Objekt schreibt die Datei automatisch auf den Datenträger. In diesem Fall erstellt und steuert der Writer tatsächlich ein Writer-Datei-Sink-Objekt, das das Schreiben der Datei auf den Datenträger behandelt. Ein Writer-Datei-Senkenobjekt steuert den Datenfluss vom Writer-Objekt zu einer einzelnen Datei.

Sie können eigene dateisenken erstellen, um mehr Kontrolle darüber zu erhalten, wie die Senke die Datei schreibt. Sie können auch auf die standardmäßige Writer-Datei-Senke zugreifen, die vom Writer als Reaktion auf einen Aufrufen von **setoutputfilename** erstellt wurde.

## <a name="creating-file-sinks"></a>Erstellen von Datei senken

Führen Sie die folgenden Schritte aus, um eine Datei Senke zu erstellen und Sie dem Writer hinzuzufügen.

1.  Erstellen Sie eine neue Senke, indem Sie die [**wmcreateschreiterfilesink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) -Funktion aufrufen.
2.  Geben Sie einen Dateinamen für die Senke an, indem Sie [**iwmschreiterfilesink:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open)aufrufen.
3.  Fügen Sie dem Writer die File-Senke hinzu, indem Sie [**iwmschreiteradvanced:: addsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink)aufrufen.
4.  Führen Sie Schreibvorgänge auf die übliche Weise aus.
5.  Nachdem das Schreiben abgeschlossen ist, wird die Datei automatisch von der Senke geschlossen.

## <a name="stopping-and-starting-file-sinks"></a>Beenden und starten von Datei senken

Nachdem das Schreiben von Vorgängen begonnen hat, können Sie das Schreiben in eine Datei Senke durch Aufrufen von [**IWMWriterFileSink2:: Beendigung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop)abbrechen.

Es gibt viele mögliche Gründe, warum das Schreiben in eine Senke beendet werden soll. Wenn Sie z. b. von einer Live Quelle aufzeichnen, sind Sie möglicherweise nur an einem Teil des Inhalts interessiert.

Sie können das Schreiben in eine Datei Senke fortsetzen, indem Sie [**IWMWriterFileSink2:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start)aufrufen. Sowohl **Beenden** als auch **starten** verwenden Präsentations Zeiten, um ungefähr zu steuern, wann der Befehl ausgeführt wird. Sie können die [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) -Methoden verwenden, um mehr Kontrolle über Start-und Endzeit Zeiten zu erhalten.

## <a name="closing-file-sinks"></a>Schließen von Datei senken

Normalerweise wird eine Datei Senke automatisch geschlossen. Wenn Sie mit dem Schreiben in eine Senke fertig sind, aber das Schreiben von Vorgängen in andere senken fortgesetzt wird, sollten Sie die Senke explizit schließen, um Ressourcen zu sparen. Um eine File-Senke zu schließen, nennen Sie [**IWMWriterFileSink2:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).

## <a name="getting-sink-statistics"></a>Senke Statistiken werden erhalten

Sie können die Dateigröße und-Dauer für eine geöffnete Senke abrufen, indem Sie [**IWMWriterFileSink2:: GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) und [**IWMWriterFileSink2:: getfileduration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmschreiterfilesink-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)
</dt> <dt>

[**IWMWriterFileSink2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)
</dt> <dt>

[**IWMWriterFileSink3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)
</dt> <dt>

[**Writer-Dateisenke (Objekt)**](writer-file-sink-object.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




