---
description: Die SampleCB-Methode ist eine Rückrufmethode, die einen Zeiger auf das Medienbeispiel empfängt.
ms.assetid: e919b694-75cb-48c6-8427-5a7a886e0ff3
title: ISampleGrabberCB::SampleCB-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB.SampleCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e98377050ec98cdccaedd54119afb6cdaccbaee56256f1406bb190d3ea875bb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817512"
---
# <a name="isamplegrabbercbsamplecb-method"></a>ISampleGrabberCB::SampleCB-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SampleCB` -Methode ist eine Rückrufmethode, die einen Zeiger auf das Medienbeispiel empfängt.

## <a name="syntax"></a>Syntax


```C++
HRESULT SampleCB(
   double       SampleTime,
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SampleTime* 
</dt> <dd>

Startzeit des Beispiels in Sekunden.

</dd> <dt>

*pSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich, oder andernfalls einen **HRESULT-Fehlercode.**

## <a name="remarks"></a>Hinweise

Rufen Sie [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md)auf, um den Rückruf einzurichten.

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

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> <dt>

[**ISampleGrabberCB-Schnittstelle**](isamplegrabbercb.md)
</dt> </dl>

 

 




