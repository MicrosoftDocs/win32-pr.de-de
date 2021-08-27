---
description: Die IsNormalRate-Methode gibt an, ob der Clip mit der normalen Wiedergaberate wiedergegeben wird. Das heißt, die Wiedergaberate der ursprünglichen Datei.
ms.assetid: 4a8fe415-f9eb-450d-9a75-e528577050d9
title: IAMTimelineSrc::IsNormalRate-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.IsNormalRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4d1c0b355b0eedee29dafb92debbabac5c7b3e574d2f161827626bc73f72c035
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083870"
---
# <a name="iamtimelinesrcisnormalrate-method"></a>IAMTimelineSrc::IsNormalRate-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `IsNormalRate` -Methode gibt an, ob der Clip mit der normalen Wiedergaberate wiedergegeben wird, d. h. der Wiedergaberate der ursprünglichen Datei.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsNormalRate(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* 
</dt> <dd>

Empfängt einen booleschen Wert, der angibt, wie der Clip gerendert wird. Wenn der Wert **TRUE** ist, wird der Clip mit der normalen Rate wiedergegeben. Andernfalls wird sie schneller oder langsamer als normal wiedergegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die Wiedergaberate eines Clips wird durch die Start- und Beendigungszeiten des Mediums relativ zu den Zeitachsenzeiten bestimmt:


```C++
Playback rate = (Media Stop <entity type="mdash"/> Media Start) / (Timeline Stop <entity type="mdash"/> Timeline Start)
```



Wenn dieses Verhältnis gleich 1 ist, wird der Clip mit der erstellungsgeschwindigkeit wiedergegeben. Andernfalls wird sie schneller oder langsamer wiedergegeben. Weitere Informationen finden Sie unter [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Requirements (Anforderungen)



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

 

 




