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
- Ausgabenummern und Formate,Identifizieren
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

Führen Sie die folgenden Schritte aus, um die Ausgabenummern für eine geladene Datei zu identifizieren. Diese Prozeduren sind für den asynchronen Reader und den synchronen Reader identisch. Wenn Schnittstellennamen variieren, werden die synchronen Readermethoden in Klammern nach den Methoden des asynchronen Readers aufgeführt.

1.  Erstellen Sie ein Readerobjekt, und laden Sie eine Datei zum Lesen. Weitere Informationen finden Sie unter [So erstellen Sie einen Reader und Öffnen einer Datei](to-create-a-reader-and-open-a-file.md) (oder So erstellen Sie einen [synchronen Reader und Öffnen einer Datei](to-create-a-synchronous-reader-and-open-a-file.md)).
2.  Rufen Sie die Gesamtzahl der Ausgaben für die Datei ab, indem [**Sie IWMReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (oder [**IWMSyncReader::GetOutputCount)**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)aufrufen.
3.  Durchlaufen Sie die Ausgaben einzeln, und führen Sie jeweils die folgenden Schritte aus:
    -   Rufen Sie die [**IWMOutputMediaProps-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) für die aktuelle Ausgabe mit einem Aufruf von [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (oder [**IWMSyncReader::GetOutputProps)**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)ab.
    -   Rufen Sie die [**WM \_ MEDIA \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) für die Ausgabe ab, indem Sie zwei Aufrufe an [**IWMMediaProps::GetMediaType vornehmen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) Führen Sie den ersten Aufruf aus, um die Größe der -Struktur abzurufen, ordnen Sie ihr anschließend Speicher zu, und übergeben Sie beim zweiten Aufruf einen Zeiger auf den zugeordneten Speicher. Alternativ können Sie [**IWMMediaProps::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype)aufrufen, wodurch der Haupttyp bereitgestellt wird, ohne dass Sie Speicher für die **WM \_ MEDIA \_ TYPE-Struktur** zuordnen müssen. Sie können Ausgaben des falschen Haupttyps überspringen.
    -   Rufen Sie den Hauptmedientyp und den Medienuntertyp aus der **WM \_ MEDIA \_ TYPE-Struktur** ab. Diese Werte werden in den **Datenmembern majortype** bzw. **subtype** gespeichert.
    -   Überprüfen Sie den Wert von **WM \_ MEDIA \_ TYPE.formattype**. Dies gibt den Typ der Struktur an, die im Puffer unter **WM \_ MEDIA \_ TYPE.pbFormat** enthalten ist. Weitere Informationen zu Formattypen finden Sie unter [Medientypen.](media-types.md)
    -   Belegen Sie Arbeitsspeicher, um die Struktur des im vorherigen Schritt identifizierten Typs zu speichern. Kopieren Sie die -Struktur in den zugeordneten Arbeitsspeicher. Bei Audio- und Videodaten bietet diese Struktur wichtige Informationen dazu, wie die Daten gerendert werden sollen.

Der synchrone Reader stellt auch Methoden zum Abrufen von Zuordnungen zwischen Ausgabe- und Streamnummern bereit. Weitere Informationen finden Sie unter [To Find Stream Numbers and Output Numbers](to-find-stream-numbers-and-output-numbers.md).

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

 

 




