---
description: Die InsertSpace-Methode teilt alle Objekte auf, die zum angegebenen Zeitpunkt vorhanden sind, und fügt Leerzeichen zwischen ihnen ein.
ms.assetid: f9e48f58-1867-405c-b208-1ab781912aa1
title: IAMTimelineTrack::InsertSpace-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a51e89a72d813e1f5a9c1c05b1a46b6674906284b61b4036c164af87af9a4559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399177"
---
# <a name="iamtimelinetrackinsertspace-method"></a>IAMTimelineTrack::InsertSpace-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `InsertSpace` -Methode teilt alle Objekte auf, die zum angegebenen Zeitpunkt vorhanden sind, und fügt Leerzeichen zwischen ihnen ein.

## <a name="syntax"></a>Syntax


```C++
HRESULT InsertSpace(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rtStart* 
</dt> <dd>

Die Zeit, zu der die Aufteilung erstellt werden soll, und der Anfangspunkt des eingefügten Leerzeichens in Einheiten von 100 Nanosekunden.

</dd> <dt>

*rtEnd* 
</dt> <dd>

Der Endpunkt des eingefügten Leerzeichens in Einheiten von 100 Nanosekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Rückgabewerte sind:



| Rückgabecode                                                                                   | Beschreibung                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | Zum angegebenen Zeitpunkt sind keine Objekte enthalten.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Ungültiges Argument.<br/>                           |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                        |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

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

 

 




