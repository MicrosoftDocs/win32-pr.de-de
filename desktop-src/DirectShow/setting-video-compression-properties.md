---
description: Festlegen von Video Komprimierungs Eigenschaften
ms.assetid: 2be03a2c-39a5-46da-9bbc-af42c08150ab
title: Festlegen von Video Komprimierungs Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d29ed7e42745ffd51fca14b7da5f72c749281e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392673"
---
# <a name="setting-video-compression-properties"></a>Festlegen von Video Komprimierungs Eigenschaften

Video Komprimierungs Filter können die [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) -Schnittstelle auf Ihren Ausgabe Pins unterstützen. Verwenden Sie diese Schnittstelle, um Komprimierungs Eigenschaften festzulegen, z. b. die Keyframerate, die Anzahl der vorhergesagten (P) Frames pro Keyframe und die relative Komprimierungs Qualität.

Zum Ermitteln der Ausgabe-PIN des Filters und zum Abfragen der PIN für die Schnittstelle müssen Sie zuerst die Methode [**ibasefilter:: umumpins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) abrufen. Einige Filter unterstützen die-Schnittstelle möglicherweise überhaupt nicht. Andere können die-Schnittstelle verfügbar machen, jedoch nicht jede Komprimierungs Eigenschaft. Um zu ermitteln, welche Eigenschaften unterstützt werden, nennen Sie [**IAMVideoCompression:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo). Diese Methode gibt mehrere Informationselemente zurück:

-   Eine Reihe von Funktionen-Flags
-   Eine beschreibende Zeichenfolge und Versionsnummern Zeichenfolge
-   Standardwerte für keyframetrate, P-Frame Rate und Qualität (falls unterstützt)

Die-Methode weist die folgende Syntax auf:


```C++
hr = pCompress->GetInfo(pszVersion, &cbVersion, pszDesc, &cbDesc, 
         &lKeyFrame, &lPFrame, &dblQuality, &lCap);
```



Die Parameter *pszversion* und *pszdesc* sind breit Zeichen Puffer, die die Versions Zeichenfolge und die Beschreibungs Zeichenfolge empfangen. Der *cbversion* -und der *cbdesc* -Parameter erhalten die erforderlichen Puffergrößen in Bytes (nicht Zeichen). Die Parameter " *lkeyframe*", " *lpframe*" und " *dblquality* " erhalten die Standardwerte für die Keyframerate, P-Frame Rate und Qualität. Qualität wird als Gleit Komma Zahl zwischen 0,0 und 1,0 ausgedrückt. Der *lcap* -Parameter empfängt eine bitweise **or** -Funktion der Funktionen-Flags, die vom enumerierten Typ " [**compressioncaps**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) " definiert werden.

Jeder dieser Parameter kann **null** sein. in diesem Fall ignoriert die Methode diesen Parameter. Wenn Sie z. b. Puffer für die Versions-und Beschreibungs Zeichenfolgen zuweisen möchten, müssen Sie zuerst die-Methode mit **null** im ersten und dritten Parameter aufzurufen Verwenden Sie die zurückgegebenen Werte für *cbversion* und *cbdesc* , um die Puffer zuzuordnen, und dann die Methode erneut aufzurufen:


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



Der Wert von *lcap* gibt an, welche der anderen **IAMVideoCompression** -Methoden der Filter unterstützt. Wenn *lcap* z. b. das \_ kankeyframe-Flag compressioncaps enthält, können Sie [**IAMVideoCompression:: get \_ Keyframerate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) zum Abrufen der [**Keyframerate und IAMVideoCompression::p UT \_ Keyframerate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) zum Festlegen der Keyframerate abrufen. Ein negativer Wert gibt an, dass der Filter den Standardwert verwendet, wie er von [**IAMVideoCompression:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo)abgerufen wird. Beispiel:


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



Im folgenden Codebeispiel wird versucht, die **IAMVideoCompression** -Schnittstelle in der Ausgabe-PIN zu finden. Wenn der Vorgang erfolgreich ist, werden die Standardwerte und die tatsächlichen Werte für die Komprimierungs Eigenschaften abgerufen:


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
> Wenn Sie die [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle zum Erstellen des Diagramms verwenden, können Sie die **IAMVideoCompression** -Schnittstelle abrufen, indem Sie [**ICaptureGraphBuilder2:: findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)aufrufen, anstatt **ibasefilter:: umumpins** zu verwenden. Die **findinterface** -Methode ist eine Hilfsmethode, die Filter und Pins im Diagramm für eine angegebene Schnittstelle durchsucht.

 

 

 



