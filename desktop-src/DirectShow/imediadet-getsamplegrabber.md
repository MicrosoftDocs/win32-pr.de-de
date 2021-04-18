---
description: Die getsamplegrabber-Methode ruft einen Zeiger auf die isamplegrabber-Schnittstelle ab, die einer Anwendung das Abrufen einzelner Beispiele aus einem Mediendaten Strom ermöglicht.
ms.assetid: ecfa1909-f1ba-40ac-a0fc-8bfbeed8d148
title: 'Imediadet:: getsamplegrabber-Methode (qedit. h)'
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
ms.openlocfilehash: e83de26f1c2186293265dc39db603e0a9cf31436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368519"
---
# <a name="imediadetgetsamplegrabber-method"></a>Imediadet:: getsamplegrabber-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetSampleGrabber` Methode ruft einen Zeiger auf die [**isamplegrabber**](isamplegrabber.md) -Schnittstelle ab, die einer Anwendung das Abrufen einzelner Beispiele aus einem Mediendaten Strom ermöglicht.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSampleGrabber(
  [out] ISampleGrabber **ppVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppval* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**isamplegrabber**](isamplegrabber.md) -Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Rufen Sie [**imediadet:: enterbitmapgrabmode**](imediadet-enterbitmapgrabmode.md) auf, bevor Sie diese Methode aufrufen. Mit der [**isamplegrabber**](isamplegrabber.md) -Schnittstelle können Sie einzelne Medien Beispiele aus dem Stream abrufen. Wenn Sie nur eine Bitmap aus einem Videoframe benötigen, können Sie stattdessen die [**imediadet:: getbitmapbits**](imediadet-getbitmapbits.md) -Methode aufrufen. Die **isamplegrabber** -Schnittstelle ist flexibler, erfordert aber mehr Arbeit durch die Anwendung.

Wenn diese Methode erfolgreich ausgeführt wird, hat die von ihr zurückgegebene [**isamplegrabber**](isamplegrabber.md) -Schnittstelle einen ausstehenden Verweis Zähler. Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imediadet-Schnittstelle**](imediadet.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




