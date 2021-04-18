---
description: 'Mit der FixTimes2-Methode werden die angegebenen Start-und Endzeit Zeiten auf die nächsten Frame Begrenzungen gerundet, wie in der Frameraten Einstellung der übergeordneten Gruppe definiert. Diese Methode entspricht iamtimelineobj:: fixtimes, erfordert jedoch reftime-Werte.'
ms.assetid: bdb3d999-2c91-4108-9286-c6e1f3362c09
title: 'Iamtimelineobj:: FixTimes2-Methode (qedit. h)'
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
ms.openlocfilehash: 48b487d8dc17d6b815ea9dff79fc58af953b0bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372762"
---
# <a name="iamtimelineobjfixtimes2-method"></a>Iamtimelineobj:: FixTimes2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

`FixTimes2`Mit der-Methode werden die angegebenen Start-und Endzeit Zeiten auf die nächsten Frame Begrenzungen gerundet, wie in der Frameraten Einstellung der übergeordneten Gruppe definiert. Diese Methode entspricht [**iamtimelineobj:: fixtimes**](iamtimelineobj-fixtimes.md), erfordert jedoch [**reftime**](reftime.md) -Werte.

## <a name="syntax"></a>Syntax


```C++
HRESULT FixTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PStart* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Startzeit in Sekunden enthält. Wenn der Aufruf erfolgreich ist, wird diese Variable auf die abgerundete Zeit festgelegt.

</dd> <dt>

*pstopps* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Endzeit in Sekunden enthält. Wenn der Aufruf erfolgreich ist, wird diese Variable auf die abgerundete Zeit festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder E \_ notintree zurück, wenn das Objekt nicht Teil einer Gruppe ist.

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

[**Iamtimelineobj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




