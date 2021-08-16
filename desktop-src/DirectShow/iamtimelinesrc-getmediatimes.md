---
description: Die GetMediaTimes-Methode ruft die Start- und Beendigungszeiten des Mediums ab.
ms.assetid: c6a7d992-ceb5-4378-aee2-f2d778b41516
title: IAMTimelineSrc::GetMediaTimes-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.GetMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a2a4b3fc716ba0865a010155e2f1e8a592cab396f5efb0c2d4afa3264da4a337
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756040"
---
# <a name="iamtimelinesrcgetmediatimes-method"></a>IAMTimelineSrc::GetMediaTimes-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetMediaTimes` -Methode ruft die Start- und Beendigungszeiten des Mediums ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStart* 
</dt> <dd>

Empfängt die Startzeit des Mediums in Einheiten von 100 Nanosekunden.

</dd> <dt>

*Pstop* 
</dt> <dd>

Empfängt die Medienstoppzeit in Einheiten von 100 Nanosekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die Medienzeiten sind relativ zur ursprünglichen Mediendatei. Weitere Informationen finden Sie unter [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

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

[**IAMTimelineSrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




