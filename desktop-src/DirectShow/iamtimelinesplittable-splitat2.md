---
description: Die SplitAt2-Methode teilt das Objekt zum angegebenen Zeitpunkt auf. Diese Methode entspricht IAMTimelineSplittable::SplitAt, verwendet jedoch einen REFTIME-Wert.
ms.assetid: 33d240db-4ef8-455a-81a6-633ee12837c2
title: IAMTimelineSplittable::SplitAt2-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9c3a5720ade42291037611c155c2cb9e834f0734e7af6e2c36277c409592143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904910"
---
# <a name="iamtimelinesplittablesplitat2-method"></a>IAMTimelineSplittable::SplitAt2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SplitAt2` -Methode teilt das -Objekt zum angegebenen Zeitpunkt auf. Diese Methode entspricht [**IAMTimelineSplittable::SplitAt,**](iamtimelinesplittable-splitat.md)verwendet jedoch einen [**REFTIME-Wert.**](reftime.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT SplitAt2(
   REFTIME Time
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Time* 
</dt> <dd>

Zeit, zu der das Objekt relativ zum Anfang der Zeitachse in Sekunden aufgeteilt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                                   | Beschreibung                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | Nichts aufzuteilen.<br/>                       |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Das -Objekt ist zu diesem Zeitpunkt nicht vorhanden.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

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

[**IAMTimelineSplittable-Schnittstelle**](iamtimelinesplittable.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




