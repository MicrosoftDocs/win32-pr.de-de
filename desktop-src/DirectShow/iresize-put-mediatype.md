---
description: Die put \_ MediaType-Methode legt den Ausgabemedientyp für den Resizerfilter fest.
ms.assetid: e213179e-cc88-4365-aaa0-51d4b9c97476
title: IResize::p ut_MediaType-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_MediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6c26878af6f091efd3c3f321cb073ce51a8e6236d4bafa326ab99f85f39e1a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818201"
---
# <a name="iresizeput_mediatype-method"></a>IResize::p ut \_ MediaType-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `put_MediaType` -Methode legt den Ausgabemedientyp für den Resizer-Filter fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_MediaType(
  [in] const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmt* \[ In\]
</dt> <dd>

Zeiger auf eine [**AM \_ MEDIA \_ TYPE-Struktur,**](/windows/win32/api/strmif/ns-strmif-am_media_type) die den Medientyp enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

DES ruft diese Methode auf, bevor sie den Ausgabepin des Filters verbindet. Verwenden Sie den Medientyp als Medientyp des Ausgabepins. Geben Sie diesen Medientyp in der [**CTransformFilter::GetMediaType-Methode**](ctransformfilter-getmediatype.md) zurück, und überprüfen Sie agsint diesen Typ in der [**CTransformFilter::CheckTransform-Methode.**](ctransformfilter-checktransform.md) DES ruft diese Methode nie auf, nachdem der Ausgabepin verbunden wurde.

Derzeit legt DES den Ausgabemedientyp immer auf ein unkomprimiertes RGB-Format mit einem **VIDEOINFOHEADER-Formatblock** fest (Formattyp entspricht FORMAT \_ VideoInfo). Der Untertyp kann MEDIASUBTYPE \_ ARGB32 sein, was auf 32-Bit-RGB mit einem Alphakanal hinweist.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | DirectX 9.0 oder höher<br/>                                                         |
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> <dt>

[**IResize-Schnittstelle**](iresize.md)
</dt> </dl>

 

 




