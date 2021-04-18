---
title: Zuweisen von Ausgabeformaten
description: Zuweisen von Ausgabeformaten
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- Windows Media-Format-SDK, Zuweisen von Ausgabeformaten
- Advanced Systems Format (ASF), Zuweisen von Ausgabeformaten
- ASF (Advanced Systems Format), Zuweisen von Ausgabeformaten
- Advanced Systems Format (ASF), Ausgabe Nummern und Formate
- ASF (Advanced Systems Format), Ausgabe Nummern und Formate
- ausgabezahlen und Formate, zuweisen
- Codecs, Ausgabe Nummern und Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633673053a2b34a2f7aed5ed3f6ae66457a7ee13
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "106337833"
---
# <a name="assigning-output-formats"></a>Zuweisen von Ausgabeformaten

Einige Codecs können digitale Mediendaten in mehrere nicht komprimierte Formate decoeinigen. Sie können alle unterstützten Formate für eine bestimmte Ausgabe mit dem asynchronen Reader oder dem synchronen Reader finden.

Um alle verfügbaren Formate für eine Ausgabe zu überprüfen, führen Sie die folgenden Schritte aus. Diese Prozeduren sind sowohl für den asynchronen Reader als auch für den synchronen Reader identisch. Wenn Schnittstellennamen unterschiedlich sind, werden die synchronen Reader-Methoden nach den Methoden des asynchronen Readers in Klammern aufgelistet.

1.  Erstellen Sie ein Reader-Objekt, und laden Sie eine Datei zum Lesen. Weitere Informationen finden Sie unter so [Erstellen Sie einen Reader und öffnen eine Datei](to-create-a-reader-and-open-a-file.md) (oder [zum Erstellen eines synchronen Readers und Öffnen einer Datei](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Bestimmen Sie die Ausgabe, für die Sie die verfügbaren Formate suchen möchten. Wenn Sie nicht bereits wissen, welche Ausgabe Sie verwenden möchten, können Sie die Ausgaben in der Datei mithilfe der Prozeduren in identifizieren, [um Ausgabe Nummern zu identifizieren](to-identify-output-numbers.md).
3.  Rufen Sie die Gesamtanzahl der verfügbaren Formate für die gewünschte Ausgabe ab, indem Sie [**iwmreader:: getoutputformatcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (oder [**iwmsyncreader:: getoutputformatcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)) aufrufen.
4.  Durchlaufen Sie die verfügbaren Formate nacheinander, indem Sie die folgenden Schritte ausführen:
    -   Rufen Sie die [**iwmoutputmediadie**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) -Schnittstelle für das aktuelle Ausgabeformat durch Aufrufen von [**iwmreader:: getoutputformat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (oder [**iwmsyncreader:: getoutputformat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)) ab.
    -   Rufen Sie die [**WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur für das Ausgabeformat ab, indem Sie zwei Aufrufe an [**iwmmedia-Eigenschaften:: getmediatype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)durchführen. Führen Sie den ersten-Befehl aus, um die Größe der Struktur abzurufen, und weisen Sie dann Arbeitsspeicher zu, und übergeben Sie einen Zeiger auf den zugeordneten Speicher im zweiten-Befehl.
    -   Suchen Sie den Medien Untertyp des Ausgabeformats in **WM \_ Media \_ Type. Untertyp**.
    -   Wenn es sich bei dem aktuellen Untertyp um das Format handelt, das Sie für die Ausgabe verwenden möchten, brechen Sie die Schleife aus. Andernfalls wechseln Sie zur nächsten Iterationen.

        Für Audiodaten müssen Sie die Werte in der **WaveFormatEx** -Struktur hinsichtlich ihrer Anforderungen überprüfen. **WM \_ \_Medientyp. pbformat** verweist auf die **WaveFormatEx** -Struktur für Audioausgaben.

5.  Wenn Sie die gewünschte Ausgabe gefunden haben, legen Sie Sie für die Verwendung mit dem Reader fest, indem Sie [**iwmreader:: SetOutput-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) Eigenschaften (oder [**iwmsyncreader:: SetOutput-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)Eigenschaften) aufrufen. Sie müssen einen Zeiger an die **iwmoutputmedia-** Schnittstelle übergeben, die im ersten Schritt der Schleife abgerufen wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmmedia-Eigenschaften Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**Iwmoutputmediadie-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[**Iwmreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Iwmsynkreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Arbeiten mit Ausgaben**](working-with-outputs.md)
</dt> </dl>

 

 




