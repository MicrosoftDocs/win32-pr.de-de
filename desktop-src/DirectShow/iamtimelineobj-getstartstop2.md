---
description: Die GetStartStop2-Methode ruft die Start- und Stoppzeiten des Objekts relativ zum übergeordneten Element des Objekts ab. Diese Methode entspricht IAMTimelineObj::GetStartStop, nimmt jedoch REFTIME-Werte an.
ms.assetid: 140842f5-3a24-4947-a360-ef97cba414ee
title: IAMTimelineObj::GetStartStop2-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1ff1644c2ba83848d0c9efa1b850a65aa8cfd1de1607a9fa0cabbab39579e0db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155451"
---
# <a name="iamtimelineobjgetstartstop2-method"></a>IAMTimelineObj::GetStartStop2-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die -Methode ruft die Start- und Stoppzeiten des Objekts `GetStartStop2` relativ zum übergeordneten Element des Objekts ab. Diese Methode entspricht [**IAMTimelineObj::GetStartStop,**](iamtimelineobj-getstartstop.md)nimmt jedoch [**REFTIME-Werte**](reftime.md) an.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStartStop2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStart* 
</dt> <dd>

Empfängt die Startzeit in Sekunden.

</dd> <dt>

*Pstop* 
</dt> <dd>

Empfängt die Stoppzeit in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




