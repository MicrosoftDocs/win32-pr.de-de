---
description: Ruft die Erweiterungs Schnittstellen ab, die möglicherweise mit einem Windows-Abbild Erfassungs-Gerätetreiber (WIA) 2,0 geliefert werden.
ms.assetid: 70f20f33-905c-4a88-8065-1cf876e98302
title: 'IWiaItem2:: GetExtension-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2fea4c4b9a2dd909b7ec49097ee94664b47f7e47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041759"
---
# <a name="iwiaitem2getextension-method"></a>IWiaItem2:: GetExtension-Methode

Ruft die Erweiterungs Schnittstellen ab, die möglicherweise mit einem Windows-Abbild Erfassungs-Gerätetreiber (WIA) 2,0 geliefert werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] VOID   **ppOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*bstrinname* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen der Erweiterung an, auf die die aufrufenden Anwendung einen Zeiger erfordert.

<dt>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**Segmentationfilter**


</dt> <dd>

Die Segmentierungs Filter Erweiterung. Dies ist zurzeit der einzige gültige Wert für diesen Parameter.

</dd> </dl> </dd> <dt>

*riidextensioninterface* \[ in\]
</dt> <dd>

Typ: **refID**

Gibt den Bezeichner der Erweiterungsschnittstelle an.

</dd> <dt>

*ppOut* \[ vorgenommen\]
</dt> <dd>

Typ: **void \* \***

Empfängt die Adresse eines Zeigers auf die Erweiterungsschnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung ruft diese Methode auf, um ein Erweiterungs Objekt zu erstellen, das eine der WIA 2,0-Treiber Erweiterungs Schnittstellen implementiert. **IWiaItem2:: GetExtension** speichert die Adresse der Erweiterungsschnittstelle des Erweiterungs Objekts im *riidextensioninterface* -Parameter. Die Anwendung verwendet dann den Schnittstellen Zeiger, um die Methoden aufzurufen.

Anwendungen müssen die [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Methode für die Schnittstellen Zeiger aufrufen, die Sie über den *riidextensioninterface* -Parameter empfangen.

## <a name="examples"></a>Beispiele

Createsegmentationfilter erstellt eine Instanz des Segmentierungs Filters des Treibers ([**iwiasegmentationfilter**](-wia-iwiasegmentationfilter.md)) durch Aufrufen von **IWiaItem2:: GetExtension** für die eingegangene [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle.


```C++
HRESULT
CreateSegmentationFilter(
   IWiaItem2               *pWiaItem2,
   IWiaSegmentationFilter  **ppSegmentationFilter)
{
   HRESULT                 hr         = S_OK;
   IWiaSegmentationFilter *pSegFilter = NULL;
    
   if (!pWiaItem2 || !ppSegmentationFilter)
   {
      hr = E_INVALIDARG;
   }

   if (SUCCEEDED(hr))
   {
      BSTR    bstrFilterString = SysAllocString(WIA_SEGMENTATION_FILTER_STR);

      if (bstrFilterString)
      {
         hr = pWiaItem2->GetExtension(0,
                                      bstrFilterString,
                                      IID_IWiaSegmentationFilter,
                                      (void**)&pSegFilter);
         SysFreeString(bstrFilterString);
         bstrFilterString = NULL;
      }
      else
      {
         hr = E_OUTOFMEMORY;
      }
   }

   if (SUCCEEDED(hr))
   {
     *ppSegmentationFilter = pSegFilter;
      pSegFilter = NULL;
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



 

 
