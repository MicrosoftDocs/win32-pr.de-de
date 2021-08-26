---
description: Die SetStartStop2-Methode legt die Start- und Beendigungszeiten des Objekts relativ zum übergeordneten Objekt fest. Diese Methode entspricht IAMTimelineObj::SetStartStop, verwendet jedoch REFTIME-Werte.
ms.assetid: 0fc79c82-d8e1-4b87-9e59-6d9e6ca614f3
title: IAMTimelineObj::SetStartStop2-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 30e7f9e6ce54cb86e2eee486937841842311dd498b42ec42e101128612bf16d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086830"
---
# <a name="iamtimelineobjsetstartstop2-method"></a>IAMTimelineObj::SetStartStop2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SetStartStop2` -Methode legt die Start- und Beendigungszeiten des Objekts relativ zum übergeordneten Objekt fest. Diese Methode entspricht [**IAMTimelineObj::SetStartStop,**](iamtimelineobj-setstartstop.md)verwendet jedoch [**REFTIME-Werte.**](reftime.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStartStop2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Start* 
</dt> <dd>

Neue Startzeit in Sekunden oder –1, um die vorhandene Startzeit beizubehalten.

</dd> <dt>

*Beenden* 
</dt> <dd>

Neue Beendigungszeit in Sekunden oder –1, um die vorhandene Beendigungszeit beizubehalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück:



| Rückgabecode                                                                                  | Beschreibung                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Ungültiges Argument.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>    | Nicht implementiert.<br/>  |



 

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

[**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




