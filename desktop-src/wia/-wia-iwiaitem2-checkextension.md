---
description: 'Überprüft, ob eine angegebene Erweiterung auf dem Computer verfügbar ist und von der IWiaItem2:: GetExtension-Methode verwendet werden kann.'
ms.assetid: 672f6418-4ce3-4570-a412-fe639c9f5eb8
title: 'IWiaItem2:: checkextension-Methode (WIA. h)'
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
ms.openlocfilehash: 65b0b5b3ace1634a20dfa63382d82099fef0686e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357397"
---
# <a name="iwiaitem2checkextension-method"></a>IWiaItem2:: checkextension-Methode

Überprüft, ob eine angegebene Erweiterung auf dem Computer verfügbar ist und von der [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) -Methode verwendet werden kann.

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

*lFlags* \[ in\]
</dt> <dd>

Type: **Long**

Derzeit nicht verwendet. Sollte auf Null festgelegt werden.

</dd> <dt>

*bstrinname* \[ in\]
</dt> <dd>

Typ: **BSTR**

Gibt den Namen der Erweiterung an.

</dd> <dt>

*riidextensioninterface* \[ in\]
</dt> <dd>

Typ: **refID**

Derzeit nicht verwendet.

</dd> <dt>

*pbextensionist vorhanden* \[ vorgenommen\]
</dt> <dd>

Typ: **bool \** _

Empfängt einen Zeiger auf einen _ * bool * *.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**Alarm**


</dt> <dd>

Die angegebene Erweiterung ist nicht verfügbar.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**Fall**


</dt> <dd>

Die angegebene Erweiterung ist verfügbar.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Mit dieser Methode können Anwendungen überprüfen, ob eine Erweiterung verfügbar ist, bevor Sie die [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) -Methode aufrufen. Außerdem kann die Anwendung überprüfen, welche Erweiterungen verfügbar sind, ohne Sie gemeinsam zu erstellen, und dann entscheiden, welche Erweiterungen verwendet werden sollen.

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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




