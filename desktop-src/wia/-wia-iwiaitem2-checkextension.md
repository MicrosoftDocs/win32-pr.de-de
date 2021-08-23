---
description: Überprüft, ob eine angegebene Erweiterung auf dem Computer verfügbar ist und von der IWiaItem2::GetExtension-Methode verwendet werden kann.
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: IWiaItem2::CheckExtension-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CheckExtension
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 50240fbf10155fae555c6cd2e30bf8c86c571b8d52b86e02eab9f5bb11ac17ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965579"
---
# <a name="iwiaitem2checkextension-method"></a>IWiaItem2::CheckExtension-Methode

Überprüft, ob eine angegebene Erweiterung auf dem Computer verfügbar ist und von der [**IWiaItem2::GetExtension-Methode verwendet werden**](-wia-iwiaitem2-getextension.md) kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckExtension(
  [in]  LONG   lFlags,
  [in]  BSTR   bstrName,
  [in]  REFIID riidExtensionInterface,
  [out] BOOL   *pbExtensionExists
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

Gibt den Namen der Erweiterung an.

</dd> <dt>

*riidExtensionInterface* \[ In\]
</dt> <dd>

Typ: **REFIID**

Derzeit nicht verwendet.

</dd> <dt>

*pbExtensionExists* \[ out\]
</dt> <dd>

Typ: **BOOL \***

Empfängt einen Zeiger auf eine **BOOL.**

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**FALSE**


</dt> <dd>

Die angegebene Erweiterung ist nicht verfügbar.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**STIMMT**


</dt> <dd>

Die angegebene Erweiterung ist verfügbar.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Mit dieser Methode können Anwendungen überprüfen, ob eine Erweiterung verfügbar ist, bevor sie die [**IWiaItem2::GetExtension-Methode**](-wia-iwiaitem2-getextension.md) aufrufen. Außerdem kann die Anwendung überprüfen, welche Erweiterungen verfügbar sind, ohne sie gemeinsam zu erstellen, und dann entscheiden, welche Erweiterungen verwendet werden sollen.

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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




