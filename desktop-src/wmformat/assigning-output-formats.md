---
title: Zuweisen von Ausgabeformaten
description: Zuweisen von Ausgabeformaten
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- Windows Medienformat-SDK, Zuweisen von Ausgabeformaten
- Advanced Systems Format (ASF), Zuweisen von Ausgabeformaten
- ASF (Advanced Systems Format), Zuweisen von Ausgabeformaten
- Advanced Systems Format (ASF), Ausgabenummern und Formate
- ASF (Advanced Systems Format), Ausgabenummern und Formate
- Ausgabenummern und Formate,Zuweisen
- Codecs, Ausgabenummern und Formate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80672419a032b2fff779259ffc6dcebfbe9e9a569f9d4b7afbb75ae5a84fac2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659370"
---
# <a name="assigning-output-formats"></a>Zuweisen von Ausgabeformaten

Einige Codecs können digitale Mediendaten in mehrere unkomprimierte Formate dekomprimieren. Sie finden alle unterstützten Formate für eine bestimmte Ausgabe entweder mit dem asynchronen Reader oder dem synchronen Reader.

Führen Sie die folgenden Schritte aus, um alle verfügbaren Formate für eine Ausgabe zu untersuchen. Diese Prozeduren sind für den asynchronen Reader und den synchronen Reader identisch. Wenn Schnittstellennamen variieren, werden die synchronen Readermethoden in Klammern nach den Methoden des asynchronen Readers aufgeführt.

1.  Erstellen Sie ein Readerobjekt, und laden Sie eine Datei zum Lesen. Weitere Informationen finden Sie unter [So erstellen Sie einen Reader und Öffnen einer Datei](to-create-a-reader-and-open-a-file.md) (oder So erstellen Sie einen [synchronen Reader und Öffnen einer Datei](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Bestimmen Sie die Ausgabe, für die Sie die verfügbaren Formate suchen möchten. Wenn Sie noch nicht wissen, welche Ausgabe Sie verwenden möchten, können Sie die Ausgaben in der Datei mithilfe der Verfahren unter [So identifizieren Sie Ausgabenummern identifizieren](to-identify-output-numbers.md)identifizieren.
3.  Rufen Sie die Gesamtzahl der verfügbaren Formate für die gewünschte Ausgabe ab, indem Sie [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (oder [**IWMSyncReader::GetOutputFormatCount)**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)aufrufen.
4.  Durchlaufen Sie die verfügbaren Formate einzeln, und führen Sie jeweils die folgenden Schritte aus:
    -   Rufen Sie die [**IWMOutputMediaProps-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) für das aktuelle Ausgabeformat ab, indem Sie [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (oder [**IWMSyncReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)) aufrufen.
    -   Rufen Sie die [**WM \_ MEDIA \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) für das Ausgabeformat ab, indem Sie zwei Aufrufe an [**IWMMediaProps::GetMediaType vornehmen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) Führen Sie den ersten Aufruf aus, um die Größe der -Struktur abzurufen, ordnen Sie ihr anschließend Speicher zu, und übergeben Sie beim zweiten Aufruf einen Zeiger auf den zugeordneten Speicher.
    -   Suchen Sie den Medienuntertyp des Ausgabeformats in **WM \_ MEDIA \_ TYPE.subtype**.
    -   Wenn der aktuelle Untertyp für Videos das Format ist, das Sie für die Ausgabe verwenden möchten, unterbrechen Sie die Schleife. Wechseln Sie andernfalls zur nächsten Iteration.

        Für Audiodaten müssen Sie die Werte in der **WAVEFORMATEX-Struktur** ihren Anforderungen entsprechend überprüfen. **WM \_ MEDIA \_ TYPE.pbFormat** zeigt auf die **WAVEFORMATEX-Struktur** für Audioausgaben.

5.  Wenn Sie die gewünschte Ausgabe gefunden haben, legen Sie sie für die Verwendung mit dem Reader fest, indem Sie [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (oder [**IWMSyncReader::SetOutputProps)**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)aufrufen. Sie müssen einen Zeiger an die **IWMOutputMediaProps-Schnittstelle** übergeben, die im ersten Schritt der Schleife abgerufen wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMMediaProps-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**IWMOutputMediaProps-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[**IWMReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMSyncReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Arbeiten mit Ausgaben**](working-with-outputs.md)
</dt> </dl>

 

 




