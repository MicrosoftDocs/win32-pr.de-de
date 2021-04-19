---
title: So identifizieren Sie Ausgabe Nummern
description: So identifizieren Sie Ausgabe Nummern
ms.assetid: a2135a71-52e6-4f62-8be8-b9886be9b37c
keywords:
- Windows Media-Format-SDK, Identifizieren von Ausgabe Nummern
- Advanced Systems Format (ASF), identifizierende Ausgabe Nummern
- ASF (Advanced Systems Format), Identifizieren von Ausgabe Nummern
- Advanced Systems Format (ASF), Ausgabe Nummern und Formate
- ASF (Advanced Systems Format), Ausgabe Nummern und Formate
- ausgabezahlen und Formate, identifizieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08f8e9a49d672efe7c04ecdde11ca4ef297d552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341504"
---
# <a name="to-identify-output-numbers"></a>So identifizieren Sie Ausgabe Nummern

Führen Sie die folgenden Schritte aus, um die Ausgabe Nummern für eine geladene Datei zu ermitteln. Diese Prozeduren sind sowohl für den asynchronen Reader als auch für den synchronen Reader identisch. Wenn Schnittstellennamen unterschiedlich sind, werden die synchronen Reader-Methoden nach den Methoden des asynchronen Readers in Klammern aufgelistet.

1.  Erstellen Sie ein Reader-Objekt, und laden Sie eine Datei zum Lesen. Weitere Informationen finden Sie unter so [Erstellen Sie einen Reader und öffnen eine Datei](to-create-a-reader-and-open-a-file.md) (oder [zum Erstellen eines synchronen Readers und Öffnen einer Datei](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Rufen Sie die Gesamtanzahl der Ausgaben für die Datei ab, indem Sie [**iwmreader:: getoutputcount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (oder [**iwmsyncreader:: getoutputcount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)) aufrufen.
3.  Führen Sie nacheinander die Ausgaben aus, und führen Sie jeweils die folgenden Schritte aus:
    -   Rufen Sie die [**iwmoutputmediadie**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) -Schnittstelle für die aktuelle Ausgabe mit einem Befehl von [**iwmreader:: getoutputrequi(**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) oder [**iwmsynkreader:: GetOutput-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)Eigenschaften) ab.
    -   Rufen Sie die [**WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur für die Ausgabe ab, indem Sie zwei Aufrufe an [**iwmmedia-Eigenschaften:: getmediatype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)durchführen. Führen Sie den ersten-Befehl aus, um die Größe der Struktur abzurufen, und weisen Sie dann Arbeitsspeicher zu, und übergeben Sie einen Zeiger auf den zugeordneten Speicher im zweiten-Befehl. Alternativ können Sie [**iwmmedia-Eigenschaften:: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype)aufrufen, das den Haupttyp übermittelt, ohne dass Sie Arbeitsspeicher für die **WM- \_ \_ Medientyp** Struktur zuweisen müssen. Sie können Ausgaben des falschen Haupt Typs überspringen.
    -   Rufen Sie den Haupt Medientyp und den Medien Untertyp aus der **WM- \_ \_ Medientyp** Struktur ab. Diese Werte werden in den Datenmembern **majortype** und **Untertyp** gespeichert.
    -   Überprüfen Sie den Wert von **WM \_ Media \_ Type. formatType**. Gibt den Typ der Struktur an, die im Puffer bei **WM \_ Media \_ Type. pbformat** enthalten ist. Weitere Informationen zu Format Typen finden Sie unter [Medientypen](media-types.md).
    -   Weisen Sie Arbeitsspeicher zu, um die Struktur des Typs zu speichern, der im vorherigen Schritt identifiziert wurde. Kopieren Sie die Struktur in den zugeordneten Arbeitsspeicher. Für Audiodaten und Videos bietet diese Struktur wichtige Informationen darüber, wie die Daten gerendert werden sollen.

Der synchrone Reader bietet auch Methoden zum Abrufen von Zuordnungen zwischen Ausgabe Nummern und streamnummern. Weitere Informationen [finden Sie unter so finden Sie streamnummern und Ausgabe Nummern](to-find-stream-numbers-and-output-numbers.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> <dt>

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

 

 




