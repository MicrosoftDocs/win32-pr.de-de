---
description: Filtert das Vorschaubild.
ms.assetid: 1710211a-a35c-4a51-b3bb-6f03f234f247
title: IWiaImageFilter::FilterPreviewImage-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.FilterPreviewImage
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 96b1d8ce92a847dcd4ffcebca6b45df2b652ad74c1216fc60b8aac72bb6a12ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659720"
---
# <a name="iwiaimagefilterfilterpreviewimage-method"></a>IWiaImageFilter::FilterPreviewImage-Methode

Filtert das Vorschaubild.

## <a name="syntax"></a>Syntax


```C++
HRESULT FilterPreviewImage(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaChildItem2,
  [in] RECT      InputImageExtents,
  [in] IStream   *pInputStream
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lFlags* \[ In\]
</dt> <dd>

Typ: **LONG**

Nicht verwendet. Auf 0 festlegen.

</dd> <dt>

*pWiaChildItem2* \[ In\]
</dt> <dd>

Typ: **[ **IWiaItem2**](-wia-iwiaitem2.md)\***

Das Element, das verarbeitet wird.

</dd> <dt>

*InputImageExtents* \[ In\]
</dt> <dd>

Typ: **RECT**

Die Koordinaten (im physischen Erfassungsbereich) des Bilds, das von der Vorschaukomponente intern zwischengespeichert wird.

</dd> <dt>

*pInputStream* \[ In\]
</dt> <dd>

Typ: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\***

Ein Zeiger auf die [IStream-Schnittstelle](/windows/win32/api/objidl/nn-objidl-istream) für die zwischengespeicherten Bilddaten, die gefiltert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode nicht direkt aus Ihrer Anwendung auf.

*pWiaChildItem2* muss ein untergeordnetes Element von *pWiaItem2* sein, das an [**IWiaImageFilter::InitializeFilter übergeben wurde.**](-wia-iwiaimagefilter-initializefilter.md)

*InputImageExtents* ist erforderlich, da der Bildverarbeitungsfilter für das Ausschneiden des Bildbereichs zuständig ist, den *pWiaChildItem2* aus den Bilddaten darstellt, die über *pInputStream* übergeben werden.

Eine Anwendung muss sicherstellen, dass *pWiaChildItem2* über das gleiche Bildformat (WIA IPA FORMAT), die gleiche Auflösung (WIA IPS XRES und WIA IPS YRES) und die gleiche Bittiefe \_ \_ \_ \_ \_ \_ (WIA IPA DEPTH) verfügt wie \_ \_ *pWiaItem2,* als es an [**GetNewPreview übergeben wurde.**](-wia-iwiapreview-getnewpreview.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
