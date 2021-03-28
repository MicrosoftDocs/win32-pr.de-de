---
description: Ab Windows Vista besteht eine größere Verwendung aus Datei spezifischen Miniaturbildern als in früheren Versionen von Windows.
title: Entwickeln von Miniatur Ansichts Handlern
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 218264a9-ed26-4049-a721-232943f6ec53
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c05e13f24a2f4d70a58bab904150b1e488f74854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977392"
---
# <a name="building-thumbnail-handlers"></a><span data-ttu-id="04f45-103">Entwickeln von Miniatur Ansichts Handlern</span><span class="sxs-lookup"><span data-stu-id="04f45-103">Building Thumbnail Handlers</span></span>

<span data-ttu-id="04f45-104">Ab Windows Vista besteht eine größere Verwendung aus Datei spezifischen Miniaturbildern als in früheren Versionen von Windows.</span><span class="sxs-lookup"><span data-stu-id="04f45-104">As of Windows Vista, greater use is made of file-specific thumbnail images than in earlier versions of Windows.</span></span> <span data-ttu-id="04f45-105">Sie werden in allen Ansichten, in Dialogfeldern und für jeden Dateityp verwendet, der Sie bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="04f45-105">They are used in all views, in dialogs, and for any file type that provides them.</span></span> <span data-ttu-id="04f45-106">Die Miniaturansicht wurde ebenfalls geändert.</span><span class="sxs-lookup"><span data-stu-id="04f45-106">Thumbnail display was also changed.</span></span> <span data-ttu-id="04f45-107">Es ist ein kontinuierliches Spektrum Benutzer auswählbarer Größen verfügbar, nicht die diskreten Größen wie Symbole und Miniaturansichten.</span><span class="sxs-lookup"><span data-stu-id="04f45-107">A continuous spectrum of user-selectable sizes is available rather than the discrete sizes such as Icons and Thumbnails.</span></span>

<span data-ttu-id="04f45-108">Die [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) -Schnittstelle macht die Bereitstellung einer Miniaturansicht einfacher als die ältere [**iextractimage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) oder [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2).</span><span class="sxs-lookup"><span data-stu-id="04f45-108">The [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) interface makes providing a thumbnail more straightforward than the older [**IExtractImage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) or [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2).</span></span> <span data-ttu-id="04f45-109">Beachten Sie jedoch, dass vorhandener Code, der **iextractimage** oder **IExtractImage2** verwendet, weiterhin gültig und unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="04f45-109">Note, however, that existing code that uses **IExtractImage** or **IExtractImage2** is still valid and supported.</span></span>

## <a name="the-recipethumbnailprovider-sample"></a><span data-ttu-id="04f45-110">Das Beispiel "recipeer thumbnailprovider"</span><span class="sxs-lookup"><span data-stu-id="04f45-110">The RecipeThumbnailProvider Sample</span></span>

