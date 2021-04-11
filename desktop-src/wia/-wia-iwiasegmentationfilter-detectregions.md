---
description: Bestimmt die Unterbereiche eines Bilds, das auf dem flachen Platen angeordnet ist, sodass jede Unterregion in einem separaten Bildelement abgerufen werden kann.
ms.assetid: 899d61f0-2dd8-4a68-827e-89e85ebb5143
title: Iwiasegmentationfilter::D etectregions-Methode (WIA. h)
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
ms.openlocfilehash: 94fe2f5076e9ff7cc0de0f7c916f6edacf2d03fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129416"
---
# <a name="iwiasegmentationfilterdetectregions-method"></a>Iwiasegmentationfilter::D etectregions-Methode

Bestimmt die Unterbereiche eines Bilds, das auf dem flachen Platen angeordnet ist, sodass jede Unterregion in einem separaten Bildelement abgerufen werden kann.

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

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*pinputstream* \[ in\]
</dt> <dd>

Typ: **[IStream](/windows/win32/api/objidl/nn-objidl-istream) \** _

Gibt einen Zeiger auf das [IStream](/windows/win32/api/objidl/nn-objidl-istream) -Vorschaubild an.

</dd> <dt>

_pWiaItem2 * \[ in\]
</dt> <dd>

Typ: **[**IWiaItem2**](-wia-iwiaitem2.md) \** _

Gibt einen Zeiger auf das [_ *IWiaItem2* *](-wia-iwiaitem2.md) -Element an, für das *pinputstream abgerufen* wurde. Der Segmentierungs Filter erstellt untergeordnete Elemente für dieses Element.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode bestimmt die Unterbereiche des durch pinputstream dargestellten Bilds. Für jede unterregion, die Sie erkennt, wird ein untergeordnetes Element für das [**IWiaItem2**](-wia-iwiaitem2.md) -Element erstellt, das im *pWiaItem2* -Parameter angegeben ist. Für jedes untergeordnete Element muss der Segmentierungs Filter Werte für das umgebende Rechteck des zu überprüfenden Bereichs festlegen, wobei die folgenden [**Eigenschaften Konstanten für die WIA-Eigenschaft des Scanners**](-wia-wiaitempropscanneritem.md)verwendet werden.

-   [**WIA- \_ IPS- \_ xPos**](-wia-wiaitempropscanneritem.md)
-   [**WIA- \_ IPS ( \_ yPos)**](-wia-wiaitempropscanneritem.md)
-   [**WIA- \_ IPS- \_ XBlock**](-wia-wiaitempropscanneritem.md)
-   [**WIA- \_ IPS \_ yblock**](-wia-wiaitempropscanneritem.md)

Ein erweiterter Filter erfordert möglicherweise auch andere [**Scanner-WIA-Element Eigenschafts Konstanten**](-wia-wiaitempropscanneritem.md) , wie z. b. **WIA- \_ IPS \_ deschiefe \_ X** und **WIA- \_ IPS \_ deschiefe \_ Y**, wenn der Treiber de-Schiefe unterstützt.

Wenn die Anwendung **iwiasegmentationfilter::D etectregions** mehrmals aufruft, muss die Anwendung zunächst die untergeordneten Elemente löschen, die beim letzten Aufruf von **iwiasegmentationfilter::D etectregions** erstellt wurden.

Wenn eine Anwendung Eigenschaften in *pWiaItem2* ändert, muss zwischen dem Abrufen des Bilds in *pinputstream* und dem Aufruf von **iwiasegmentationfilter::D etectregions** die ursprünglichen Eigenschaften (d. h. die Eigenschaften, die das Element beim Abrufen des Streams enthielt) wieder hergestellt werden. Dies kann durch [**getpropertystream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) und [**setpropertystream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream)erreicht werden.

Die Anwendung muss den [IStream](/windows/win32/api/objidl/nn-objidl-istream) zurücksetzen, wenn der zugehörige-Befehl denselben Stream mehrmals an den Segmentierungs Filter übergibt. Die Anwendung muss den Stream auch nach dem anfänglichen Download und vor dem Aufrufen von **iwiasegmentationfilter::D etectregions** zurücksetzen.

## <a name="examples"></a>Beispiele

Die Segmentierung führt die Regions Erkennung im Stream () aus, die an `pImageStream` detectsubregions weitergeleitet wird. Weitere Informationen finden Sie in diesem Beispiel in der [**GetExtension**](-wia-iwiaitem2-getextension.md) für die in diesem Beispiel verwendete Methode "".


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



Downloadpreviewimage lädt Bilddaten aus dem Scanner herunter, indem die [**getnewpreview**](-wia-iwiapreview-getnewpreview.md) -Methode der Vorschau Komponente aufgerufen wird. Anschließend wird detectsubregions aufgerufen, wenn der Anwendungs Benutzer den Segmentierungs Filter aufrufen möchte, der für jeden erkannten Bereich ein untergeordnetes Element unter pWiaItem2 erstellt. Weitere Informationen finden Sie unter **iwiasegmentationfilter::D etectregions** für die detectsubregions-Methode, die in diesem Beispiel verwendet wird.

In diesem Beispiel legt der Anwendungs Benutzer fest, `m_bUseSegmentationFilter` indem Sie auf ein Kontrollkästchen klicken. Wenn die Anwendung dies unterstützt, sollte zuerst überprüft werden, ob der Treiber über einen Segmentierungs Filter verfügt, indem [**checkextension**](-wia-iwiaitem2-checkextension.md)aufgerufen wird. Unter [**getnewpreview**](-wia-iwiapreview-getnewpreview.md) finden Sie ein Beispiel für die checkimgfilter-Methode, das zeigt, wie dies erreicht werden kann.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
