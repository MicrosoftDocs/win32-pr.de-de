---
description: 'Mit der SetCutPoint2-Methode wird die Zeit festgelegt, zu der der Übergang von einer Quelle zum nächsten schneidet, wenn der Übergang als Ausschneiden gerendert wird. Diese Methode entspricht iamtimelinetrans:: setcutpoint, aber nimmt einen reftime-Wert an.'
ms.assetid: d06d3ee7-04a2-4266-9995-bfabea24aef9
title: 'Iamtimelinetrans:: SetCutPoint2-Methode (qedit. h)'
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
ms.openlocfilehash: 117ec522416f0d5722c8ef7aa17cd6e81720b4c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371998"
---
# <a name="iamtimelinetranssetcutpoint2-method"></a>Iamtimelinetrans:: SetCutPoint2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetCutPoint2` Methode legt die Zeit fest, zu der der Übergang von einer Quelle zum nächsten abbricht, wenn der Übergang als Ausschneiden gerendert wird. Diese Methode entspricht [**iamtimelinetrans:: setcutpoint**](iamtimelinetrans-setcutpoint.md), aber nimmt einen [**reftime**](reftime.md) -Wert an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetCutPoint2(
   REFTIME TLTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tltime* 
</dt> <dd>

Der Ausschneide Punkt relativ zum Anfang des Übergangs in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

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

[**Iamtimelinetrans-Schnittstelle**](iamtimelinetrans.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




