---
description: Die FixMediaTimes-Methode rundet die angegebenen Zeitwerte auf die nächste Framegrenze, wie durch die Ausgabebildrate definiert. Im Allgemeinen müssen Anwendungen diese Methode nicht aufrufen.
ms.assetid: 11537715-3be1-4a3c-8700-50b13835ffe9
title: IAMTimelineSrc::FixMediaTimes-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dcace4e501a27b1f82b148533f382f5c86bafb17d9bf34343f1e43a8893672c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052400"
---
# <a name="iamtimelinesrcfixmediatimes-method"></a>IAMTimelineSrc::FixMediaTimes-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die -Methode rundet die angegebenen Zeitwerte auf die nächste Framegrenze, wie durch `FixMediaTimes` die Ausgabebildrate definiert. Im Allgemeinen müssen Anwendungen diese Methode nicht aufrufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT FixMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStart* 
</dt> <dd>

Zeiger auf eine Variable, die die Startzeit in Einheiten von 100 Nanosekunden enthält. Wenn der Aufruf erfolgreich ist, wird diese Variable auf die gerundete Zeit festgelegt.

</dd> <dt>

*Pstop* 
</dt> <dd>

Zeiger auf eine Variable, die die Stoppzeit in Einheiten von 100 Nanosekunden enthält. Wenn der Aufruf erfolgreich ist, wird diese Variable auf die gerundete Zeit festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode ähnelt der [**IAMTimelineObj::FixTimes-Methode,**](iamtimelineobj-fixtimes.md) behält jedoch das ursprüngliche Verhältnis von Medienzeiten und Zeitachsenzeiten bei. Nur das Runden der Zeiten auf die nächste Rahmengrenze könnte dieses Verhältnis verzerren.

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

[**IAMTimelineSrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




