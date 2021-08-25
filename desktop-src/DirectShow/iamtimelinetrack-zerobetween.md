---
description: Die ZeroBetween-Methode entfernt alles aus der Spur zwischen den angegebenen Zeiten. Diese Methode teilt alle Objekte auf, die den angegebenen Zeitbereich umfassen, und entfernt die Teile, die in den Bereich fallen.
ms.assetid: df173a3c-147b-4f2d-9bcb-a8c2873f5420
title: IAMTimelineTrack::ZeroBetween-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b5ec57833ed34a432988c42351a333362168112174cccd7a989e0c2e1bddd694
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982900"
---
# <a name="iamtimelinetrackzerobetween-method"></a>IAMTimelineTrack::ZeroBetween-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `ZeroBetween` -Methode entfernt alles aus der Spur zwischen den angegebenen Zeiten. Diese Methode teilt alle Objekte auf, die den angegebenen Zeitbereich umfassen, und entfernt die Teile, die in den Bereich fallen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ZeroBetween(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rtStart* 
</dt> <dd>

Anfang des zu löschenden Bereichs in Einheiten von 100 Nanosekunden.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Ende des zu löschenden Bereichs in Einheiten von 100 Nanosekunden.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMTimelineTrack-Schnittstelle**](iamtimelinetrack.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




