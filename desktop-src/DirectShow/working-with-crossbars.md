---
description: Arbeiten mit quer leisten
ms.assetid: 6e8ee9c3-6776-498b-ad38-36f8172a27ae
title: Arbeiten mit quer leisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3d3a1c43703ac662d44854b0fc6bad8b280c368
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350138"
---
# <a name="working-with-crossbars"></a>Arbeiten mit quer leisten

Wenn eine Video Erfassungs Karte mehr als eine physische Eingabe aufweist oder mehr als einen Hardware Pfad für Daten unterstützt, enthält das Filter Diagramm möglicherweise den Filter für die [analoge Video quer Leiste](analog-video-crossbar-filter.md). Der Erfassungs Diagramm-Generator fügt diesen Filter bei Bedarf automatisch hinzu. Sie wird über den Erfassungs Filter als Upstream verwendet. Abhängig von der Hardware kann das Filter Diagramm mehr als eine Instanz des Querbalken Filters enthalten.

Der Querbalken Filter macht die [**iamcrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) -Schnittstelle verfügbar, mit der Sie eine bestimmte Eingabe an eine bestimmte Ausgabe weiterleiten können. Beispielsweise kann eine Grafikkarte einen koaxialen Connector und eine S-Video-Eingabe enthalten. Diese werden als Eingabe Pins auf dem Querbalken Filter dargestellt. Um eine Eingabe auszuwählen, leiten Sie die entsprechende Eingabe-PIN mithilfe der [**iamcrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) -Methode an die Ausgabepin der quer Leiste weiter.

Wenn Sie Querbalken Filter im Diagramm suchen möchten, können Sie die [**ICaptureGraphBuilder2:: findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) -Methode verwenden, um nach Filtern zu suchen, die **iamcrossbar** unterstützen. Der folgende Code sucht beispielsweise nach zwei Querbalken:


```C++
// Search upstream for a crossbar.
IAMCrossbar *pXBar1 = NULL;
hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
if (SUCCEEDED(hr)) 
{
    // Found one crossbar. Get its IBaseFilter interface.
    IBaseFilter *pFilter = NULL;
    hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pFilter);
    if (SUCCEEDED(hr)) 
    {
        // Search upstream for another crossbar.
        IAMCrossbar *pXBar2 = NULL;
        hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pFilter,
                 IID_IAMCrossbar, (void**)&pXBar2);
        pFilter->Release();

        if (SUCCEEDED(hr))
        {
            /* ... */
            pXBar2->Release();
        }
    }
    pXBar1->Release();
}
```



Eine allgemeinere Vorgehensweise finden Sie in der ccrossbar-Klasse im [amcap-Beispiel](amcap-sample.md).

Sobald Sie über einen Zeiger auf die **iamcrossbar** -Schnittstelle verfügen, können Sie Informationen über den Querbalken Filter, einschließlich des physischen Typs der einzelnen PIN, und der Matrix, in der die Eingabe Pins geroutet werden können, an die Ausgabe Pins weiterleiten.

-   Um den Typ des physischen Verbindungs Typs zu bestimmen, dem eine PIN entspricht, nennen Sie die [**iamcrossbar:: get \_ crossbarpininfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) -Methode. Die-Methode gibt einen Member der [**physicalconnectortype**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) -Enumeration zurück. Eine S-Video-PIN gibt z. b. den Wert "physconn \_ Video \_ SVideo" zurück.

    Die **get \_ crossbarinfo** -Methode gibt auch an, ob zwei Pins miteinander verknüpft sind. Beispielsweise kann eine Video-Tuner-PIN mit einer audiotuner-Pin verknüpft werden. Verwandte Pins haben die gleiche Pin-Richtung und sind in der Regel Teil desselben physischen Jack oder Connector auf der Karte.

-   Um zu ermitteln, ob Sie eine Eingabe-PIN an eine bestimmte Ausgabe-PIN weiterleiten können, müssen Sie die [**iamcrossbar:: canroute**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute) -Methode abrufen.
-   Um das aktuelle Routing zwischen Pins zu ermitteln, müssen Sie die [**iamcrossbar:: get \_ isroutedto**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto) -Methode abrufen.

Die vorherigen Methoden geben alle Pins nach Indexnummer an, wobei Ausgabe Pins und Eingabe Pins beide von 0 (null) indiziert werden. Aufrufen der **iamcrossbar:: get \_ pincounts** -Methode, um die Anzahl der Pins im Filter zu ermitteln.

Im folgenden Code werden z. b. Informationen zu einem Querbalken Filter im Konsolenfenster angezeigt:


