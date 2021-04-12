---
title: So erzwingen Sie Key-Frame einfügen
description: So erzwingen Sie Key-Frame einfügen
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- Advanced Systems Format (ASF), Erzwingen von Tasten Frame-Einfügungen
- ASF (Advanced Systems Format), Erzwingen von Tasten Frame-Einfügungen
- Advanced Systems Format (ASF), Keyframe-Einfügungen
- ASF (Advanced Systems Format), Keyframe-Einfügungen
- Keyframes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23006eef1e51d8bc63f2d55cac22e09a2052d83e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104472389"
---
# <a name="to-force-key-frame-insertion"></a>So erzwingen Sie Key-Frame einfügen

Der Windows Media Video 9-Codec unterstützt erzwungene Keyframe-Einfügevorgänge. Wenn Sie ein Beispiel an den Writer übergeben, können Sie angeben, dass es als [*Keyframe*](wmformat-glossary.md)codiert werden muss.

Führen Sie die folgenden Schritte aus, um das Einfügen von Schlüsseln für ein Beispiel zu erzwingen.

1.  Weisen Sie einen Puffer zum Speichern des Beispiels zu, und rufen Sie einen Zeiger auf die [**inssbuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) -Schnittstelle ab, die den Puffer durch Aufrufen von [**iwmwriter:: allopriesample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample)enthält.
2.  Rufen Sie den Speicherort und die Größe des Puffers ab, der in Schritt 1 erstellt wurde, indem Sie [**inssbuffer:: getbufferandlength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength)aufrufen.
3.  Kopieren Sie die Beispiel Daten in den Puffer Speicherort, und stellen Sie sicher, dass das Beispiel erfolgreich in den zugeordneten Puffer passt. Abhängig von der Quelle der Beispiele können Sie eine Vielzahl von Funktionen verwenden, um die Daten zu kopieren. Wenn Sie z. b. einen Stream aus einer AVI-Datei kopieren, können Sie die AVI-Funktion **avistreamread** verwenden.
4.  Aktualisieren Sie die im Puffer verwendete Datenmenge, um die tatsächliche Größe des Beispiels durch Aufrufen von " [**inssbuffer:: SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength)" widerzuspiegeln.
5.  Abrufen eines Zeigers auf die [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) -Schnittstelle durch Aufrufen von " **inssbuffer:: QueryInterface**".
6.  Legen Sie das Beispiel als erzwungener Keyframe fest, indem Sie die [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) -Methode aufrufen, um die "WM \_ sampleextensionguid \_ outputcleanpoint"-Eigenschaft festzulegen. Diese Eigenschaft ist ein boolescher Wert. Legen Sie diese Einstellung auf **true** fest.
7.  Übergeben Sie die Puffer Schnittstelle zusammen mit der Eingabe Nummer und der Beispiel Zeit mithilfe der Methode [**iwmwriter:: schreitesample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) an den Writer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmwriter:: schreitesample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[**So schreiben Sie Beispiele**](to-write-samples.md)
</dt> <dt>

[**Codierung der Variablen Bitrate (VBR)**](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




