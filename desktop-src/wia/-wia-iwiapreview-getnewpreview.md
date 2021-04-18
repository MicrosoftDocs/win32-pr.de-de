---
description: Speichert das vom Treiber zurückgegebene ungefilterte Bild intern zwischen.
ms.assetid: 09cb242d-d1d6-4130-8b49-0770940471d8
title: 'Iwiapreview:: getnewpreview-Methode (WIA. h)'
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
ms.openlocfilehash: c3f1251e7ec1b98d43e616c1ff6f2b3b2aacd8b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354498"
---
# <a name="iwiapreviewgetnewpreview-method"></a>Iwiapreview:: getnewpreview-Methode

Speichert das vom Treiber zurückgegebene ungefilterte Bild intern zwischen.

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

*pWiaItem2* \[ in\]
</dt> <dd>

Typ: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Gibt einen Zeiger auf das [_ *IWiaItem2* *](-wia-iwiaitem2.md) -Element für das Bild an.

</dd> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*pwiatransfercallback* \[ in\]
</dt> <dd>

Typ: **[**iwiatransfercallback**](-wia-iwiatransfercallback.md) \** _

Gibt einen Zeiger auf die [_ *iwiatransfercallback* *](-wia-iwiatransfercallback.md) -Schnittstelle der aufrufenden Anwendung an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung muss **iwiapreview:: getnewpreview** aufrufen, bevor [**iwiapreview::D etectregions**](-wia-iwiapreview-detectregions.md)aufgerufen wird.

**Iwiapreview:: getnewpreview** legt die [**WIA-Eigenschaft \_ DPS \_ Preview**](-wia-wiaitempropscannerdevice.md) fest (und setzt Sie vor der Rückgabe zurück, es sei denn, Sie wurde zuvor festgelegt). Dadurch kann der Treiber und die Hardware sowie der Bild Verarbeitungs Filter wissen, dass es sich bei dem Element um eine Vorschauversion handelt.

Intern erstellt die Windows-Abbild Übernahme (WIA) 2,0 Preview-Komponente eine Instanz des filterverarbeitungs Filters des Treibers, indem [**GetExtension**](-wia-iwiaitem2-getextension.md) auf *pWiaItem2* aufgerufen wird. Die WIA 2,0-Vorschau Komponente führt dies aus, wenn die Anwendung **iwiapreview:: getnewpreview** aufruft. Die WIA 2,0-Vorschau Komponente initialisiert auch den Filter in **iwiapreview:: getnewpreview**. Dieselbe Filter Instanz wird von der WIA 2,0-Vorschau Komponente während eines [**iwiapreview:: updatepreview**](-wia-iwiapreview-updatepreview.md)-Aufrufes verwendet.

Vor dem Aufrufen der WIA 2,0-Vorschau Komponente sollte eine Anwendung [**checkextension**](-wia-iwiaitem2-checkextension.md) aufrufen, um sicherzustellen, dass der Treiber über einen Bild Verarbeitungs Filter verfügt. Er sollte **checkextension** für das Element aufrufen, das an **iwiapreview:: getnewpreview** übergeben würde. Es ist nutzlos, Live-Vorschau Versionen ohne Bild Verarbeitungs Filter bereitzustellen. Wenn eine Anwendung **iwiapreview:: getnewpreview** für einen Treiber ohne Bild Verarbeitungs Filter aufruft, schlägt der Aufruf fehl.

## <a name="examples"></a>Beispiele

Checkimgfilter überprüft, ob der Treiber über einen Bild Verarbeitungs Filter verfügt. Vor dem Aufrufen der Vorschau Komponente sollte eine Anwendung sicherstellen, dass der Treiber über einen Bild Verarbeitungs Filter verfügt.


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



Downloadpreviewimage lädt Bilddaten aus dem Scanner herunter, indem die **iwiapreview:: getnewpreview** -Methode der Vorschau Komponente aufgerufen wird. Anschließend wird detectsubregions aufgerufen, wenn der Anwendungs Benutzer den Segmentierungs Filter aufrufen möchte, der für jeden erkannten Bereich ein untergeordnetes Element unter pWiaItem2 erstellt. Siehe [**erkenctregions**](-wia-iwiasegmentationfilter-detectregions.md) für die detectsubregions-Methode, die in diesem Beispiel verwendet wird.

In diesem Beispiel legt der Anwendungs Benutzer fest, `m_bUseSegmentationFilter` indem Sie auf ein Kontrollkästchen klicken. Wenn die Anwendung dies unterstützt, sollte zuerst überprüft werden, ob der Treiber über einen Segmentierungs Filter verfügt, indem [**checkextension**](-wia-iwiaitem2-checkextension.md)aufgerufen wird. Unter **iwiapreview:: getnewpreview** finden Sie ein Beispiel für die checkimgfilter-Methode, das zeigt, wie dies erreicht werden kann.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




