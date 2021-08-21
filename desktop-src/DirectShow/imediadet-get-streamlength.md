---
description: Die methode \_ get StreamLength ruft die Dauer des aktuellen Streams ab.
ms.assetid: b3c13abe-cd56-4960-9862-bda47a0e87ed
title: IMediaDet::get_StreamLength-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_StreamLength
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f29b11c5b9b054a759648343ea8b27c8f883d044cd65073b0bddc5ea8884a6d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154287"
---
# <a name="imediadetget_streamlength-method"></a>IMediaDet::get \_ StreamLength-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `get_StreamLength` -Methode ruft die Dauer des aktuellen Streams ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_StreamLength(
  [out, retval] double *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Empfängt die Dauer des Streams in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Legen Sie vor dem Aufrufen dieser Methode den Dateinamen und stream fest, indem Sie [**IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) und [**IMediaDet::p ut \_ CurrentStream aufrufen.**](imediadet-put-currentstream.md)

Wenn sich die Medienerkennung im Bitmap-Greifmodus befindet, gibt diese Methode E \_ INVALIDARG zurück. Weitere Informationen finden Sie unter [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md).

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK-Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMediaDet-Schnittstelle**](imediadet.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




