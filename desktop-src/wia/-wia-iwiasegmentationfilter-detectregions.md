---
description: Bestimmt die Unterregionen eines Bilds, das auf dem Flachbildschirm ausgelegt ist, sodass jeder untere Bereich in ein separates Bildelement übernommen werden kann.
ms.assetid: 899d61f0-2dd8-4a68-827e-89e85ebb5143
title: IWiaSegmentationFilter::D etectRegions-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter.DetectRegions
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 46496360d7b54bed837ba287d604233a9fac98ee13807744b4adbfb52e9934d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450260"
---
# <a name="iwiasegmentationfilterdetectregions-method"></a>IWiaSegmentationFilter::D etectRegions-Methode

Bestimmt die Unterregionen eines Bilds, das auf dem Flachbildschirm ausgelegt ist, sodass jeder untere Bereich in ein separates Bildelement übernommen werden kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT DetectRegions(
  [in] LONG      lFlags,
  [in] IStream   *pInputStream,
  [in] IWiaItem2 *pWiaItem2
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*pInputStream* \[ In\]
</dt> <dd>

Typ: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\***

Gibt einen Zeiger auf das [IStream-Vorschaubild](/windows/win32/api/objidl/nn-objidl-istream) an.

</dd> <dt>

*pWiaItem2* \[ In\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Gibt einen Zeiger auf das [**IWiaItem2-Element**](-wia-iwiaitem2.md) an, für das *pInputStream* erworben wurde. Der Segmentierungsfilter erstellt untergeordnete Elemente für dieses Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode bestimmt die Unterregionen des durch pInputStream dargestellten Bilds. Für jeden erkannten Unterbereich wird ein untergeordnetes Element für das [**im pWiaItem2-Parameter angegebene IWiaItem2-Element**](-wia-iwiaitem2.md) erstellt.  Für jedes untergeordnete Element muss der Segmentierungsfilter Werte für das umgebundene Rechteck des zu überprüfenden Bereichs festlegen, indem die folgenden [**WIA-Elementeigenschaftskonstationen für**](-wia-wiaitempropscanneritem.md)Scanner verwendet werden.

-   [**WIA \_ IPS \_ XPOS**](-wia-wiaitempropscanneritem.md)
-   [**WIA \_ IPS \_ YPOS**](-wia-wiaitempropscanneritem.md)
-   [**WIA \_ IPS \_ XEXTENT**](-wia-wiaitempropscanneritem.md)
-   [**WIA \_ IPS \_ YEXTENT**](-wia-wiaitempropscanneritem.md)

Für einen erweiterten Filter sind möglicherweise auch andere [**WIA-Elementeigenschaftskonstten**](-wia-wiaitempropscanneritem.md) für Scanner erforderlich, z. B. **WIA \_ IPS \_ DESKEW \_ X** und **WIA \_ IPS \_ DESKEW \_ Y,** wenn der Treiber die Deskewing unterstützt.

Wenn die Anwendung **IWiaSegmentationFilter::D etectRegions** mehr als einmal aufruft, muss die Anwendung zuerst die untergeordneten Elemente löschen, die durch den letzten Aufruf von **IWiaSegmentationFilter::D etectRegions** erstellt wurden.

Wenn eine Anwendung Eigenschaften in *pWiaItem2* ändert, müssen die ursprünglichen Eigenschaften (d. h. die Eigenschaften, die das Element beim Abrufen des Streams hatte) wiederhergestellt werden, zwischen dem Abrufen des Images in *pInputStream* und dem Aufruf **von IWiaSegmentationFilter::D etectRegions).** Dies kann mit [**GetPropertyStream und**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) [**SetPropertyStream erfolgen.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream)

Die Anwendung muss den [IStream zurücksetzen,](/windows/win32/api/objidl/nn-objidl-istream) wenn sein Aufruf denselben Stream mehr als einmal an den Segmentierungsfilter übergibt. Die Anwendung muss den Stream auch nach dem ersten Download und vor dem Aufruf von **IWiaSegmentationFilter::D etectRegions zurücksetzen.**

## <a name="examples"></a>Beispiele

Die Segmentierung führt die Erkennung von Regionen für den Stream ( ) aus, `pImageStream` der an DetectSubregions übergeben wird. Siehe die [**in diesem Beispiel verwendete GetExtension**](-wia-iwiaitem2-getextension.md) for CreateSegmentationFilter-Methode.


```C++
HRESULT
DetectSubregions(
   IN IStream   *pImageStream,
   IN IWiaItem2 *pWiaItem2)
{
   HRESULT                 hr                  = S_OK;
   IWiaSegmentationFilter* pSegmentationFilter = NULL;

   if (!pWiaItem2 || !pImageStream)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      hr = CreateSegmentationFilter(pWiaItem2, &pSegmentationFilter);
   }

   if (SUCCEEDED(hr))
   {
      hr = pSegmentationFilter->DetectRegions(0,pImageStream, pWiaItem2); 
   }

   if (pSegmentationFilter)
   {
      pSegmentationFilter->Release();
      pSegmentationFilter = NULL;
   }

   return hr;
}
```



DownloadPreviewImage lädt Bilddaten vom Scanner herunter, indem die [**GetNewPreview-Methode**](-wia-iwiapreview-getnewpreview.md) der Vorschaukomponente aufruft. Anschließend wird DetectSubregions aufgerufen, wenn der Anwendungsbenutzer den Segmentierungsfilter aufrufen möchte. Dadurch wird unter pWiaItem2 für jede erkannte Region ein untergeordnetes Element erstellt. Die in diesem Beispiel verwendete DetectSubregions-Methode finden Sie unter **IWiaSegmentationFilter::D etectRegions.**

In diesem Beispiel legt der Anwendungsbenutzer `m_bUseSegmentationFilter` fest, indem er auf ein Kontrollkästchen klickt. Wenn die Anwendung dies unterstützt, sollte sie zunächst überprüfen, ob der Treiber über einen Segmentierungsfilter verfügt, indem [**CheckExtension aufruft.**](-wia-iwiaitem2-checkextension.md) Unter [**GetNewPreview finden**](-wia-iwiapreview-getnewpreview.md) Sie ein Beispiel für die CheckImgFilter-Methode, das zeigt, wie dies möglich ist.


```C++
HRESULT
DownloadPreviewImage(
   IN IWiaItem2 *pWiaFlatbedItem2)
{
   HRESULT hr              = S_OK;
   BOOL    bHasImgFilter   = FALSE;

   IWiaTransferCallback *pAppWiaTransferCallback = NULL;

   hr = CheckImgFilter(pWiaFlatbedItem2, &bHasImgFilter)

   if (SUCCEEDED(hr))
   {
      if (bHasImgFilter)
      {
         IWiaPreview *pWiaPreview = NULL;

         // In this example, the AppWiaTransferCallback class implements 
         // the IWiaTransferCallback interface.  
         // The constructor of AppWiaTransferCallback sets the reference count 
         // to 1.
         pAppWiaTransferCallback = new AppWiaTransferCallback();

         hr = pAppWiaTransferCallback ? S_OK : E_OUTOFMEMORY;

         if (SUCCEEDED(hr))
         {
            // Acquire image from scanner
            hr = m_pWiaPreview->GetNewPreview(pWiaFlatbedItem2,
                                              0,
                                              pAppWiaTransferCallback);    
         }

         //
         // Check the application UI for whether the user wants
         // to use the segmentation filter indicated by the value 
         // of m_bUseSegmentationFilter.
         //
         // m_FlatbedPreviewStream is the stream that
         // AppWiaTransferCallback::GetNextStream returned for the
         // flatbed item.
         // This stream is where the image data is stored after
         // the successful return of GetNewPreview.
         // The stream is passed into the segmentation filter
         // for region detection.
         if (SUCCEEDED(hr) && m_bUseSegmentationFilter)
         {
            DetectSubregions(m_FlatbedPreviewStream, pWiaFlatbedItem2);
         }

         if (pAppWiaTransferCallback)
         {
            // If the call to GetNewPreview was successful, the
            // preview component calls AddRef on the callback so
            // this call doesn't delete the object.

            pAppWiaTransferCallback->Release();
         }

      }
      else
      {
         // Do not create an instance of preview component if the driver 
         // does not come with an image-processing filter.
         // You can use a segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
