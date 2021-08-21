---
description: Die SetUserID-Methode legt einen anwendungsdefinierte Bezeichner für das Objekt fest.
ms.assetid: 102fe29e-dc2c-4377-bce3-ba3c61dcb355
title: IAMTimelineObj::SetUserID-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetUserID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8a4c04f2e401778d65e661e56ce546263764adfda7063308ac9b9a5a85e12bda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078960"
---
# <a name="iamtimelineobjsetuserid-method"></a>IAMTimelineObj::SetUserID-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SetUserID` -Methode legt einen anwendungsdefinierte Bezeichner für das -Objekt fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetUserID(
   long newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* 
</dt> <dd>

Wert, der den Bezeichner angibt. Dieser Bezeichner wird nur von der Anwendung verwendet und kann ein beliebiger Wert sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Requirements (Anforderungen)



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

 

 




