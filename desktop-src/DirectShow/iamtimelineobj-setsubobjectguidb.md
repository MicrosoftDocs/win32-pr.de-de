---
description: Die SetSubObjectGUIDB-Methode gibt die GUID des Diesem Objekt zugeordneten Unterobjekts an. Diese Methode entspricht IAMTimelineObj::SetSubObjectGUID, nimmt jedoch einen BSTR-Wert an.
ms.assetid: b2523b17-1df3-4be5-8bbb-6b67815f9349
title: IAMTimelineObj::SetSubObjectGUIDB-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a9bb2f88e1312a3a8640147d9ced7ebc1c2157a0633aeed969f36c43236b6052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154966"
---
# <a name="iamtimelineobjsetsubobjectguidb-method"></a>IAMTimelineObj::SetSubObjectGUIDB-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `SetSubObjectGUIDB` -Methode gibt die GUID des Unterobjekts an, das diesem -Objekt zugeordnet ist. Diese Methode entspricht [**IAMTimelineObj::SetSubObjectGUID,**](iamtimelineobj-setsubobjectguid.md) nimmt jedoch einen **BSTR-Wert** an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSubObjectGUIDB(
   BSTR newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* 
</dt> <dd>

**BSTR,** das die GUID des Unterobjekts darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn erfolgreich, oder ein **HRESULT-Wert,** der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

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

 

 




