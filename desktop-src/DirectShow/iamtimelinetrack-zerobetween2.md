---
description: Die ZeroBetween2-Methode entfernt alles aus der Spur zwischen den angegebenen Zeiten. Diese Methode entspricht IAMTimelineTrack::ZeroBetween, verwendet jedoch REFTIME-Werte.
ms.assetid: 56b9be30-cc3f-4843-bf35-910498242d71
title: IAMTimelineTrack::ZeroBetween2-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72ea9d96be976f1b09e1cdc9721eb5eebe7adce2905d7a028d70a9ff50ff58bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952779"
---
# <a name="iamtimelinetrackzerobetween2-method"></a>IAMTimelineTrack::ZeroBetween2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `ZeroBetween2` -Methode entfernt alles aus der Spur zwischen den angegebenen Zeiten. Diese Methode entspricht [**IAMTimelineTrack::ZeroBetween,**](iamtimelinetrack-zerobetween.md)verwendet jedoch [**REFTIME-Werte.**](reftime.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT ZeroBetween2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rtStart* 
</dt> <dd>

Anfang des bereichs, der gelöscht werden soll, in Sekunden.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Ende des zu löschende Bereichs in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                             | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Der Zeitbereich geht über alles hinaus, was in der Spur vorliegt.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                             |



 

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

[**IAMTimelineTrack-Schnittstelle**](iamtimelinetrack.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




