---
title: So decodieren Sie Audio in S/PDIF
description: So decodieren Sie Audio in S/PDIF
ms.assetid: b56c2d0a-a7c6-44f8-832a-bbbe7ae053e6
keywords:
- Windows Medienformat-SDK, Decodieren von Audiodaten in S/PDIF
- Windows Medienformat-SDK, Digitales Verbindungsformat (S/PDIF)
- Advanced Systems Format (ASF), Decodieren von Audiodaten in S/PDIF
- ASF (Advanced Systems Format), Decodieren von Audiodaten in S/PDIF
- Advanced Systems Format (ASF),Format für digitale Verbindungen (S/PDIF)
- ASF (Advanced Systems Format),Format für digitale Verbindungen (S/PDIF)
- Format für digitale Verbindungen (S/PDIF), Decodieren von Audiodaten
- S/PDIF (Format für digitale Verbindungen/Digitale Verbindung/S/PDIF), Decodieren von Audiodaten
- Decodieren von Audiodaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84bd4fdbafd5685882f34b698c0745b998b6cee2e63514041db17fed2195346c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845588"
---
# <a name="to-decode-audio-to-spdif"></a>So decodieren Sie Audio in S/PDIF

Audio, das mit dem Windows Media Audio 9-Professional codec codiert ist, kann in das Format der digitalen Verbindung (S/PDIF) decodiert werden. Führen Sie zum Generieren der S/PDIF-Ausgabe die folgenden Schritte aus:

1.  Öffnen Sie eine Datei, die einen Windows Media Audio 9 Professional enthält, indem Sie die [**IWMReader::Open-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) aufrufen.
2.  Identifizieren Sie die Ausgabenummer des Streams, den Sie wünschen. Weitere Informationen finden Sie unter [So identifizieren Sie Ausgabenummern.](to-identify-output-numbers.md)
3.  Rufen Sie [**die IWMReaderAdvanced2::SetOutputSetting-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) auf, um die S/PDIF-Ausgabe zu konfigurieren. Verwenden Sie \_ g wszEnableWMAProSPDIFOutput als Einstellungsnamen. Der Datentyp ist **WMT \_ TYPE \_ BOOL.** Legen Sie den Wert auf **TRUE** fest, um die S/PDIF-Ausgabe zu aktivieren.
4.  Rufen Sie die Ausgabeeigenschaftenschnittstelle [**(IWMOutputMediaProps)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)des gewünschten Ausgabeformats ab, indem Sie die [**IWMReader::GetOutputFormat-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) aufrufen. Weitere Informationen zum Aufzählen von Ausgabeformaten finden Sie unter [Zuweisen von Ausgabeformaten.](assigning-output-formats.md)
5.  Legen Sie das Ausgabeformat fest, indem Sie die [**IWMReader::SetOutputProps-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) aufrufen. Übergeben Sie einen Zeiger auf die **IWMOutputMediaProps-Schnittstelle,** die Sie in Schritt 4 erhalten haben.
6.  Nehmen Sie weitere Konfigurationsänderungen vor, und beginnen Sie mit der Wiedergabe.

> [!Note]  
> Sie können die vorherigen Schritte für den synchronen Reader ausführen, indem Sie die entsprechenden Methoden der [**IWMSyncReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) verwenden.

 

Der folgende Beispielcode veranschaulicht, wie Sie einen Audiostream so festlegen, dass Audio als S/PDIF-Daten ausgegeben wird. Bei dieser Funktion wird davon ausgegangen, dass bereits eine Datei in den Reader geladen wurde und dass die Ausgabenummer identifiziert wurde. Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).


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

[**Weiterführende Themen**](advanced-topics.md)
</dt> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> <dt>

[**IWMReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMReaderAdvanced2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**IWMSyncReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> </dl>

 

 




