---
description: Die SetCutPoint-Methode legt die Zeit fest, zu der der Übergang von einer Quelle zur nächsten schneidet, wenn der Übergang als Schnitt gerendert wird.
ms.assetid: 2660f4a8-e249-45d7-8866-02a9f2ef52b8
title: IAMTimelineTrans::SetCutPoint-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c411925ebe10ad35641e38ae2332605d7691ae24f0cc96ff716bd7d00e6603f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052070"
---
# <a name="iamtimelinetranssetcutpoint-method"></a>IAMTimelineTrans::SetCutPoint-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SetCutPoint` -Methode legt die Zeit fest, zu der der Übergang von einer Quelle zur nächsten schneidet, wenn der Übergang als Schnitt gerendert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetCutPoint(
   REFERENCE_TIME TLTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TLTime* 
</dt> <dd>

Schnittpunkt relativ zum Beginn des Übergangs in Einheiten von 100 Nanosekunden. Wenn der Wert außerhalb der Grenzen des Übergangs liegt, wird er auf die nächste gültige Zeit abgeschnitten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Standardmäßig ist der Schnittpunkt die Mitte des Übergangs. Bei einem Übergang, der sich über eine Sekunde erstreckt, beträgt der Standardmäßige Schnittpunkt beispielsweise 0,5 Sekunden in den Übergang.

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

 

 




