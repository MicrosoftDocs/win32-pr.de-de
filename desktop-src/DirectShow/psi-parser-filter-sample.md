---
description: Beispiel für PSI-Parser-Filter
ms.assetid: e815d57f-25e5-4a71-8f40-e7abec0db236
title: Beispiel für PSI-Parser-Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1099375d2dbabf9ee6c8e891b0a1780bebbb599d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104555069"
---
# <a name="psi-parser-filter-sample"></a>Beispiel für PSI-Parser-Filter

## <a name="description"></a>BESCHREIBUNG

Der PSI-Parser-Filter empfängt Programm spezifische Informationen (PSI) aus einem MPEG-2-Transportstream und extrahiert Programminformationen aus der Programm Zuordnungs Tabelle (Page Association Table, Pat) und den Programm Zuordnungs Tabellen (PMT). Diese Informationen ermöglichen es einer Anwendung, den MPEG-2-Demultiplexer zu konfigurieren. Der Filter unterstützt eine benutzerdefinierte Schnittstelle, [**IMpeg2PsiParser**](impeg2psiparser.md), zum Abrufen der PSI-Informationen.

Dieser Filter ist für MPEG-2-Geräte (z. b. IEEE 1394 MPEG-2-Camcorder und D-VHS-Geräte) konzipiert. Weitere Informationen finden Sie unter [mstape-Treiber](mstape-driver.md) . Digitale TV-Broadcast Quellen sollten einen TIF-Filter verwenden, um Programminformationen zu erhalten.

## <a name="usage"></a>Verbrauch

Sie können den PSI-Parser-Filter in GraphEdit wie folgt testen:

1.  Starten Sie GraphEdit.
2.  Fügen Sie eine MPEG-2-transportquelle ein. MPEG-2-Camcorder und D-VHS-Geräte werden in der Kategorie Video Erfassungs Quellen als "Microsoft AV/C Tape subunit Device" angezeigt.
3.  Verbinden Sie den Quell Filter mit dem MPEG-2-Demultiplexer-Filter.
4.  Verwenden Sie die Eigenschaften Seite in der Demux, um eine Ausgabe-PIN mit dem Medientyp "MPEG-2 psi" zu erstellen. Diese PIN liefert die Abschnitte Pat und PMT.
5.  Verwenden Sie die Eigenschaften Seite Demux, um die PID 0x00 der Ausgabe-PIN zuzuordnen. Legen Sie den Inhaltstyp auf "MPEG2 PSI-Abschnitte" fest.
6.  Verbinden Sie die Demux-Ausgabe-PIN mit dem PSI-Parser, wie im folgenden Diagramm dargestellt.

    ![Diagramm des PSI-Parserfilters](images/psi-parser.png)

7.  Führen Sie das Diagramm aus, um psi-Daten an den PSI-Parser-Filter zu übergeben. Da der Filter die Pat-Abschnitte decodiert, ordnet er die PMT-PIDs automatisch derselben Ausgabepin in der Demux zu, sodass die PMT-Abschnitte empfangen werden.
8.  Verwenden Sie die Eigenschaften Seite "PSI-Parser", um eine Programmnummer auszuwählen. Die Liste der elementaren Datenströme auf der Eigenschaften Seite zeigt die PID und den Streamtyp an, die jedem elementaren Datenstrom im ausgewählten Programm zugeordnet sind. Die Eigenschaften Seite ist so konzipiert, dass in ISO/IEC 13818-1 definierte Streamtypen erkannt werden.
9.  Geben Sie die audiopid-Nummer in das Eingabefeld für die **audiopid** und die Video-PID-Nummer im Bearbeitungsfeld für die **Video-PID** ein.
10. Klicken Sie auf die Schaltfläche **Programm anzeigen** . Der PSI-Parser konfiguriert die Ausgabe Pins für die Demux so, dass Sie den Programm Datenstrom Informationen entsprechen und die Pins rendern.

> [!Note]  
> Die Eigenschaften Seite "PSI-Parser" wird bereitgestellt, um das Testen zu vereinfachen und Beispielcode bereitzustellen, mit dem der MPEG-2-Demultiplexer konfiguriert wird. Es wird nicht empfohlen, von Anwendungen zu verwenden. Anwendungen sollten das Programm gesteuert konfigurieren.

 

Um den PSI-Parser-Filter in einer Anwendung zu verwenden, müssen Sie zunächst das Filter Diagramm aus der MPEG-2-Quelle mit der MPEG-2-Komponente entwickeln. Der Code für diesen Schritt wird hier nicht angezeigt, da die genaue Diagramm Konfiguration von der Quelle abhängt.

