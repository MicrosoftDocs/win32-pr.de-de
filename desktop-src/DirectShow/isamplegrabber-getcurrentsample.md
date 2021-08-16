---
description: Die GetCurrentSample-Methode ist nicht implementiert.
ms.assetid: 0c903498-3c1d-4e95-a797-ca8cfded25f2
title: ISampleGrabber::GetCurrentSample-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentSample
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4f86d0ec8c0d405c29811e6bfa58e3fdeb69dbf923df5b3d028dcc938fbbca78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818005"
---
# <a name="isamplegrabbergetcurrentsample-method"></a>ISampleGrabber::GetCurrentSample-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetCurrentSample`-Methode ist nicht implementiert.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCurrentSample(
   IMediaSample **ppSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppSample* 
</dt> <dd>

Reserviert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ NOTIMPL zurück.

## <a name="remarks"></a>Hinweise

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

[Verwenden des Beispielgrabbers](using-the-sample-grabber.md)
</dt> <dt>

[**ISampleGrabber-Schnittstelle**](isamplegrabber.md)
</dt> </dl>

 

 




