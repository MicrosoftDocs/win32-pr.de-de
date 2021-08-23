---
description: Die GetSubObject-Methode ruft das Unterobjekt ab, das diesem Objekt zugeordnet ist.
ms.assetid: 478597d6-ae13-4fa9-a928-19893f378f1a
title: IAMTimelineObj::GetSubObject-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ba3bc12e3b123768c88ce7f43955be419a0dfe84b6437701f9609e03a3fa0bdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118155371"
---
# <a name="iamtimelineobjgetsubobject-method"></a>IAMTimelineObj::GetSubObject-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetSubObject` -Methode ruft das diesem -Objekt zugeordnete Unterobjekt ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSubObject(
  [out, retval] IUnknown **pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Empfängt einen Zeiger auf die **IUnknown-Schnittstelle** des Unterobjekts. Wenn das Objekt kein Unterobjekt besitzt, wird der Wert auf **NULL** festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Jedes Zeitachsenobjekt kann einen Zeiger auf ein zugeordnetes Unterobjekt enthalten.

Wenn der in *pVal* zurückgegebene Wert nicht **NULL** ist, weist die **IUnknown-Schnittstelle** einen ausstehenden Verweiszähler auf. Stellen Sie sicher, dass Sie die Schnittstelle freigeben, wenn Sie sie nicht mehr verwenden.

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

 

 




