---
description: PSI Parser-Filterbeispiel
ms.assetid: e815d57f-25e5-4a71-8f40-e7abec0db236
title: PSI Parser-Filterbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de960d36900a417212cdd34ac795b504d4ad073ccd61619ffad110d5fe125fad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747924"
---
# <a name="psi-parser-filter-sample"></a>PSI Parser-Filterbeispiel

## <a name="description"></a>Beschreibung

Der PSI-Parserfilter empfängt programmspezifische Informationen (Program Specific Information, PSI) aus einem MPEG-2-Transportstream und extrahiert Programminformationen aus der Program Association Table (PAT) und den Program Map Tables (PMT). Diese Informationen ermöglichen einer Anwendung das Konfigurieren des MPEG-2-Demultiplexers. Der Filter unterstützt eine benutzerdefinierte Schnittstelle, [**IMpeg2PsiParser,**](impeg2psiparser.md)zum Abrufen der PSI-Informationen.

Dieser Filter ist für MPEG-2-Geräte wie IEEE 1394 MPEG-2-Tablets und D-VHS-Geräte konzipiert. Weitere Informationen finden Sie unter [MSTape-Treiber.](mstape-driver.md) Quellen für digitale Fernsehsendungen sollten einen TIF-Filter verwenden, um Programminformationen abzurufen.

## <a name="usage"></a>Verbrauch

Sie können den PSI-Parserfilter in GraphEdit wie folgt testen:

1.  Starten Sie GraphEdit.
2.  Fügen Sie eine MPEG-2-Transportquelle ein. MPEG-2-Bands und D-VHS-Geräte werden in der Kategorie Videoaufnahmequellen als "Microsoft AV/C Tape Subunit Device" angezeigt.
3.  Verbinden den Quellfilter an den MPEG-2 Demultiplexer-Filter.
4.  Verwenden Sie die Eigenschaftenseite auf der Demux, um einen Ausgabepin mit dem Medientyp "MPEG-2 PSI" zu erstellen. Mit dieser Stecknadel werden die Abschnitte PAT und PMT übermittelt.
5.  Verwenden Sie die Eigenschaftenseite demux, um pid 0x00 dem Ausgabepin zuzuordnen. Legen Sie den Inhaltstyp auf "MPEG2 PSI Sections" fest.
6.  Verbinden den Demux-Ausgabepin an psi Parser an, wie im folgenden Diagramm dargestellt.

    ![Psi-Parserfilterdiagramm](images/psi-parser.png)

7.  Führen Sie das Diagramm aus, um PSI-Daten an den PSI-Parserfilter zu leiten. Wenn der Filter die PAT-Abschnitte decodiert, ordnet er die PMT-PIDs automatisch demselben Ausgabepin auf der Demux zu, sodass er die PMT-Abschnitte empfängt.
8.  Verwenden Sie die Eigenschaftenseite PSI Parser, um eine Programmnummer auszuwählen. Die elementare Streamliste auf der Eigenschaftenseite zeigt die PID und den Streamtyp an, die jedem elementaren Stream im ausgewählten Programm zugeordnet sind. Die Eigenschaftenseite wurde entwickelt, um in ISO/IEC 13818-1 definierte Streamtypen zu erkennen.
9.  Geben Sie die PiD-Audionummer im Bearbeitungsfeld **Audio PID** und die PiD-Nummer des Videos in das Bearbeitungsfeld **Video PID** ein.
10. Klicken Sie auf die Schaltfläche **Programm anzeigen.** Der PSI-Parser konfiguriert die Ausgabepins auf der Demux so, dass sie den Programmstreaminformationen entsprechen, und rendert die Pins.

> [!Note]  
> Die Psi Parser-Eigenschaftenseite wird bereitgestellt, um das Testen zu vereinfachen und Beispielcode bereitzustellen, der den MPEG-2-Demultiplexer konfiguriert. Die Verwendung von Anwendungen wird nicht empfohlen. Anwendungen sollten die Demux programmgesteuert konfigurieren.

 

Um den PSI-Parserfilter in einer Anwendung zu verwenden, erstellen Sie zunächst den Filtergraphen von der MPEG-2-Quelle bis zur MPEG-2-Demux. Der Code für diesen Schritt wird hier nicht angezeigt, da die genaue Graphkonfiguration von der Quelle abhängt.

