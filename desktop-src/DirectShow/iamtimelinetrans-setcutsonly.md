---
description: Die SetCutsOnly-Methode gibt an, ob der Übergang als Schnitt gerendert wird. Wenn dies der Fall ist, erfolgt der Übergang sofort am Schnittpunkt. Wenn das Rendern eines Übergangs sehr lange dauert, sollten Sie eine Vorschau als Vorschauversion für die Umstellung auf die Geschwindigkeit anzeigen.
ms.assetid: 9ccff624-e37b-422e-9cb2-c472e6c8b2bb
title: IAMTimelineTrans::SetCutsOnly-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3b008e0aef31548dcba71f3b2a2940009c0cd0c71786bd9bd733c206c1d68ee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154726"
---
# <a name="iamtimelinetranssetcutsonly-method"></a>IAMTimelineTrans::SetCutsOnly-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `SetCutsOnly` -Methode gibt an, ob der Übergang als Schnitt gerendert wird. Wenn dies der Fall ist, erfolgt der Übergang sofort am Schnittpunkt. Wenn das Rendern eines Übergangs sehr lange dauert, sollten Sie eine Vorschau als Vorschauversion für die Umstellung auf die Geschwindigkeit anzeigen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetCutsOnly(
   BOOL Val
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Val* 
</dt> <dd>

Gibt an, ob der Übergang als Schnitt gerendert werden soll. True **gibt an,** dass der Übergang als sofortiger Schnitt gerendert wird. False **gibt an,** dass der Übergang über die normale Dauer gerendert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Das Rendern eines Übergangs als Schnitt ist nicht kompatibel mit dem Austauschen der Eingaben. (Siehe [**IAMTimelineTrans::SetSwapInputs**](iamtimelinetrans-setswapinputs.md).) Wenn Sie mit `SetCutsOnly` dem Wert **TRUE** aufrufen, wird die Einstellung **SetSwapInputs vorübergehend** überschrieben. Die Einstellung "Nur Kürzungen" ist jedoch für die Vorschau vorgesehen, daher wirkt sich diese Einschränkung nicht auf die Dateiausgabe aus. Denken Sie daran, vor dem Schreiben der Datei mit dem Wert `SetCutsOnly` **FALSE** auf aufrufen.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK-Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

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

 

 




