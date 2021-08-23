---
description: Speichert intern das vom Treiber zurückgegebene ungefilterte Image zwischen.
ms.assetid: 09cb242d-d1d6-4130-8b49-0770940471d8
title: IWiaPreview::GetNewPreview-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.GetNewPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2200452fe586a4755a4560f0f68094e5f107e9e7d69a823bafac4d33bc1c6ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965559"
---
# <a name="iwiapreviewgetnewpreview-method"></a>IWiaPreview::GetNewPreview-Methode

Speichert intern das vom Treiber zurückgegebene ungefilterte Image zwischen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNewPreview(
  [in] IWiaItem2            *pWiaItem2,
  [in] LONG                 lFlags,
  [in] IWiaTransferCallback *pWiaTransferCallback
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pWiaItem2* \[ In\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Gibt einen Zeiger auf das [**IWiaItem2-Element**](-wia-iwiaitem2.md) für das Bild an.

</dd> <dt>

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*pWiaTransferCallback* \[ In\]
</dt> <dd>

Typ: **[ **IWiaTransferCallback**](-wia-iwiatransfercallback.md)\***

Gibt einen Zeiger auf die [**IWiaTransferCallback-Schnittstelle**](-wia-iwiatransfercallback.md) der aufrufenden Anwendung an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Eine Anwendung muss **IWiaPreview::GetNewPreview** aufrufen, bevor sie [**IWiaPreview::D etectRegions aufruft.**](-wia-iwiapreview-detectregions.md)

**IWiaPreview::GetNewPreview** legt die [**WIA \_ DPS \_ PREVIEW-Eigenschaft**](-wia-wiaitempropscannerdevice.md) fest (und setzt sie zurück, bevor sie zurückgegeben wird, es sei denn, sie wurde zuvor festgelegt). Dadurch können Treiber und Hardware sowie der Bildverarbeitungsfilter wissen, dass es sich bei dem Element um eine Vorschauüberprüfung handelt.

Intern erstellt die komponente Windows Image Acquisition (WIA) 2.0 preview eine Instanz des Bildverarbeitungsfilters des Treibers, indem [**GetExtension**](-wia-iwiaitem2-getextension.md) auf *pWiaItem2* aufgerufen wird. Die WIA 2.0-Vorschaukomponente führt dies aus, wenn die Anwendung **IWiaPreview::GetNewPreview aufruft.** Die WIA 2.0-Vorschaukomponente initialisiert auch den Filter in **IWiaPreview::GetNewPreview.** Dieselbe Filterinstanz wird von der WIA 2.0-Vorschaukomponente während eines Aufrufs von [**IWiaPreview::UpdatePreview**](-wia-iwiapreview-updatepreview.md)verwendet.

Vor dem Aufrufen der WIA 2.0-Vorschaukomponente sollte eine Anwendung [**CheckExtension**](-wia-iwiaitem2-checkextension.md) aufrufen, um sicherzustellen, dass der Treiber einen Bildverarbeitungsfilter enthält. Sie sollte **CheckExtension** für das Element aufrufen, das an **IWiaPreview::GetNewPreview** übergeben wird. Es ist unbrauchbar, Livevorschauversionen ohne Bildverarbeitungsfilter bereitzustellen. Wenn eine Anwendung **IWiaPreview::GetNewPreview** für einen Treiber ohne Bildverarbeitungsfilter aufruft, schlägt der Aufruf fehl.

## <a name="examples"></a>Beispiele

CheckImgFilter überprüft, ob der Treiber über einen Bildverarbeitungsfilter verfügt. Vor dem Aufrufen der Vorschaukomponente sollte eine Anwendung sicherstellen, dass der Treiber über einen Bildverarbeitungsfilter verfügt.


```C++
HRESULT
CheckImgFilter(
   IN  IWiaItem2 *pWiaItem2,
   OUT BOOL      *pbHasImgFilter)
{
   HRESULT     hr = S_OK;

   if (!pWiaItem2 || !pbHasImgFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
     *pbHasImgFilter = FALSE;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_IMAGEPROC_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->CheckExtension(0,
                                        bstrFilterString,
                                        IID_IWiaSegmentationFilter,
                                        pbHasImgFilter);

         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   return hr;

}
```



DownloadPreviewImage lädt Bilddaten vom Scanner herunter, indem die **IWiaPreview::GetNewPreview-Methode** der Vorschaukomponente aufgerufen wird. Anschließend wird DetectSubregions aufgerufen, wenn der Anwendungsbenutzer den Segmentierungsfilter aufrufen möchte, der ein untergeordnetes Element unter pWiaItem2 für jede erkannte Region erstellt. Informationen zur in diesem Beispiel verwendeten DetectSubregions-Methode finden Sie unter [**DetectRegions.**](-wia-iwiasegmentationfilter-detectregions.md)

In diesem Beispiel legt der Anwendungsbenutzer `m_bUseSegmentationFilter` fest, indem er auf ein Kontrollkästchen klickt. Wenn die Anwendung dies unterstützt, sollte zunächst überprüft werden, ob der Treiber über einen Segmentierungsfilter verfügt, indem [**CheckExtension**](-wia-iwiaitem2-checkextension.md)aufgerufen wird. Unter **IWiaPreview::GetNewPreview** finden Sie das CheckImgFilter-Methodenbeispiel, das zeigt, wie dies möglich ist.


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
         // The constructor of AppWiaTransferCallback sets the reference count to 1.
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
         // Do not create an instance of preview component if the driver does
         // not come with an image processing filter.
         // You can use segmentation filter, however, if the driver
         // comes with one (omitted here).
      }
   }

   return hr;
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