Erstellen Sie als Nächstes einen Ausgabepin auf dem Demux für die PSI-Daten. Ordnen Sie diesem Pin pid 0x00 zu, der für PAT-Abschnitte reserviert ist, wie im folgenden Code gezeigt:


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



Weitere Informationen finden Sie unter [Verwenden des MPEG-2-Demultiplexers.](using-the-mpeg-2-demultiplexer.md)

Fügen Sie dem Diagramm den PSI-Parserfilter hinzu, und verbinden Sie ihn mit dem Ausgabepin auf der Demux. Fragen Sie den PSI-Parser nach der [**IMpeg2PsiParser-Schnittstelle**](impeg2psiparser.md) ab. Führen Sie nun das Diagramm aus, und warten Sie auf EC \_ PROGRAM \_ CHANGED-Ereignisse, die einen neuen PAT- oder PMT-Abschnitt signalisieren. Dieses Ereignis ist ein benutzerdefiniertes Ereignis, das vom PSI-Parserfilter definiert wird. Wenn Sie ein EC \_ PROGRAM \_ CHANGED-Ereignis erhalten, können Sie die verfügbaren PSI-Informationen abrufen, indem Sie **IMpeg2PsiParser-Methoden** aufrufen. In diesem Abschnitt werden die Methoden beschrieben, die Sie am häufigsten benötigen.

Verwenden Sie die [**IMpeg2PsiParser::GetCountOfPrograms-Methode,**](impeg2psiparser-getcountofprograms.md) um die Anzahl der Programme abzurufen:


```C++
int NumProgs = 0;
hr = pPsi->GetCountOfPrograms(&NumProgs);
```



Verwenden Sie die [**IMpeg2PsiParser::GetRecordProgramNumber-Methode,**](impeg2psiparser-getrecordprogramnumber.md) um die Programmnummer für ein bestimmtes Programm abzurufen:


```C++
WORD ProgNum = 0;
for (int i = 0; i < NumProgs; i++)
{
    hr = pPsi->GetRecordProgramNumber(i, &ProgNum);
    ...
}
```



Die Programmnummer wird verwendet, um die PMT-Einträge für einzelne Programme abzurufen. Verwenden Sie die [**GetCountOfElementaryStreams-Methode,**](impeg2psiparser-getcountofelementarystreams.md) um die Anzahl elementarer Streams in einem Programm abzurufen:


```C++
WORD cElemStreams = 0;
hr = pPsi->GetCountOfElementaryStreams(ProgNum, &cElemStreams);
```



Für jeden elementaren Stream gibt die [**IMpeg2PsiParser::GetRecordElementaryPid-Methode**](/previous-versions/windows/desktop/legacy/dd376623(v=vs.85)) die PID zurück, und die [**IMpeg2PsiParser::GetRecordStreamType-Methode**](/previous-versions/windows/desktop/legacy/dd376626(v=vs.85)) gibt den Streamtyp zurück:


```C++
BYTE ESType = 0;
WORD ESPid = 0;
for (WORD j = 0; j < cElemStreams; j++)
{
    hr = pPsi->GetRecordElementaryPid(ProgNum, j, &ESPid);
    hr = pPsi->GetRecordStreamType(ProgNum, j, &ESType);
}
```



Mit der PID und dem Streamtyp können Sie neue Ausgabepins auf dem MPEG-2-Demultiplexer konfigurieren. Dies kann einige Kenntnisse der ursprünglichen Quelle erfordern. Beispielsweise definiert ISO/IEC 13818-1 Streamtypen, die über 0xFF 0x80, als "benutzer privat", aber andere Standards, die auf MPEG-2 basieren, weisen diesen Typen möglicherweise andere Bedeutungen zu.

Der MPEG-2-Demultiplexer kann neue Pins und neue PID-Zuordnungen erstellen, während das Diagramm ausgeführt wird. Sie müssen das Diagramm jedoch beenden, um Pins zu verbinden.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Um die DirectShow SDK-Beispiele herunterzuladen, installieren Sie die neueste Version des [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Dieses Beispiel wird unter folgendem Pfad installiert: *\[ \] SDK-Stammbeispiele* \\ Multimedia \\ \\ DirectShow Filters \\ \\ PSIParser.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> <dt>

[**IMpeg2PsiParser-Schnittstelle**](impeg2psiparser.md)
</dt> </dl>

 

 
