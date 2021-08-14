---
description: Die SetBufferSamples-Methode gibt an, ob Beispieldaten beim Durchlaufen des Filters in einen Puffer kopiert werden sollen.
ms.assetid: 1ef4508e-441f-45e0-afb4-239dd947284b
title: ISampleGrabber::SetBufferSamples-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetBufferSamples
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c768a21d4e08e6900f3a46f3e398f5040aaf6b6b0bc45c9187ac07821500a372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817995"
---
# <a name="isamplegrabbersetbuffersamples-method"></a>ISampleGrabber::SetBufferSamples-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die **SetBufferSamples-Methode** gibt an, ob Beispieldaten beim Durchlaufen des Filters in einen Puffer kopiert werden sollen.

## <a name="syntax"></a>Syntax


```C++
void SetBufferSamples(
   BOOL BufferThem
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*BufferThem* 
</dt> <dd>

Boolescher Wert, der angibt, ob Beispieldaten gepuffert werden sollen. True gibt an, dass der Filter Beispieldaten in einen internen Puffer kopiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Rufen Sie [**ISampleGrabber::GetCurrentBuffer**](isamplegrabber-getcurrentbuffer.md)auf, um den kopierten Puffer abzurufen.

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

 

 




