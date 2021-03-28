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
# <a name="building-thumbnail-handlers"></a>Entwickeln von Miniatur Ansichts Handlern

Ab Windows Vista besteht eine größere Verwendung aus Datei spezifischen Miniaturbildern als in früheren Versionen von Windows. Sie werden in allen Ansichten, in Dialogfeldern und für jeden Dateityp verwendet, der Sie bereitstellt. Die Miniaturansicht wurde ebenfalls geändert. Es ist ein kontinuierliches Spektrum Benutzer auswählbarer Größen verfügbar, nicht die diskreten Größen wie Symbole und Miniaturansichten.

Die [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) -Schnittstelle macht die Bereitstellung einer Miniaturansicht einfacher als die ältere [**iextractimage**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage) oder [**IExtractImage2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iextractimage2). Beachten Sie jedoch, dass vorhandener Code, der **iextractimage** oder **IExtractImage2** verwendet, weiterhin gültig und unterstützt wird.

## <a name="the-recipethumbnailprovider-sample"></a>Das Beispiel "recipeer thumbnailprovider"

Das in diesem Abschnitt enthaltene Beispiel " [recipeer thumbnailprovider](samples-recipethumbnailprovider.md) " ist im Windows Software Development Kit (SDK) enthalten. Der Standard Installations Speicherort ist C: \\ Programme \\ Microsoft sdert \\ Windows \\ v 6.0 \\ Samples \\ WinUI \\ Shell \\ appshellintegration \\ recipeer thumbnailprovider. Der Großteil des Codes ist jedoch auch hier enthalten.

Das Beispiel " [recipeer thumbnailprovider](samples-recipethumbnailprovider.md) " veranschaulicht die Implementierung eines Miniatur Ansichts Handlers für einen neuen Dateityp, der mit der. Rezept-Erweiterung registriert wird. Das Beispiel veranschaulicht die Verwendung der verschiedenen Miniatur Ansichts Handler-APIs zum Registrieren von Miniatur Ansichts-Component Object Model (com)-Servern für benutzerdefinierte Dateitypen. Dieses Thema führt Sie durch den Beispielcode, der die Codierungsoptionen und-Richtlinien hervorhebt.

Ein Miniatur Ansichts Handler muss [**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) immer zusammen mit einer der folgenden Schnittstellen implementieren:

-   [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem)
-   [**IInitializeWithFile**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithfile)

Es gibt Fälle, in denen die Initialisierung mit Streams nicht möglich ist. In Szenarios, in denen der Miniatur Ansichts Handler [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)nicht implementiert, muss er die Ausführung im isolierten Prozess ablehnen, bei dem der systemindexer ihn standardmäßig bei einer Änderung am Datenstrom platziert. Legen Sie den folgenden Registrierungs Wert fest, um die Prozess Isolations Funktion abzulehnen.

```
HKEY_CLASSES_ROOT
   CLSID
      {The CLSID of your thumbnail handler}
         DisableProcessIsolation = 1
```

Wenn Sie [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream) implementieren und eine streambasierte Initialisierung durchführen, ist der Handler sicherer und zuverlässiger. In der Regel ist die Deaktivierung der Prozess Isolation nur für Legacy Handler vorgesehen. Deaktivieren Sie dieses Feature nicht für neuen Code. **IInitializeWithStream** sollte nach Möglichkeit die erste Wahl der Initialisierungs Schnittstelle sein.

Da die Bilddatei im Beispiel nicht in die Rezeptdatei eingebettet ist und kein Bestandteil des Datei Datenstroms ist, wird [**IInitializeWithItem**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinitializewithitem) im Beispiel verwendet. Die Implementierung der [**IInitializeWithItem:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinitializewithitem-initialize) -Methode übergibt ihre Parameter einfach an private Klassen Variablen.

[**IThumbnailProvider**](/windows/desktop/api/Thumbcache/nn-thumbcache-ithumbnailprovider) verfügt nur über eine Methode –[**getminiatur**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)–, die mit der größten gewünschten Größe des Bilds in Pixel aufgerufen wird. Obwohl der Parameter den Namen *CX* hat, wird sein Wert als maximale Größe sowohl der x-als auch der y-Dimension des Bilds verwendet. Wenn die abgerufene Miniaturansicht nicht quadratisch ist, wird die längere Achse durch *CX* beschränkt, und das Seitenverhältnis des ursprünglichen Bilds wird beibehalten.

Wenn der Wert zurückgegeben wird, stellt [**getminiatur**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) ein Handle für das abgerufene Image bereit. Außerdem wird ein Wert bereitstellt, der das Farb Format des Bilds angibt und angibt, ob es über gültige Alpha Informationen verfügt.

Die getminiatur-Implementierung im Beispiel beginnt mit einem Aufrufen der privaten **\_ GetBase64EncodedImageString** -Methode.


```C++
IFACEMETHODIMP CRecipeThumbProvider::GetThumbnail(UINT cx, 
                                                  HBITMAP *phbmp, 
                                                  WTS_ALPHATYPE *pdwAlpha)
{
    PWSTR pszBase64EncodedImageString;
    HRESULT hr = _GetBase64EncodedImageString(cx, &pszBase64EncodedImageString);
```



Der ". Rezept"-Dateityp ist einfach eine XML-Datei, die als eindeutige Dateinamenerweiterung registriert ist. Sie enthält ein Element mit dem Namen " **Bild** ", das den relativen Pfad und den Dateinamen des Bilds bereitstellt, das als Miniaturansicht für diese bestimmte. Rezeptdatei verwendet werden soll. Das **Bild** Element besteht aus dem **Quell** Attribut, das ein Base 64-codiertes Image und ein optionales **size** -Attribut angibt.

Die **Größe** hat zwei Werte: "Small" und "Large". Dies ermöglicht es Ihnen, mehrere **Bild** Knoten mit separaten Bildern bereitzustellen. Das abgerufene Abbild richtet sich danach nach dem Wert für die maximale Größe (*CX*), der im Aufrufen von [**getminiatur**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail)angegeben ist. Da Windows die Größe des Bilds nicht größer als die maximale Größe hat, können für unterschiedliche Lösungen verschiedene Abbilder bereitgestellt werden. Der Einfachheit halber wird im Beispiel das **size** -Attribut ausgelassen und nur ein Bild für alle Situationen bereitstellt.

Die **\_ GetBase64EncodedImageString** -Methode, deren Implementierung hier angezeigt wird, verwendet XML-Dokumentobjektmodell (DOM)-APIs, um den **Bild** Knoten abzurufen. Von diesem Knoten extrahiert er das Image aus den **Quell** Attributdaten.


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



" [**Getminiatur**](/windows/desktop/api/Thumbcache/nf-thumbcache-ithumbnailprovider-getthumbnail) " übergibt dann die abgerufene Zeichenfolge an " **\_ getstreamfromstring**".


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



Die **\_ getstreamfromstring** -Methode, deren Implementierung hier angezeigt wird, die das codierte Bild in einen Stream konvertiert.


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



**GetThumbnail** verwendet dann WIC-APIs (Windows Imaging Component), um eine Bitmap aus dem Stream zu extrahieren und ein Handle für diese Bitmap zu erhalten. Die Alpha Informationen sind festgelegt, WIC wurde ordnungsgemäß beendet, und die Methode wird erfolgreich beendet.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Miniatur Ansichts Handler](thumbnail-providers.md)
</dt> <dt>

[Richtlinien für Miniaturansichten](thumbnail-provider-guidelines.md)
</dt> <dt>

[**IID \_ PPV-Argumente \_**](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
