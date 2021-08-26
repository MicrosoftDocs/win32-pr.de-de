---
description: Die SetLocked-Methode legt den Bearbeitungsstatus des Objekts auf gesperrt oder entsperrt fest.
ms.assetid: 801b8bf0-5c7a-4122-9038-6b0d8bdc5da3
title: IAMTimelineObj::SetLocked-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 87298b4e1fe9bc821c72d46d09d55e898b453292940029b7189a92e455b4c206
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052480"
---
# <a name="iamtimelineobjsetlocked-method"></a>IAMTimelineObj::SetLocked-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SetLocked` -Methode legt den Bearbeitungsstatus des Objekts auf gesperrt oder entsperrt fest.

Ein gesperrter Zustand gibt an, dass das Objekt nicht bearbeitet werden soll. Ein entsperrter Zustand gibt an, dass das Objekt bearbeitet werden kann. Die Zeitachse erzwingt die Sperre nicht. Die gesperrte Einstellung ist nur zur Vereinfachung der Anwendung vorhanden.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetLocked(
   BOOL newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* 
</dt> <dd>

Boolescher Wert, der den Bearbeitungszustand des Objekts angibt. **True** gibt an, dass das Objekt gesperrt ist und nicht bearbeitet werden soll. False gibt an, dass das Objekt entsperrt und bearbeitet werden kann.

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

[**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




