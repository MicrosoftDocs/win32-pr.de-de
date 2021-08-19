---
description: Die ModifyStopTime2-Methode legt die Beendigungszeit fest. Diese Methode entspricht IAMTimelineSrc::ModifyStopTime, verwendet jedoch einen REFTIME-Wert.
ms.assetid: 8bebda47-3e52-42a2-870c-acc14561fa25
title: IAMTimelineSrc::ModifyStopTime2-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.ModifyStopTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fa2ec7a019200f91c9fb2a894c978ce93896926024f55efb229c7e5fde6fbe85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952809"
---
# <a name="iamtimelinesrcmodifystoptime2-method"></a>IAMTimelineSrc::ModifyStopTime2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `ModifyStopTime2` -Methode legt die Beendigungszeit fest. Diese Methode entspricht [**IAMTimelineSrc::ModifyStopTime,**](iamtimelinesrc-modifystoptime.md)verwendet jedoch einen [**REFTIME-Wert.**](reftime.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT ModifyStopTime2(
   REFTIME Stop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Beenden* 
</dt> <dd>

Neue Beendigungszeit in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich, oder E \_ INVALIDARG, wenn die angegebene Zeit ungültig ist.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMTimelineSrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




