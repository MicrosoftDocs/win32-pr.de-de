---
description: Die FixTimes2-Methode rundet die angegebenen Start- und Stoppzeiten auf die nächsten Rahmengrenzen, wie durch die Einstellung der Bildfrequenz der übergeordneten Gruppe definiert. Diese Methode entspricht IAMTimelineObj::FixTimes, nimmt jedoch REFTIME-Werte an.
ms.assetid: bdb3d999-2c91-4108-9286-c6e1f3362c09
title: IAMTimelineObj::FixTimes2-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.FixTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 74890c2b094172ac3ced0c9fd192a755d051b56df22301b4d64d9003eaa74e9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400905"
---
# <a name="iamtimelineobjfixtimes2-method"></a>IAMTimelineObj::FixTimes2-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die -Methode rundet die angegebenen Start- und Stoppzeiten auf die nächsten Rahmengrenzen, wie in der Einstellung für die Bildfrequenz der `FixTimes2` übergeordneten Gruppe definiert. Diese Methode entspricht [**IAMTimelineObj::FixTimes,**](iamtimelineobj-fixtimes.md)nimmt jedoch [**REFTIME-Werte**](reftime.md) an.

## <a name="syntax"></a>Syntax


```C++
HRESULT FixTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStart* 
</dt> <dd>

Zeiger auf eine Variable, die die Startzeit in Sekunden enthält. Wenn der Aufruf erfolgreich ist, wird diese Variable auf die gerundete Zeit festgelegt.

</dd> <dt>

*Pstop* 
</dt> <dd>

Zeiger auf eine Variable, die die Stoppzeit in Sekunden enthält. Wenn der Aufruf erfolgreich ist, wird diese Variable auf die gerundete Zeit festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich, oder E \_ NOTINTREE, wenn das Objekt nicht Teil einer Gruppe ist.

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

[**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




