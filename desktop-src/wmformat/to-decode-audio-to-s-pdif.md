---
title: So decodieren Sie Audiodaten in S/PDIF
description: So decodieren Sie Audiodaten in S/PDIF
ms.assetid: b56c2d0a-a7c6-44f8-832a-bbbe7ae053e6
keywords:
- Windows Media-Format-SDK, Decodieren von Audiodaten in S/PDIF
- Windows Media-Format-SDK, digitales Microsoft/Philips Digital Interconnect-Format (S/PDIF)
- Advanced Systems Format (ASF), Decodierung von Audiodaten in S/PDIF
- ASF (Advanced Systems Format), Decodierung von Audiodaten in S/PDIF
- Advanced Systems Format (ASF), digitales, digitales Interconnect-Format (S/PDIF) von Sony/Philips
- ASF (Advanced Systems Format), digitales digitales Interconnect-Format (S/PDIF) von Sony/Philips
- Digitales Interconnect-Format (S/PDIF) für Sony/Philips, Decodierung von Audiodaten
- S/PDIF (Sony/Philips Digital Interconnect-Format), Decodierung von Audiodaten
- Decodieren von Audiodateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33fa063baa8e9a88c2fb7a4d9c67375965282167
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724102"
---
# <a name="to-decode-audio-to-spdif"></a>So decodieren Sie Audiodaten in S/PDIF

Mit dem Windows Media Audio 9 Professional-Codec codierte Audiodaten können im Digital/Philips Digital Interconnect-Format (S/PDIF) decodiert werden. Führen Sie die folgenden Schritte aus, um die S/PDIF-Ausgabe zu generieren:

1.  Öffnen Sie eine Datei, die einen Windows Media Audio 9 Professional-Stream enthält, indem Sie die [**iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) -Methode aufrufen.
2.  Identifizieren Sie die Ausgabe Nummer des Datenstroms, den Sie möchten. Weitere Informationen finden [Sie unter So identifizieren Sie Ausgabe Nummern](to-identify-output-numbers.md).
3.  Aufrufen der [**IWMReaderAdvanced2:: setoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) -Methode, um die S/PDIF-Ausgabe zu konfigurieren. Verwenden Sie \_ für den Einstellungs Namen g wszene ablewmaprospdif Output. Der Datentyp ist vom **WMT- \_ Typ \_ bool**. Legen Sie den Wert auf **true** fest, um die S/PDIF-Ausgabe zu aktivieren.
4.  Rufen Sie die Schnittstelle der Ausgabe Eigenschaften ([**iwmoutputmediaproperties**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)) des gewünschten Ausgabeformats ab, indem Sie die [**iwmreader:: getoutputformat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) -Methode aufrufen. Weitere Informationen zum Aufzählen von Ausgabeformaten finden Sie unter [Zuweisen von Ausgabeformaten](assigning-output-formats.md).
5.  Legen Sie das Ausgabeformat fest, indem Sie die [**iwmreader:: setoutputrequiemethode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) aufrufen. Übergeben Sie einen Zeiger auf die **iwmoutputmedia-** Oberfläche, die Sie in Schritt 4 abgerufen haben.
6.  Nehmen Sie andere Konfigurationsänderungen vor, und starten Sie die Wiedergabe.

> [!Note]  
> Sie können die vorangehenden Schritte auf dem synchronen Reader ausführen, indem Sie die entsprechenden Methoden der [**iwmsynkreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) -Schnittstelle verwenden.

 

Der folgende Beispielcode veranschaulicht, wie Sie einen Audiostream festlegen, um Audiodaten als S/PDIF-Daten auszugeben. Diese Funktion setzt voraus, dass eine Datei bereits in den Reader geladen wurde und dass die Ausgabe Nummer identifiziert wurde. Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).


```C++
HRESULT SetSPDIF(DWORD dwOutputNum, IWMReader* pReader)
{
    HRESULT hr = S_OK;

    IWMReaderAdvanced2*  pReaderAdv   = NULL;
    IWMOutputMediaProps* pOutputProps = NULL; 

    BOOL fValue = TRUE;

    // Get the advanced reader interface.
    hr = pReader->QueryInterface(IID_IWMReaderAdvanced2,
                                 (void**)&pReaderAdv);
    GOTO_EXIT_IF_FAILED(hr);

    // Set S/PDIF output.
    hr = pReaderAdv->SetOutputSetting(dwOutputNum, 
                                      g_wszEnableWMAProSPDIFOutput, 
                                      WMT_TYPE_BOOL, 
                                      (BYTE*)&fValue, 
                                      sizeof(BOOL));
    GOTO_EXIT_IF_FAILED(hr);

    // Get the first output format for the stream.
    // NOTE: You could also enumerate the available output formats
    // and pick one to use.

    hr = pReader->GetOutputFormat(dwOutputNum, 0, &pOutputProps);
    GOTO_EXIT_IF_FAILED(hr);

    // Set the output properties back on the reader.
    hr = pReader->SetOutputProps(dwOutputNum, pOutputProps);

Exit:
    SAFE_RELEASE(pReaderAdv);
    SAFE_RELEASE(pOutputProps);

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erweiterte Themen**](advanced-topics.md)
</dt> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> <dt>

[**Iwmreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMReaderAdvanced2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**Iwmsynkreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> </dl>

 

 




