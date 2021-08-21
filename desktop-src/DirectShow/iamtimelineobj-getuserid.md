---
description: Die GetUserID-Methode ruft den anwendungsdefinierte Bezeichner des Objekts ab.
ms.assetid: 68a20dfa-990e-47de-ae02-1d3182b7f13f
title: IAMTimelineObj::GetUserID-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d76cb0c7d59fbdbea039fe518127e26b45b98a4d9ea53342ee35df1c201e7fee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155324"
---
# <a name="iamtimelineobjgetuserid-method"></a>IAMTimelineObj::GetUserID-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetUserID` -Methode ruft den anwendungsdefinierte Bezeichner des Objekts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetUserID(
   long *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* 
</dt> <dd>

Empfängt den anwendungsdefinierte Bezeichner.

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

 

 




