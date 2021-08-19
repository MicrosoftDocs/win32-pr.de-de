---
description: Die ModifyStopTime-Methode legt die Beendigungszeit relativ zur Zeitachse fest.
ms.assetid: 0d9b6cf7-d029-4c35-9045-82cbeff1e3ae
title: IAMTimelineSrc::ModifyStopTime-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f6d611395ad8989ea551fb98d1a3d538786881b0a5afc908a030367cac52ee80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952819"
---
# <a name="iamtimelinesrcmodifystoptime-method"></a>IAMTimelineSrc::ModifyStopTime-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `ModifyStopTime` -Methode legt die Beendigungszeit relativ zur Zeitachse fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT ModifyStopTime(
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Beenden* 
</dt> <dd>

Neue Beendigungszeit in Einheiten von 100 Nanosekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder E \_ INVALIDARG zurück, wenn die angegebene Zeit ungültig ist.

## <a name="remarks"></a>Hinweise

Diese Methode entspricht dem Aufrufen von [**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md) mit der ursprünglichen Startzeit und einer neuen Beendigungszeit.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

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

 

 




