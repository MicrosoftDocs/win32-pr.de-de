---
description: Die GetTimelineType-Methode ruft den Typ des Objekts ab.
ms.assetid: db46457f-25d0-4421-af73-426d65b720d3
title: IAMTimelineObj::GetTimelineType-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetTimelineType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9f9c69bcd6b14b489fab4caa399e481613bc7cbeeb30245e00ece480b97b31ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155334"
---
# <a name="iamtimelineobjgettimelinetype-method"></a>IAMTimelineObj::GetTimelineType-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `GetTimelineType` -Methode ruft den Typ des Objekts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTimelineType(
   TIMELINE_MAJOR_TYPE *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* 
</dt> <dd>

Empfängt einen Member des [**aufzählten TIMELINE \_ MAJOR \_ TYPE-Typs,**](timeline-major-type.md) der den Objekttyp angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK-Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




