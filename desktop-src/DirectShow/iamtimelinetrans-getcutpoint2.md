---
description: Die GetCutPoint2-Methode ruft den Schnittpunkt ab. Diese Methode entspricht IAMTimelineTrans::GetCutPoint, verwendet jedoch einen REFTIME-Wert.
ms.assetid: bf2b7cac-6740-44d8-a889-8c745a23db19
title: IAMTimelineTrans::GetCutPoint2-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 291aff15260d5d693f3e6b0281d693a7351132fc017358f6f9ee21020dfd4f26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952759"
---
# <a name="iamtimelinetransgetcutpoint2-method"></a>IAMTimelineTrans::GetCutPoint2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetCutPoint2` -Methode ruft den Schnittpunkt ab. Diese Methode entspricht [**IAMTimelineTrans::GetCutPoint,**](iamtimelinetrans-getcutpoint.md)verwendet jedoch einen [**REFTIME-Wert.**](reftime.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCutPoint2(
   REFTIME *pTLTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTLTime* 
</dt> <dd>

Empfängt den Schnittpunkt relativ zur Startzeit des Übergangs in Sekunden.

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

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