<span data-ttu-id="04f45-111">Das in diesem Abschnitt enthaltene Beispiel " [recipeer thumbnailprovider](samples-recipethumbnailprovider.md) " ist im Windows Software Development Kit (SDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="04f45-111">The [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) sample dissected in this section is included in the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="04f45-112">Der Standard Installations Speicherort ist C: \\ Programme \\ Microsoft sdert \\ Windows \\ v 6.0 \\ Samples \\ WinUI \\ Shell \\ appshellintegration \\ recipeer thumbnailprovider.</span><span class="sxs-lookup"><span data-stu-id="04f45-112">Its default install location is C:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Samples\\WinUI\\Shell\\AppShellIntegration\\RecipeThumbnailProvider.</span></span> <span data-ttu-id="04f45-113">Der Großteil des Codes ist jedoch auch hier enthalten.</span><span class="sxs-lookup"><span data-stu-id="04f45-113">However, the bulk of the code is included here as well.</span></span>

<span data-ttu-id="04f45-114">Das Beispiel " [recipeer thumbnailprovider](samples-recipethumbnailprovider.md) " veranschaulicht die Implementierung eines Miniatur Ansichts Handlers für einen neuen Dateityp, der mit der. Rezept-Erweiterung registriert wird.</span><span class="sxs-lookup"><span data-stu-id="04f45-114">The [RecipeThumbnailProvider](samples-recipethumbnailprovider.md) sample demonstrates the implementation of a thumbnail handler for a new file type registered with a .recipe extension.</span></span> <span data-ttu-id="04f45-115">Das Beispiel veranschaulicht die Verwendung der verschiedenen Miniatur Ansichts Handler-APIs zum Registrieren von Miniatur Ansichts-Component Object Model (com)-Servern für benutzerdefinierte Dateitypen.</span><span class="sxs-lookup"><span data-stu-id="04f45-115">The sample illustrates the use of the different thumbnail handler APIs to register thumbnail extraction Component Object Model (COM) servers for custom file types.</span></span> <span data-ttu-id="04f45-116">Dieses Thema führt Sie durch den Beispielcode, der die Codierungsoptionen und-Richtlinien hervorhebt.</span><span class="sxs-lookup"><span data-stu-id="04f45-116">This topic walks you through the sample code, highlighting coding choices and guidelines.</span></span>

<span data-ttu-id="04f45-117">Ein Miniatur Ansichts Handler muss [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) immer zusammen mit einer der folgenden Schnittstellen implementieren:</span><span class="sxs-lookup"><span data-stu-id="04f45-117">A thumbnail handler must always implement [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) in concert with one of these interfaces:</span></span>

-   [<span data-ttu-id="04f45-118">**IInitializeWithStream**</span><span class="sxs-lookup"><span data-stu-id="04f45-118">**IInitializeWithStream**</span></span>](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [<span data-ttu-id="04f45-119">**IInitializeWithItem**</span><span class="sxs-lookup"><span data-stu-id="04f45-119">**IInitializeWithItem**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [<span data-ttu-id="04f45-120">**IInitializeWithFile**</span><span class="sxs-lookup"><span data-stu-id="04f45-120">**IInitializeWithFile**</span></span>](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)

<span data-ttu-id="04f45-121">Es gibt Fälle, in denen die Initialisierung mit Streams nicht möglich ist.</span><span class="sxs-lookup"><span data-stu-id="04f45-121">There are cases where initialization with streams is not possible.</span></span> <span data-ttu-id="04f45-122">In Szenarios, in denen der Miniatur Ansichts Handler [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)nicht implementiert, muss er die Ausführung im isolierten Prozess ablehnen, bei dem der systemindexer ihn standardmäßig bei einer Änderung am Datenstrom platziert.</span><span class="sxs-lookup"><span data-stu-id="04f45-122">In scenarios where your thumbnail handler does not implement [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream), it must opt out of running in the isolated process where the system indexer places it by default when there is a change to the stream.</span></span> <span data-ttu-id="04f45-123">Legen Sie den folgenden Registrierungs Wert fest, um die Prozess Isolations Funktion abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="04f45-123">To opt out of the process isolation feature, set the following registry value.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {The CLSID of your thumbnail handler}
         DisableProcessIsolation = 1
```

<span data-ttu-id="04f45-124">Wenn Sie [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) implementieren und eine streambasierte Initialisierung durchführen, ist der Handler sicherer und zuverlässiger.</span><span class="sxs-lookup"><span data-stu-id="04f45-124">If you implement [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) and do a stream-based initialization, your handler is more secure and reliable.</span></span> <span data-ttu-id="04f45-125">In der Regel ist die Deaktivierung der Prozess Isolation nur für Legacy Handler vorgesehen. Deaktivieren Sie dieses Feature nicht für neuen Code.</span><span class="sxs-lookup"><span data-stu-id="04f45-125">Typically, disabling process isolation is only intended for legacy handlers; avoid disabling this feature for any new code.</span></span> <span data-ttu-id="04f45-126">**IInitializeWithStream** sollte nach Möglichkeit die erste Wahl der Initialisierungs Schnittstelle sein.</span><span class="sxs-lookup"><span data-stu-id="04f45-126">**IInitializeWithStream** should be your first choice of initialization interface whenever possible.</span></span>

<span data-ttu-id="04f45-127">Da die Bilddatei im Beispiel nicht in die Rezeptdatei eingebettet ist und kein Bestandteil des Datei Datenstroms ist, wird [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) im Beispiel verwendet.</span><span class="sxs-lookup"><span data-stu-id="04f45-127">Because the image file in the sample is not embedded in the .recipe file and is not a part of its file stream, [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) is used in the sample.</span></span> <span data-ttu-id="04f45-128">Die Implementierung der [**IInitializeWithItem:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) -Methode übergibt ihre Parameter einfach an private Klassen Variablen.</span><span class="sxs-lookup"><span data-stu-id="04f45-128">The implementation of the [**IInitializeWithItem::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) method simply passes its parameters to private class variables.</span></span>

<span data-ttu-id="04f45-129">[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) verfügt nur über eine Methode –[**getminiatur**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)–, die mit der größten gewünschten Größe des Bilds in Pixel aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="04f45-129">[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) has only one method—[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)—that is called with the largest desired size of the image, in pixels.</span></span> <span data-ttu-id="04f45-130">Obwohl der Parameter den Namen *CX* hat, wird sein Wert als maximale Größe sowohl der x-als auch der y-Dimension des Bilds verwendet.</span><span class="sxs-lookup"><span data-stu-id="04f45-130">Although the parameter is named *cx*, its value is used as the maximum size of both the x and y dimensions of the image.</span></span> <span data-ttu-id="04f45-131">Wenn die abgerufene Miniaturansicht nicht quadratisch ist, wird die längere Achse durch *CX* beschränkt, und das Seitenverhältnis des ursprünglichen Bilds wird beibehalten.</span><span class="sxs-lookup"><span data-stu-id="04f45-131">If the retrieved thumbnail is not square, then the longer axis is limited by *cx* and the aspect ratio of the original image is preserved.</span></span>

<span data-ttu-id="04f45-132">Wenn der Wert zurückgegeben wird, stellt [**getminiatur**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) ein Handle für das abgerufene Image bereit.</span><span class="sxs-lookup"><span data-stu-id="04f45-132">When it returns, [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) provides a handle to the retrieved image.</span></span> <span data-ttu-id="04f45-133">Außerdem wird ein Wert bereitstellt, der das Farb Format des Bilds angibt und angibt, ob es über gültige Alpha Informationen verfügt.</span><span class="sxs-lookup"><span data-stu-id="04f45-133">It also provides a value that indicates the color format of the image and whether it has valid alpha information.</span></span>

<span data-ttu-id="04f45-134">Die getminiatur-Implementierung im Beispiel beginnt mit einem Aufrufen der privaten **\_ GetBase64EncodedImageString** -Methode.</span><span class="sxs-lookup"><span data-stu-id="04f45-134">The GetThumbnail implementation in the sample begins with a call to the private **\_GetBase64EncodedImageString** method.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
```



<span data-ttu-id="04f45-135">Der ". Rezept"-Dateityp ist einfach eine XML-Datei, die als eindeutige Dateinamenerweiterung registriert ist.</span><span class="sxs-lookup"><span data-stu-id="04f45-135">The .recipe file type is simply an XML file registered as a unique file name extension.</span></span> <span data-ttu-id="04f45-136">Sie enthält ein Element mit dem Namen " **Bild** ", das den relativen Pfad und den Dateinamen des Bilds bereitstellt, das als Miniaturansicht für diese bestimmte. Rezeptdatei verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="04f45-136">It includes an element called **Picture** that provides the relative path and file name of the image to use as the thumbnail for this particular .recipe file.</span></span> <span data-ttu-id="04f45-137">Das **Bild** Element besteht aus dem **Quell** Attribut, das ein Base 64-codiertes Image und ein optionales **size** -Attribut angibt.</span><span class="sxs-lookup"><span data-stu-id="04f45-137">The **Picture** element consists of the **Source** attribute that specifies a base 64 encoded image, and an optional **Size** attribute.</span></span>

<span data-ttu-id="04f45-138">Die **Größe** hat zwei Werte: "Small" und "Large".</span><span class="sxs-lookup"><span data-stu-id="04f45-138">**Size** has two values, Small and Large.</span></span> <span data-ttu-id="04f45-139">Dies ermöglicht es Ihnen, mehrere **Bild** Knoten mit separaten Bildern bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="04f45-139">This allows you to provide multiple **Picture** nodes with separate images.</span></span> <span data-ttu-id="04f45-140">Das abgerufene Abbild richtet sich danach nach dem Wert für die maximale Größe (*CX*), der im Aufrufen von [**getminiatur**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="04f45-140">The image retrieved then depends on the maximum size value (*cx*) provided in the call to [**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail).</span></span> <span data-ttu-id="04f45-141">Da Windows die Größe des Bilds nicht größer als die maximale Größe hat, können für unterschiedliche Lösungen verschiedene Abbilder bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="04f45-141">Because Windows never sizes the image any larger than its maximum size, different images can be provided for different resolutions.</span></span> <span data-ttu-id="04f45-142">Der Einfachheit halber wird im Beispiel das **size** -Attribut ausgelassen und nur ein Bild für alle Situationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="04f45-142">However, for simplicity, the sample omits the **Size** attribute and provides only one image for all situations.</span></span>

<span data-ttu-id="04f45-143">Die **\_ GetBase64EncodedImageString** -Methode, deren Implementierung hier angezeigt wird, verwendet XML-Dokumentobjektmodell (DOM)-APIs, um den **Bild** Knoten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="04f45-143">The **\_GetBase64EncodedImageString** method, whose implementation is shown here, uses XML Document Object Model (DOM) APIs to retrieve the **Picture** node.</span></span> <span data-ttu-id="04f45-144">Von diesem Knoten extrahiert er das Image aus den **Quell** Attributdaten.</span><span class="sxs-lookup"><span data-stu-id="04f45-144">From that node it extracts the image from the **Source** attribute data.</span></span>


```C++
HRESULT CRecipeThumbProvider::_GetBase64EncodedImageString(UINT /* cx */, 
                                                           PWSTR *ppszResult)
{
    *ppszResult = NULL;

    IXMLDOMDocument *pXMLDoc;
    HRESULT hr = _LoadXMLDocument(&pXMLDoc);
    if (SUCCEEDED(hr))
    {
        BSTR bstrQuery = SysAllocString(L"Recipe/Attachments/Picture");
        hr = bstrQuery ? S_OK : E_OUTOFMEMORY;
        if (SUCCEEDED(hr))
        {
            IXMLDOMNode *pXMLNode;
            hr = pXMLDoc->selectSingleNode(bstrQuery, &pXMLNode);
            if (SUCCEEDED(hr))
            {
                IXMLDOMElement *pXMLElement;
                hr = pXMLNode->QueryInterface(&pXMLElement);
                if (SUCCEEDED(hr))
                {
                    BSTR bstrAttribute = SysAllocString(L"Source");
                    hr = bstrAttribute ? S_OK : E_OUTOFMEMORY;
                    if (SUCCEEDED(hr))
                    {
                        VARIANT varValue;
                        hr = pXMLElement->getAttribute(bstrAttribute, &varValue);
                        if (SUCCEEDED(hr))
                        {
                            if ((varValue.vt == VT_BSTR) && varValue.bstrVal && varValue.bstrVal[0])
                            {
                                hr = SHStrDupW(varValue.bstrVal, ppszResult);
                            }
                            else
                            {
                                hr = E_FAIL;
                            }
                            VariantClear(&varValue);
                        }
                        SysFreeString(bstrAttribute);
                    }
                    pXMLElement->Release();
                }
                pXMLNode->Release();
            }
            SysFreeString(bstrQuery);
        }
        pXMLDoc->Release();
    }
    return hr;
}
```



<span data-ttu-id="04f45-145">" [**Getminiatur**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) " übergibt dann die abgerufene Zeichenfolge an " **\_ getstreamfromstring**".</span><span class="sxs-lookup"><span data-stu-id="04f45-145">[**GetThumbnail**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) then passes the retrieved string to **\_GetStreamFromString**.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
    if (SUCCEEDED(hr))
    {
        IStream *pImageStream;
        hr = _GetStreamFromString(pszBase64EncodedImageString, &pImageStream);
```



<span data-ttu-id="04f45-146">Die **\_ getstreamfromstring** -Methode, deren Implementierung hier angezeigt wird, die das codierte Bild in einen Stream konvertiert.</span><span class="sxs-lookup"><span data-stu-id="04f45-146">The **\_GetStreamFromString** method, whose implementation is shown here, which converts the encoded image to a stream.</span></span>


```C++
HRESULT CRecipeThumbProvider::_GetStreamFromString(PCWSTR pszImageName, 
                                                   IStream **ppImageStream)
{
    HRESULT hr = E_FAIL;

    DWORD dwDecodedImageSize = 0;
    DWORD dwSkipChars        = 0;
    DWORD dwActualFormat     = 0;

    // Base64-decode the string
    BOOL fSuccess = CryptStringToBinaryW(pszImageName, 
                                         NULL, 
                                         CRYPT_STRING_BASE64,
                                         NULL, 
                                         &dwDecodedImageSize, 
                                         &dwSkipChars, 
                                         &dwActualFormat);
    if (fSuccess)
    {
        BYTE *pbDecodedImage = (BYTE*)LocalAlloc(LPTR, dwDecodedImageSize);
        if (pbDecodedImage)
        {
            fSuccess = CryptStringToBinaryW(pszImageName, 
                                            lstrlenW(pszImageName), 
                                            CRYPT_STRING_BASE64,
                                            pbDecodedImage, 
                                            &dwDecodedImageSize, 
                                            &dwSkipChars, 
                                            &dwActualFormat);
            if (fSuccess)
            {
                *ppImageStream = SHCreateMemStream(pbDecodedImage, 
                                                   dwDecodedImageSize);
                if (*ppImageStream != NULL)
                {
                    hr = S_OK;
                }
            }
            LocalFree(pbDecodedImage);
        }
    }
    return hr;
}
```



<span data-ttu-id="04f45-147">**GetThumbnail** verwendet dann WIC-APIs (Windows Imaging Component), um eine Bitmap aus dem Stream zu extrahieren und ein Handle für diese Bitmap zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="04f45-147">**GetThumbnail** then uses Windows Imaging Component (WIC) APIs to extract a bitmap from the stream and get a handle to that bitmap.</span></span> <span data-ttu-id="04f45-148">Die Alpha Informationen sind festgelegt, WIC wurde ordnungsgemäß beendet, und die Methode wird erfolgreich beendet.</span><span class="sxs-lookup"><span data-stu-id="04f45-148">The alpha information is set, WIC is properly exited, and the method terminates successfully.</span></span>


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
    if (SUCCEEDED(hr))
    {
        IStream *pImageStream;
        hr = _GetStreamFromString(pszBase64EncodedImageString, &pImageStream);
        if (SUCCEEDED(hr))
        {
            hr = WICCreate32BitsPerPixelHBITMAP(pImageStream, 
                                                cx, 
                                                phbmp, 
                                                pdwAlpha);;

            pImageStream->Release();
        }
        CoTaskMemFree(pszBase64EncodedImageString);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="04f45-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="04f45-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04f45-150">Miniatur Ansichts Handler</span><span class="sxs-lookup"><span data-stu-id="04f45-150">Thumbnail Handlers</span></span>](thumbnail-providers.md)
</dt> <dt>

[<span data-ttu-id="04f45-151">Richtlinien für Miniaturansichten</span><span class="sxs-lookup"><span data-stu-id="04f45-151">Thumbnail Handler Guidelines</span></span>](thumbnail-provider-guidelines.md)
</dt> <dt>

[<span data-ttu-id="04f45-152">**IID \_ PPV-Argumente \_**</span><span class="sxs-lookup"><span data-stu-id="04f45-152">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
