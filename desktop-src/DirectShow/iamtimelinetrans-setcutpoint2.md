---
description: Die SetCutPoint2-Methode legt die Zeit fest, zu der der Übergang von einer Quelle zur nächsten schneidet, wenn der Übergang als Schnitt gerendert wird. Diese Methode entspricht IAMTimelineTrans::SetCutPoint, verwendet jedoch einen REFTIME-Wert.
ms.assetid: d06d3ee7-04a2-4266-9995-bfabea24aef9
title: IAMTimelineTrans::SetCutPoint2-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9d4dedfb31efab45f56229e2dd4db10fc9e43defe822662bc2d7be06f0c1a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502340"
---
# <a name="iamtimelinetranssetcutpoint2-method"></a>IAMTimelineTrans::SetCutPoint2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SetCutPoint2` -Methode legt die Zeit fest, zu der der Übergang von einer Quelle zur nächsten schneidet, wenn der Übergang als Schnitt gerendert wird. Diese Methode entspricht [**IAMTimelineTrans::SetCutPoint,**](iamtimelinetrans-setcutpoint.md)verwendet jedoch einen [**REFTIME-Wert.**](reftime.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetCutPoint2(
   REFTIME TLTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TLTime* 
</dt> <dd>

Schnittpunkt relativ zum Beginn des Übergangs in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

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

[**IAMTimelineTrans-Schnittstelle**](iamtimelinetrans.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




