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
# <a name="setting-video-compression-properties"></a><span data-ttu-id="a0481-103">Festlegen von Video Komprimierungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a0481-103">Setting Video Compression Properties</span></span>

<span data-ttu-id="a0481-104">Video Komprimierungs Filter können die [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) -Schnittstelle auf Ihren Ausgabe Pins unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a0481-104">Video compression filters can support the [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) interface on their output pins.</span></span> <span data-ttu-id="a0481-105">Verwenden Sie diese Schnittstelle, um Komprimierungs Eigenschaften festzulegen, z. b. die Keyframerate, die Anzahl der vorhergesagten (P) Frames pro Keyframe und die relative Komprimierungs Qualität.</span><span class="sxs-lookup"><span data-stu-id="a0481-105">Use this interface to set compression properties, such as the key frame rate, the number of predicted (P) frames per key frame, and the relative compression quality.</span></span>

<span data-ttu-id="a0481-106">Zum Ermitteln der Ausgabe-PIN des Filters und zum Abfragen der PIN für die Schnittstelle müssen Sie zuerst die Methode [**ibasefilter:: umumpins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) abrufen.</span><span class="sxs-lookup"><span data-stu-id="a0481-106">First, call the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method to find the filter's output pin, and query the pin for the interface.</span></span> <span data-ttu-id="a0481-107">Einige Filter unterstützen die-Schnittstelle möglicherweise überhaupt nicht.</span><span class="sxs-lookup"><span data-stu-id="a0481-107">Some filters may not support the interface at all.</span></span> <span data-ttu-id="a0481-108">Andere können die-Schnittstelle verfügbar machen, jedoch nicht jede Komprimierungs Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a0481-108">Others may expose the interface but not support every compression property.</span></span> <span data-ttu-id="a0481-109">Um zu ermitteln, welche Eigenschaften unterstützt werden, nennen Sie [**IAMVideoCompression:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span><span class="sxs-lookup"><span data-stu-id="a0481-109">To determine which properties are supported, call [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span></span> <span data-ttu-id="a0481-110">Diese Methode gibt mehrere Informationselemente zurück:</span><span class="sxs-lookup"><span data-stu-id="a0481-110">This method returns several pieces of information:</span></span>

-   <span data-ttu-id="a0481-111">Eine Reihe von Funktionen-Flags</span><span class="sxs-lookup"><span data-stu-id="a0481-111">A set of capabilities flags</span></span>
-   <span data-ttu-id="a0481-112">Eine beschreibende Zeichenfolge und Versionsnummern Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a0481-112">A descriptive string and version-number string</span></span>
-   <span data-ttu-id="a0481-113">Standardwerte für keyframetrate, P-Frame Rate und Qualität (falls unterstützt)</span><span class="sxs-lookup"><span data-stu-id="a0481-113">Default values for key frame rate, P frame rate, and quality (when supported)</span></span>

<span data-ttu-id="a0481-114">Die-Methode weist die folgende Syntax auf:</span><span class="sxs-lookup"><span data-stu-id="a0481-114">The method has the following syntax:</span></span>


```C++
hr = pCompress->GetInfo(pszVersion, &cbVersion, pszDesc, &cbDesc, 
         &lKeyFrame, &lPFrame, &dblQuality, &lCap);
```



<span data-ttu-id="a0481-115">Die Parameter *pszversion* und *pszdesc* sind breit Zeichen Puffer, die die Versions Zeichenfolge und die Beschreibungs Zeichenfolge empfangen.</span><span class="sxs-lookup"><span data-stu-id="a0481-115">The *pszVersion* and *pszDesc* parameters are wide-character buffers that receive the version string and description string.</span></span> <span data-ttu-id="a0481-116">Der *cbversion* -und der *cbdesc* -Parameter erhalten die erforderlichen Puffergrößen in Bytes (nicht Zeichen).</span><span class="sxs-lookup"><span data-stu-id="a0481-116">The *cbVersion* and *cbDesc* parameters receive the required buffer sizes in bytes (not characters).</span></span> <span data-ttu-id="a0481-117">Die Parameter " *lkeyframe*", " *lpframe*" und " *dblquality* " erhalten die Standardwerte für die Keyframerate, P-Frame Rate und Qualität.</span><span class="sxs-lookup"><span data-stu-id="a0481-117">The *lKeyFrame*, *lPFrame*, and *dblQuality* parameters receive the default values for the key frame rate, P frame rate, and quality.</span></span> <span data-ttu-id="a0481-118">Qualität wird als Gleit Komma Zahl zwischen 0,0 und 1,0 ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="a0481-118">Quality is expressed as a floating-point number from 0.0 to 1.0.</span></span> <span data-ttu-id="a0481-119">Der *lcap* -Parameter empfängt eine bitweise **or** -Funktion der Funktionen-Flags, die vom enumerierten Typ " [**compressioncaps**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) " definiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0481-119">The *lCap* parameter receives a bitwise **OR** of the capabilities flags, which are defined by the [**CompressionCaps**](/windows/desktop/api/strmif/ne-strmif-compressioncaps) enumerated type.</span></span>

