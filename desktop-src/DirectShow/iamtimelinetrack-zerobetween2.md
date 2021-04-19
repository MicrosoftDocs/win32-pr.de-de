---
description: 'Die ZeroBetween2-Methode entfernt alle Elemente aus der Spur zwischen den angegebenen Uhrzeiten. Diese Methode entspricht iamtimelinetrack:: zerobetween, erfordert jedoch reftime-Werte.'
ms.assetid: 56b9be30-cc3f-4843-bf35-910498242d71
title: 'Iamtimelinetrack:: ZeroBetween2-Methode (qedit. h)'
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
ms.openlocfilehash: 27e3ab5cc2a631cb54c926824c2f3410413cd981
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360327"
---
# <a name="iamtimelinetrackzerobetween2-method"></a>Iamtimelinetrack:: ZeroBetween2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `ZeroBetween2` Methode entfernt alle Elemente aus der Spur zwischen den angegebenen Uhrzeiten. Diese Methode entspricht [**iamtimelinetrack:: zerobetween**](iamtimelinetrack-zerobetween.md), erfordert jedoch [**reftime**](reftime.md) -Werte.

## <a name="syntax"></a>Syntax


```C++
HRESULT ZeroBetween2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rtstart* 
</dt> <dd>

Der Anfang des Bereichs, der gelöscht werden soll (in Sekunden).

</dd> <dt>

*rtend* 
</dt> <dd>

Das Ende des Bereichs, der gelöscht werden soll (in Sekunden).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Die folgenden Werte sind möglich.



| Rückgabecode                                                                             | Beschreibung                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Der Zeitbereich fällt über alle Elemente in der Spur hinaus.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                             |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iamtimelinetrack-Schnittstelle**](iamtimelinetrack.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




