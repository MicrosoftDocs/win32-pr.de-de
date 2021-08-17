---
title: So erzwingen sie Key-Frame Einfügen
description: So erzwingen sie Key-Frame Einfügen
ms.assetid: 456482da-aaa2-41f8-93f7-c0fa5abe7dd2
keywords:
- Advanced Systems Format (ASF), Erzwingen von Keyframeeinfügungen
- ASF (Advanced Systems Format), Erzwingen von Keyframeeinfügungen
- Advanced Systems Format (ASF), Keyframeeinfügungen
- ASF (Advanced Systems Format), Keyframeeinfügungen
- Keyframes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d400c0ee4ba97aa7de559b1394dbe5c9fb2a974c124924aeae0839b1b4dae0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196496"
---
# <a name="to-force-key-frame-insertion"></a>So erzwingen sie Key-Frame Einfügen

Der Windows Media Video 9-Codec unterstützt das erzwungene Einfügen von Keyframes. Wenn Sie ein Beispiel an den Writer übergeben, können Sie angeben, dass es als Keyframe [*codiert werden muss.*](wmformat-glossary.md)

Um das Einfügen eines Keyframes für ein Beispiel zu erzwingen, führen Sie die folgenden Schritte aus.

1.  Ordnen Sie einen Puffer zum Speichern des Beispiels zu, und rufen Sie einen Zeiger auf die [**INSSBuffer-Schnittstelle**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) ab, die den Puffer enthält, indem [**Sie IWMWriter::AllocateSample aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample)
2.  Rufen Sie den Speicherort und die Größe des in Schritt 1 erstellten Puffers ab, indem Sie [**INSSBuffer::GetBufferAndLength aufrufen.**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength)
3.  Kopieren Sie die Beispieldaten an die Pufferposition, und stellen Sie sicher, dass das übergebene Beispiel in den zugeordneten Puffer passt. Abhängig von der Quelle Ihrer Beispiele können Sie eine Vielzahl von Funktionen verwenden, um die Daten zu kopieren. Wenn Sie beispielsweise einen Stream aus einer AVI-Datei kopieren, können Sie die AVI-Funktion **AVIStreamRead verwenden.**
4.  Aktualisieren Sie die im Puffer verwendete Datenmenge, um die tatsächliche Größe des Beispiels widerzurufen, indem [**Sie INSSBuffer::SetLength aufrufen.**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength)
5.  Rufen Sie einen Zeiger auf die [**INSSBuffer3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) ab, indem Sie **INSSBuffer::QueryInterface aufrufen.**
6.  Legen Sie das Beispiel als erzwungenen Keyframe fest, indem Sie die [**INSSBuffer3::SetProperty-Methode**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) aufrufen, um die WM \_ SampleExtensionGUID \_ OutputCleanPoint-Eigenschaft festlegen. Diese Eigenschaft ist ein boolescher Wert. Legen Sie ihn auf **TRUE fest.**
7.  Übergeben Sie mithilfe der [**IWMWriter::WriteSample-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) die Pufferschnittstelle zusammen mit der Eingabenummer und der Stichprobenzeit an den Writer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)
</dt> <dt>

[**So schreiben Sie Beispiele**](to-write-samples.md)
</dt> <dt>

[**VBR-Codierung (Variable Bit Rate)**](variable-bit-rate--vbr--encoding.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