<span data-ttu-id="a0481-120">Jeder dieser Parameter kann **null** sein. in diesem Fall ignoriert die Methode diesen Parameter.</span><span class="sxs-lookup"><span data-stu-id="a0481-120">Any of these parameters can be **NULL**, in which case the method ignores that parameter.</span></span> <span data-ttu-id="a0481-121">Wenn Sie z. b. Puffer für die Versions-und Beschreibungs Zeichenfolgen zuweisen möchten, müssen Sie zuerst die-Methode mit **null** im ersten und dritten Parameter aufzurufen</span><span class="sxs-lookup"><span data-stu-id="a0481-121">For example, to allocate buffers for the version and description strings, first call the method with **NULL** in the first and third parameters.</span></span> <span data-ttu-id="a0481-122">Verwenden Sie die zurückgegebenen Werte für *cbversion* und *cbdesc* , um die Puffer zuzuordnen, und dann die Methode erneut aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="a0481-122">Use the returned values for *cbVersion* and *cbDesc* to allocate the buffers and then call the method again:</span></span>


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



<span data-ttu-id="a0481-123">Der Wert von *lcap* gibt an, welche der anderen **IAMVideoCompression** -Methoden der Filter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0481-123">The value of *lCap* indicates which of the other **IAMVideoCompression** methods the filter supports.</span></span> <span data-ttu-id="a0481-124">Wenn *lcap* z. b. das \_ kankeyframe-Flag compressioncaps enthält, können Sie [**IAMVideoCompression:: get \_ Keyframerate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) zum Abrufen der [**Keyframerate und IAMVideoCompression::p UT \_ Keyframerate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) zum Festlegen der Keyframerate abrufen.</span><span class="sxs-lookup"><span data-stu-id="a0481-124">For example, if *lCap* contains the CompressionCaps\_CanKeyFrame flag, you can call [**IAMVideoCompression::get\_KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-get_keyframerate) to get the key frame rate and [**IAMVideoCompression::put\_KeyFrameRate**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-put_keyframerate) to set the key frame rate.</span></span> <span data-ttu-id="a0481-125">Ein negativer Wert gibt an, dass der Filter den Standardwert verwendet, wie er von [**IAMVideoCompression:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo)abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a0481-125">A negative value indicates that the filter will use the default value, as obtained from [**IAMVideoCompression::GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamvideocompression-getinfo).</span></span> <span data-ttu-id="a0481-126">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a0481-126">For example:</span></span>


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



<span data-ttu-id="a0481-127">Im folgenden Codebeispiel wird versucht, die **IAMVideoCompression** -Schnittstelle in der Ausgabe-PIN zu finden.</span><span class="sxs-lookup"><span data-stu-id="a0481-127">The following code example tries to find the **IAMVideoCompression** interface on the output pin.</span></span> <span data-ttu-id="a0481-128">Wenn der Vorgang erfolgreich ist, werden die Standardwerte und die tatsächlichen Werte für die Komprimierungs Eigenschaften abgerufen:</span><span class="sxs-lookup"><span data-stu-id="a0481-128">If it succeeds, it retrieves the default and actual values for the compression properties:</span></span>


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
> <span data-ttu-id="a0481-129">Wenn Sie die [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle zum Erstellen des Diagramms verwenden, können Sie die **IAMVideoCompression** -Schnittstelle abrufen, indem Sie [**ICaptureGraphBuilder2:: findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)aufrufen, anstatt **ibasefilter:: umumpins** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0481-129">If you are using the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface to build your graph, you can obtain the **IAMVideoCompression** interface by calling [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface), instead of using **IBaseFilter::EnumPins**.</span></span> <span data-ttu-id="a0481-130">Die **findinterface** -Methode ist eine Hilfsmethode, die Filter und Pins im Diagramm für eine angegebene Schnittstelle durchsucht.</span><span class="sxs-lookup"><span data-stu-id="a0481-130">The **FindInterface** method is a helper method that searches filters and pins in the graph for a specified interface.</span></span>

 

 

 



