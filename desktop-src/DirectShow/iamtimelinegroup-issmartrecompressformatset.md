---
description: Die IsSmartRecompressFormatSet-Methode bestimmt, ob ein intelligentes Neukomprimierungsformat für die Gruppe festgelegt wurde.
ms.assetid: d2b7ecc7-2348-402d-8d96-e0922e06a685
title: IAMTimelineGroup::IsSmartRecompressFormatSet-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.IsSmartRecompressFormatSet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e37dfd551f92e0be10ae80f123ce0df0011aa09d2b74313c6a72b2706d7f8a16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107830"
---
# <a name="iamtimelinegroupissmartrecompressformatset-method"></a>IAMTimelineGroup::IsSmartRecompressFormatSet-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `IsSmartRecompressFormatSet` -Methode bestimmt, ob ein intelligentes Neukomprimierungsformat für die Gruppe festgelegt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsSmartRecompressFormatSet(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* 
</dt> <dd>

Empfängt einen booleschen Wert, der angibt, ob ein Komprimierungsformat festgelegt wurde. True gibt an, dass ein Komprimierungsformat festgelegt wurde.

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

[**IAMTimelineGroup-Schnittstelle**](iamtimelinegroup.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




