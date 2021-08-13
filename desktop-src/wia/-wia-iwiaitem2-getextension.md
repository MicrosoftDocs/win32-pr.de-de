---
description: Ruft die Erweiterungsschnittstellen ab, die mit einem WIA 2.0-Gerätetreiber (Windows Image Acquisition) verbunden sein können.
ms.assetid: 70f20f33-905c-4a88-8065-1cf876e98302
title: IWiaItem2::GetExtension-Methode (Wia.h)
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
ms.openlocfilehash: 4c9738afe60d79b73149c9dd7dda8c3bbd1017c3b41d023b47160b624bcd7c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450414"
---
# <a name="iwiaitem2getextension-method"></a>IWiaItem2::GetExtension-Methode

Ruft die Erweiterungsschnittstellen ab, die mit einem WIA 2.0-Gerätetreiber (Windows Image Acquisition) verbunden sein können.

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

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*bstrName* \[ In\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen der Erweiterung an, auf die die aufrufende Anwendung einen Zeiger erfordert.

<dt>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>

<span id="SegmentationFilter"></span><span id="segmentationfilter"></span><span id="SEGMENTATIONFILTER"></span>**SegmentationFilter**


</dt> <dd>

Die Segmentierungsfiltererweiterung. Dies ist derzeit der einzige gültige Wert für diesen Parameter.

</dd> </dl> </dd> <dt>

*riidExtensionInterface* \[ In\]
</dt> <dd>

Typ: **REFIID**

Gibt den Bezeichner der Erweiterungsschnittstelle an.

</dd> <dt>

*ppOut* \[ out\]
</dt> <dd>

Typ: **\* \* VOID**

Empfängt die Adresse eines Zeigers auf die Erweiterungsschnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Eine Anwendung ruft diese Methode auf, um ein Erweiterungsobjekt zu erstellen, das eine der WIA 2.0-Treibererweiterungsschnittstellen implementiert. **IWiaItem2::GetExtension** speichert die Adresse der Erweiterungsschnittstelle des Erweiterungsobjekts im *riidExtensionInterface-Parameter.* Die Anwendung verwendet dann den Schnittstellenzeiger zum Aufrufen ihrer Methoden.

Anwendungen müssen die [IUnknown::Release-Methode für](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) die Schnittstellenzeigen aufrufen, die sie über den *riidExtensionInterface-Parameter* erhalten.

## <a name="examples"></a>Beispiele

CreateSegmentationFilter erstellt eine Instanz des Segmentierungsfilters des Treibers ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)), indem **IWiaItem2::GetExtension** auf der übergebenen [**IWiaItem2-Schnittstelle**](-wia-iwiaitem2.md) aufgerufen wird.


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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
