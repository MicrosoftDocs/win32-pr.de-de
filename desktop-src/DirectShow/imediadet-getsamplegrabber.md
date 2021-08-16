---
description: Die GetSampleGrabber-Methode ruft einen Zeiger auf die ISampleGrabber-Schnittstelle ab, mit der eine Anwendung einzelne Beispiele aus einem Medienstream abrufen kann.
ms.assetid: ecfa1909-f1ba-40ac-a0fc-8bfbeed8d148
title: IMediaDet::GetSampleGrabber-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.GetSampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f2c3c580a44b9cff35d7ee801cfc611b5cf8a8df828f54c28b022e5c1a1b862a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819042"
---
# <a name="imediadetgetsamplegrabber-method"></a>IMediaDet::GetSampleGrabber-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetSampleGrabber` -Methode ruft einen Zeiger auf die [**ISampleGrabber-Schnittstelle**](isamplegrabber.md) ab, die es einer Anwendung ermöglicht, einzelne Beispiele aus einem Medienstream abzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSampleGrabber(
  [out] ISampleGrabber **ppVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppVal* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die [**ISampleGrabber-Schnittstelle.**](isamplegrabber.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Rufen Sie [**IMediaDet::EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md) auf, bevor Sie diese Methode aufrufen. Mit der [**ISampleGrabber-Schnittstelle**](isamplegrabber.md) können Sie einzelne Medienbeispiele aus dem Stream abrufen. Wenn Sie nur eine Bitmap aus einem Videoframe benötigen, rufen Sie stattdessen die [**IMediaDet::GetBitmapBits-Methode**](imediadet-getbitmapbits.md) auf. Die **ISampleGrabber-Schnittstelle** ist flexibler, erfordert jedoch mehr Arbeit durch die Anwendung.

Wenn diese Methode erfolgreich ist, verfügt die [**zurückgegebene ISampleGrabber-Schnittstelle**](isamplegrabber.md) über einen ausstehenden Verweiszähler. Stellen Sie sicher, dass Sie die Schnittstelle freigeben, wenn Sie sie nicht mehr verwenden.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IMediaDet-Schnittstelle**](imediadet.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




