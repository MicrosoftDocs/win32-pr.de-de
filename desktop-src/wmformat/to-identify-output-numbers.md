---
title: So identifizieren Sie Ausgabenummern
description: So identifizieren Sie Ausgabenummern
ms.assetid: a2135a71-52e6-4f62-8be8-b9886be9b37c
keywords:
- Windows Medienformat-SDK, Identifizieren von Ausgabenummern
- Advanced Systems Format (ASF), Identifizieren von Ausgabenummern
- ASF (Advanced Systems Format), Identifizieren von Ausgabenummern
- Advanced Systems Format (ASF), Ausgabenummern und Formate
- ASF (Advanced Systems Format), Ausgabenummern und Formate
- Ausgabenummern und -formate, Identifizieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c601481520632806ac56e12e16e1474336897d1be341c9d19df8e235d6355ab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699380"
---
# <a name="to-identify-output-numbers"></a>So identifizieren Sie Ausgabenummern

Führen Sie die folgenden Schritte aus, um die Ausgabenummern für eine geladene Datei zu identifizieren. Diese Prozeduren sind für den asynchronen Reader und den synchronen Reader identisch. Wenn Schnittstellennamen variieren, werden die synchronen Readermethoden in Klammern nach den Methoden des asynchronen Readers aufgelistet.

1.  Erstellen Sie ein Readerobjekt, und laden Sie eine Datei zum Lesen. Weitere Informationen finden Sie unter So erstellen Sie [einen Reader und Öffnen](to-create-a-reader-and-open-a-file.md) einer Datei (oder So erstellen Sie einen [synchronen Reader und Öffnen einer Datei](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Rufen Sie die Gesamtanzahl der Ausgaben für die Datei ab, indem Sie [**IWMReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (oder [**IWMSyncReader::GetOutputCount) aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)
3.  Führen Sie eine Schleife durch die Ausgaben nacheinander aus, und führen Sie jeweils die folgenden Schritte aus:
    -   Rufen Sie [**die IWMOutputMediaProps-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) für die aktuelle Ausgabe mit einem Aufruf von [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (oder [**IWMSyncReader::GetOutputProps)**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)ab.
    -   Rufen Sie die [**WM \_ MEDIA \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) für die Ausgabe ab, indem Sie zwei Aufrufe von [**IWMMediaProps::GetMediaType tätigen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) Nehmen Sie den ersten Aufruf vor, um die Größe der Struktur zu erhalten, ordnen Sie dann Arbeitsspeicher zu, und übergeben Sie beim zweiten Aufruf einen Zeiger auf den zugeordneten Arbeitsspeicher. Alternativ können Sie [**IWMMediaProps::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype)aufrufen, das den Haupttyp liefert, ohne dass Sie Arbeitsspeicher für die **WM \_ MEDIA \_ TYPE-Struktur zuordnen** müssen. Sie können Ausgaben des falschen Haupttyps überspringen.
    -   Rufen Sie den Hauptmedientyp und medienuntertyp aus der **WM \_ MEDIA \_ TYPE-Struktur** ab. Diese Werte werden in den Daten members **majortype bzw.** **subtype** gespeichert.
    -   Überprüfen Sie den Wert von **WM \_ MEDIA \_ TYPE.formattype**. Dies gibt den Typ der -Struktur an, die im Puffer in **WM \_ MEDIA \_ TYPE.pbFormat enthalten ist.** Weitere Informationen zu Formattypen finden Sie unter [Medientypen.](media-types.md)
    -   Ordnen Sie Arbeitsspeicher zu, um die Struktur des im vorherigen Schritt identifizierten Typs zu halten. Kopieren Sie die -Struktur in den zugeordneten Arbeitsspeicher. Bei Audio- und Videoinhalten erhalten Sie mit dieser Struktur wichtige Informationen dazu, wie die Daten gerendert werden sollen.

Der synchrone Reader stellt auch Methoden zum Abrufen von Zuordnungen zwischen Ausgabenummern und Datenstromnummern zur Verwendung. Weitere Informationen finden Sie unter [So suchen Sie Streamnummern und Ausgabenummern.](to-find-stream-numbers-and-output-numbers.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Eingaben, Streams und Ausgaben**](inputs-streams-and-outputs.md)
</dt> <dt>

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

 

 




