---
description: Die GetMuted-Methode ruft den stummgeschalteten Zustand des Objekts ab.
ms.assetid: e901af1f-1137-4708-a98b-c9f83edc5ab9
title: IAMTimelineObj::GetMuted-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f30c0292316f1c876216532b9a2a3193317370d0103ddbc0ab94c6801fae1504
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051650"
---
# <a name="iamtimelineobjgetmuted-method"></a>IAMTimelineObj::GetMuted-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetMuted` -Methode ruft den stummgeschalteten Zustand des Objekts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetMuted(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* 
</dt> <dd>

Empfängt einen Wert, der den stummgeschalteten Zustand angibt. Wenn der Wert **TRUE** ist, werden das Objekt und seine untergeordneten Elemente stummgeschaltet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn das übergeordnete Element eines Objekts stummgeschaltet ist, wird das Objekt unabhängig von seinem stummgeschalteten Zustand stummgeschaltet. Wenn das übergeordnete Element nicht mehr stummgeschaltet ist, wird der vorherige stummgeschaltete Zustand des Objekts wiederhergestellt.

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

 

 




