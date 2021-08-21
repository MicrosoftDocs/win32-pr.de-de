---
description: Die GetCutPoint-Methode ruft den Schnittpunkt ab.
ms.assetid: f54ef17e-3407-4164-911d-3dc7fad656ed
title: IAMTimelineTrans::GetCutPoint-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0582446a3f88b3692b50ca97d033a85d1dfca475051e3538c39d41003e788ebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154794"
---
# <a name="iamtimelinetransgetcutpoint-method"></a>IAMTimelineTrans::GetCutPoint-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetCutPoint` -Methode ruft den Schnittpunkt ab. Wenn Sie einen Übergang als Schnitt rendern, ist der Schnittpunkt der Zeitpunkt, zu dem der Übergang von einer Quelle zur nächsten schneidet. Standardmäßig ist dieser Wert die Mitte des Übergangs. Bei einem Übergang, der sich über eine Sekunde erstreckt, beträgt der Standardmäßige Schnittpunkt beispielsweise 0,5 Sekunden in den Übergang.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCutPoint(
   REFERENCE_TIME *pTLTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTLTime* 
</dt> <dd>

Empfängt den Schnittpunkt relativ zur Startzeit des Übergangs in Einheiten von 100 Nanosekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück:



| Rückgabecode                                                                               | Beschreibung                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Der Schnittpunkt wurde nicht festgelegt. Der zurückgegebene Wert ist der Standardwert.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Der Schnittpunkt wurde auf einen anderen Wert als den Standardwert festgelegt.<br/>            |
| <dl> <dt>**E \_ POINTER**</dt> </dl> | **NULL-Zeigerargument.**<br/>                                          |



 

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

[**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md)
</dt> <dt>

[**IAMTimelineTrans::GetCutsOnly**](iamtimelinetrans-getcutsonly.md)
</dt> <dt>

[**IAMTimeline::TransitionsEnabled**](iamtimeline-transitionsenabled.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




