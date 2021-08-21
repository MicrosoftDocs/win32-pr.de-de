---
description: Die Remove-Methode entfernt dieses Objekt aus der Zeitachse (einschließlich Unterobjekten, aber nicht untergeordneten Objekten) zur Wiederherstellung an anderer Stelle.
ms.assetid: 118a08a5-abba-47df-8aeb-42ce8c8ed2ba
title: IAMTimelineObj::Remove-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.Remove
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 356f7239cbdbe3972f11fcc95dd9bf44dc1b06d086a8e44c9131c0061f3ec211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155263"
---
# <a name="iamtimelineobjremove-method"></a>IAMTimelineObj::Remove-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `Remove` -Methode entfernt dieses Objekt aus der Zeitachse (einschließlich Unterobjekten, aber nicht von untergeordneten Objekten), um es an anderer Stelle wiederzuerlangen.

## <a name="syntax"></a>Syntax


```C++
HRESULT Remove();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode nur auf, wenn die Anwendung das Objekt sofort wieder in die Zeitachse einfügt. Es ist ein ungültiger Vorgang, diese Methode aufzurufen, ohne dann das Objekt erneut zu setzen. Um ein Objekt dauerhaft zu entfernen, rufen [**Sie IAMTimelineObj::RemoveAll auf.**](iamtimelineobj-removeall.md)

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

 

 