```C++
// Helper function to associate a name with the type.
const char * GetPhysicalPinName(long lType)
{
    switch (lType) 
    {
    case PhysConn_Video_Tuner:            return "Video Tuner";
    case PhysConn_Video_Composite:        return "Video Composite";
    case PhysConn_Video_SVideo:           return "S-Video";
    case PhysConn_Video_RGB:              return "Video RGB";
    case PhysConn_Video_YRYBY:            return "Video YRYBY";
    case PhysConn_Video_SerialDigital:    return "Video Serial Digital";
    case PhysConn_Video_ParallelDigital:  return "Video Parallel Digital"; 
    case PhysConn_Video_SCSI:             return "Video SCSI";
    case PhysConn_Video_AUX:              return "Video AUX";
    case PhysConn_Video_1394:             return "Video 1394";
    case PhysConn_Video_USB:              return "Video USB";
    case PhysConn_Video_VideoDecoder:     return "Video Decoder";
    case PhysConn_Video_VideoEncoder:     return "Video Encoder";
        
    case PhysConn_Audio_Tuner:            return "Audio Tuner";
    case PhysConn_Audio_Line:             return "Audio Line";
    case PhysConn_Audio_Mic:              return "Audio Microphone";
    case PhysConn_Audio_AESDigital:       return "Audio AES/EBU Digital";
    case PhysConn_Audio_SPDIFDigital:     return "Audio S/PDIF";
    case PhysConn_Audio_SCSI:             return "Audio SCSI";
    case PhysConn_Audio_AUX:              return "Audio AUX";
    case PhysConn_Audio_1394:             return "Audio 1394";
    case PhysConn_Audio_USB:              return "Audio USB";
    case PhysConn_Audio_AudioDecoder:     return "Audio Decoder";
        
    default:                              return "Unknown Type";
    }    
}

void DisplayCrossbarInfo(IAMCrossbar *pXBar)
{
    HRESULT hr;
    long cOutput = -1, cInput = -1;
    hr = pXBar->get_PinCounts(&cOutput, &cInput);

    for (long i = 0; i < cOutput; i++)
    {
        long lRelated = -1, lType = -1, lRouted = -1;

        hr = pXBar->get_CrossbarPinInfo(FALSE, i, &lRelated, &lType);
        hr = pXBar->get_IsRouted(i, &lRouted);

        printf("Output pin %d: %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated out: %d, Routed in: %d\n", lRelated, lRouted);
        printf("\tSwitching Matrix: ");

        for (long j = 0; j < cInput; j++)
        {
            hr = pXBar->CanRoute(i, j);
            printf("%d-%s", j, (S_OK == hr ? "Yes" : "No"));
        }
        printf("\n\n");
    }

    for (i = 0; i < cInput; i++)
    {
        long lRelated = -1, lType = -1;

        hr = pXBar->get_CrossbarPinInfo(TRUE, i, &lRelated, &lType);

        printf("Input pin %d - %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated in: %d\n", lRelated);
    }
}
```



Bei einer hypothetischen Karte kann diese Funktion die folgende Ausgabe ergeben:


```C++
Output pin 0: S-Video
    Related out: 2, Routed in: 0
    Switching Matrix: 0-Yes 1-No 2-No 3-No
Output pin 1 - Video Tuner
    Related out: 2, Routed in: 1
    Switching Matrix: 0-No 1-Yes 2-No 3-No
Output pin 2 - Audio decoder
    Related out: 1, Routed in: -1
    Switching Matrix: 0-No 1-No 2-Yes 3-Yes

Input pin 0 - S-Video
    Related in: 2
Input pin 1 - Video Tuner
    Related in: 3
Input pin 2 - Audio line
    Related in: 0
Input pin 3 - Audio tuner
    Related in: 1
```



Auf der Ausgabe Seite sind das S-Video und der Video-Tuner beide mit dem Audiodecoder verknüpft. Auf der Eingabe Seite bezieht sich der Video-Tuner auf den audiotuner, und das S-Video bezieht sich auf die audiozeile in. Die s-Video-Eingabe wird an die s-Video-Ausgabe weitergeleitet. und die Video-Tuner-Eingabe wird an die Video-Tuner-Ausgabe weitergeleitet. Zurzeit wird nichts an den Audiodecoder weitergeleitet, aber entweder die audiozeile in oder der audiotuner kann an Sie weitergeleitet werden.

Sie können das vorhandene Routing ändern, indem Sie die [**iamcrossbar:: Route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) -Methode aufrufen.

 

 



