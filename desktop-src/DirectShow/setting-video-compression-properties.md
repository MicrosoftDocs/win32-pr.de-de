---
description: Festlegen von Videokomprimierungseigenschaften
ms.assetid: 2be03a2c-39a5-46da-9bbc-af42c08150ab
title: Festlegen von Videokomprimierungseigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3f1d73d27acb99e5a197ec4501411669278a6fd5c7b857875141d8831c7173f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583280"
---
# <a name="setting-video-compression-properties"></a>Festlegen von Videokomprimierungseigenschaften

Videokomprimierungsfilter können die [**IAMVideoCompression-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) auf ihren Ausgabepins unterstützen. Verwenden Sie diese Schnittstelle, um Komprimierungseigenschaften wie die Keyframerate, die Anzahl der vorhergesagten Frames (P) pro Keyframe und die relative Komprimierungsqualität zu festlegen.

Rufen Sie zunächst die [**IBaseFilter::EnumPins-Methode**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) auf, um den Ausgabepin des Filters zu suchen, und fragen Sie den Pin für die Schnittstelle ab. Einige Filter unterstützen die Schnittstelle möglicherweise überhaupt nicht. Andere können die Schnittstelle verfügbar machen, aber nicht jede Komprimierungseigenschaft unterstützen. Um zu bestimmen, welche Eigenschaften unterstützt werden, rufen [**Sie IAMVideoCompression::GetInfo auf.**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo) Diese Methode gibt mehrere Informationen zurück:

-   Eine Reihe von Funktionenflags
-   Eine beschreibende Zeichenfolge und versionsbasierte Zeichenfolge
-   Standardwerte für Keyframerate, P Framerate und Qualität (falls unterstützt)

Die -Methode hat die folgende Syntax:


```C++
hr = pCompress->GetInfo(pszVersion, &cbVersion, pszDesc, &cbDesc, 
         &lKeyFrame, &lPFrame, &dblQuality, &lCap);
```



Die *Parameter pszVersion* und *pszDesc* sind Breitzeichenpuffer, die die Versionszeichenfolge und die Beschreibungszeichenfolge empfangen. Die *Parameter cbVersion* und *cbDesc* empfangen die erforderlichen Puffergrößen in Bytes (nicht Zeichen). Die *Parameter lKeyFrame,* *lPFrame* und *dblQuality* erhalten die Standardwerte für die Keyframerate, die P-Framerate und die Qualität. Die Qualität wird als Gleitkommazahl von 0,0 bis 1,0 ausgedrückt. Der *lCap-Parameter* empfängt ein bitweises **OR** der Funktionenflags, die durch den [**aufzählten CompressionCaps-Typ**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) definiert werden.

Jeder dieser Parameter kann **NULL sein.** In diesem Fall ignoriert die -Methode diesen Parameter. Um beispielsweise Puffer für die Versions- und Beschreibungszeichenfolgen zu reservieren, rufen Sie zuerst die -Methode mit **NULL** im ersten und dritten Parameter auf. Verwenden Sie die zurückgegebenen Werte für *cbVersion* und *cbDesc,* um die Puffer zu reservieren, und rufen Sie dann die -Methode erneut auf:


```C++
int cbVersion, cbDesc; // Size in bytes, not characters!
hr = pCompress->GetInfo(0, &cbVersion, 0, &cbDesc, 0, 0, 0, 0);
if (SUCCEEDED(hr))
{
    WCHAR *pszVersion = new WCHAR[cbVersion/2]; // Wide character = 2 bytes
    WCHAR *pszDesc = new WCHAR[cbDesc/2];
    hr = pCompress->GetInfo(pszVersion, 0, pszDesc, 0, 0, 0, 0, 0);
}
```



Der Wert von *lCap gibt* an, welche der anderen **IAMVideoCompression-Methoden** der Filter unterstützt. Wenn *lCap* beispielsweise das CompressionCaps-CanKeyFrame-Flag enthält, können Sie \_ [**IAMVideoCompression::get \_ KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) aufrufen, um die Keyframerate und [**IAMVideoCompression::p ut \_ KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) zum Festlegen der Keyframerate zu erhalten. Ein negativer Wert gibt an, dass der Filter den Standardwert aus [**IAMVideoCompression::GetInfo verwendet.**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo) Beispiel:


```C++
if (lCap & CompressionCaps_CanKeyFrame)
{
    hr = pCompress->get_KeyFrameRate(&lKeyFrame);
    if (FAILED(hr) || lKeyFrame < 0)
    {
        lKeyFrame = lDefaultKeyFrame; // From GetInfo.
    }
}
```



Im folgenden Codebeispiel wird versucht, die **IAMVideoCompression-Schnittstelle** auf dem Ausgabepin zu finden. Wenn dies erfolgreich ist, werden die Standardwerte und die tatsächlichen Werte für die Komprimierungseigenschaften abgerufen:


```C++
HRESULT hr = E_FAIL;
IEnumPins *pEnum = NULL;
IPin *pPin = NULL;
IAMVideoCompression *pCompress = NULL;

// Find the pin that supports IAMVideoCompression (if any).
pFilter->EnumPins(&pEnum);
while (S_OK == pEnum->Next(1, &pPin, NULL))
{
    hr = pPin->QueryInterface(IID_IAMVideoCompression, (void**)&pCompress);
    pPin->Release();
    if (SUCCEEDED(hr)) // Found the interface.
    {
        break;
    }
}
if (SUCCEEDED(hr)) 
{
    long lCap;                     // Capability flags
    long lKeyFrame, lPFrame;       // Real values
    double m_Quality;
    long lKeyFrameDef, lPFrameDef; // Default values
    double QualityDef;
    
    // Get default values and capabilities.
    hr = pCompress->GetInfo(0, 0, 0, 0, &KeyFrameDef, &lPFrameDef,
             &QualityDef, &lCap);
    if (SUCCEEDED(hr))
    {
        // Get actual values where possible.
        if (lCap & CompressionCaps_CanKeyFrame)
        {
            hr = pCompress->get_KeyFrameRate(&lKeyFrame);
            if (FAILED(hr) || lKeyFrame < 0)
                lKeyFrame = lKeyFrameDef;
        }
        if (lCap & CompressionCaps_CanBFrame)
        {
            hr = pCompress->get_PFramesPerKeyFrame(&lPFrame);
            if (FAILED(hr) || lPFrame < 0)
                lPFrame = lPFrameDef;
        }
        if (lCap & CompressionCaps_CanQuality)
        {
            hr = pCompress->get_Quality(&Quality);
            if (FAILED(hr) || Quality < 0)
                Quality = QualityDef;
        }
    }
}
```



> [!Note]  
> Wenn Sie die [**ICaptureGraphBuilder2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) zum Erstellen Ihres Graphen verwenden, können Sie die **IAMVideoCompression-Schnittstelle** abrufen, indem Sie [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)aufrufen, anstatt **IBaseFilter::EnumPins** zu verwenden. Die **FindInterface-Methode** ist eine Hilfsmethode, die Filter und Stecknadeln im Diagramm nach einer angegebenen Schnittstelle durchsucht.

 

 

 



