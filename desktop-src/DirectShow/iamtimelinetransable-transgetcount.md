---
description: Die TransGetCount-Methode ruft die Anzahl der Übergänge für dieses Objekt ab.
ms.assetid: f7fb4a99-c841-4680-b7f1-e4d887f12707
title: IAMTimelineTransable::TransGetCount-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransGetCount
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e69724854e69b4139811b5afe2f3b516f592c17594650f585e576dea0f6c9894
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399187"
---
# <a name="iamtimelinetransabletransgetcount-method"></a>IAMTimelineTransable::TransGetCount-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `TransGetCount` -Methode ruft die Anzahl der Übergänge für dieses Objekt ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT TransGetCount(
   long *pCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCount* 
</dt> <dd>

Empfängt die Anzahl der Übergänge.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMTimelineTransable-Schnittstelle**](iamtimelinetransable.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




