---
description: Die InsertSpace2-Methode teilt alle Objekte auf, die zum angegebenen Zeitpunkt vorhanden sind, und fügt Leerzeichen zwischen ihnen ein. Diese Methode entspricht IAMTimelineTrack::InsertSpace, verwendet jedoch REFTIME-Werte.
ms.assetid: 818a1dad-0c8d-4728-82d6-cd52c6c830a2
title: IAMTimelineTrack::InsertSpace2-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f851e6bdccb755977210fcd67e7ce0bb6cb270ec3ff6a4f1fed4806a035a11a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052250"
---
# <a name="iamtimelinetrackinsertspace2-method"></a>IAMTimelineTrack::InsertSpace2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `InsertSpace2` -Methode teilt alle Objekte auf, die zum angegebenen Zeitpunkt vorhanden sind, und fügt Leerzeichen zwischen ihnen ein. Diese Methode entspricht [**IAMTimelineTrack::InsertSpace,**](iamtimelinetrack-insertspace.md)verwendet jedoch [**REFTIME-Werte.**](reftime.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT InsertSpace2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rtStart* 
</dt> <dd>

Uhrzeit, zu der die Aufteilung und der Startpunkt des eingefügten Leerzeichens in Sekunden erstellt werden sollen.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Endpunkt des eingefügten Leerzeichens in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Rückgabewerte sind:



| Rückgabecode                                                                                   | Beschreibung                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | Zum angegebenen Zeitpunkt sind keine Objekte vorhanden.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiges Argument.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                        |



 

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

 

 