Erstellen Sie als nächstes eine Ausgabe-PIN für die Demux-Datei für die PSI-Daten. Karten-PID 0x00, die für Pat-Abschnitte reserviert ist, zu dieser Pin, wie im folgenden Code gezeigt:


```C++
// Set the media type to MPEG-2 table sections.
AM_MEDIA_TYPE mt;
ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;

// Create the pin.
IPin *pPsiPin;
hr = pDemux->CreateOutputPin(&mt, L"PSI", &pPsiPin);
if (SUCCEEDED(hr))
{
    // Map to PID 0.
    ULONG Pid = 0x00;
    hr = pPid->MapPID(1, &Pid, MEDIA_MPEG2_PSI);
}
```



Weitere Informationen finden Sie unter [Verwenden des MPEG-2-demultiplexers](using-the-mpeg-2-demultiplexer.md).

Fügen Sie dem Diagramm den PSI-Parser-Filter hinzu, und verbinden Sie ihn mit der Ausgabe-PIN auf der Demux-Datei. Fragen Sie den PSI-Parser nach der [**IMpeg2PsiParser**](impeg2psiparser.md) -Schnittstelle ab. Führen Sie nun das Diagramm aus, und warten Sie auf geänderte Ereignisse von "EC- \_ Programm" \_ , die einen neuen Pat-oder PMT-Abschnitt Dieses Ereignis ist ein benutzerdefiniertes Ereignis, das vom PSI-Parser-Filter definiert wird. Wenn Sie ein \_ geändertes Ereignis vom Typ "EC-Programm" erhalten \_ , können Sie die verfügbaren PSI-Informationen abrufen, indem Sie **IMpeg2PsiParser** In diesem Abschnitt werden die Methoden beschrieben, die Sie am häufigsten benötigen.

Um die Anzahl der Programme zu erhalten, verwenden Sie die [**IMpeg2PsiParser:: getzählto fprograms**](impeg2psiparser-getcountofprograms.md) -Methode:


```C++
int NumProgs = 0;
hr = pPsi->GetCountOfPrograms(&NumProgs);
```



Um die Programmnummer für ein bestimmtes Programm abzurufen, verwenden Sie die [**IMpeg2PsiParser:: getrecordprogramnumber**](impeg2psiparser-getrecordprogramnumber.md) -Methode:


```C++
WORD ProgNum = 0;
for (int i = 0; i < NumProgs; i++)
{
    hr = pPsi->GetRecordProgramNumber(i, &ProgNum);
    ...
}
```



Die Programmnummer dient zum Abrufen der PMT-Einträge für einzelne Programme. Um die Anzahl der elementaren Datenströme in einem Programm zu erhalten, verwenden Sie die [**getzähltofelementarystreams**](impeg2psiparser-getcountofelementarystreams.md) -Methode:


```C++
WORD cElemStreams = 0;
hr = pPsi->GetCountOfElementaryStreams(ProgNum, &cElemStreams);
```



Für jeden elementaren Stream gibt die [**IMpeg2PsiParser:: getrecorschementarypid**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) -Methode die PID zurück, und die [**IMpeg2PsiParser:: getrecordstreamtype**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) -Methode gibt den Streamtyp zurück:


```C++
BYTE ESType = 0;
WORD ESPid = 0;
for (WORD j = 0; j < cElemStreams; j++)
{
    hr = pPsi->GetRecordElementaryPid(ProgNum, j, &ESPid);
    hr = pPsi->GetRecordStreamType(ProgNum, j, &ESType);
}
```



Die PID und der Streamtyp ermöglichen es Ihnen, neue Ausgabe Pins für den MPEG-2-Demultiplexer zu konfigurieren. Dies erfordert möglicherweise einige Kenntnisse der ursprünglichen Quelle. ISO/IEC 13818-1 definiert z. b. die Streamtypen 0x80 bis 0xFF als "Benutzer privat", aber andere auf MPEG-2 basierende Standards können diesen Typen andere Bedeutungen zuweisen.

Der MPEG-2-Demultiplexer kann während der Ausführung des Diagramms neue Pins und neue PID-Zuordnungen erstellen, aber Sie müssen das Diagramm zum Verbinden von Pins unterbinden.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK Root \]* \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ psiparser.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> <dt>

[**IMpeg2PsiParser-Schnittstelle**](impeg2psiparser.md)
</dt> </dl>

 

 
