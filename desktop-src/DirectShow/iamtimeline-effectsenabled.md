---
description: Die EffectsEnabled-Methode bestimmt, ob Effekte aktiviert sind. Wenn Effekte deaktiviert sind, verbleiben sie auf der Zeitachse, werden aber nicht gerendert.
ms.assetid: fd8bb2aa-9c10-4a85-9e9d-1b342fbce03b
title: IAMTimeline::EffectsEnabled-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EffectsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e63561c62f3cbaf7a3a257179167e657ee4d10c6206b6d74062039362b272aef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905280"
---
# <a name="iamtimelineeffectsenabled-method"></a>IAMTimeline::EffectsEnabled-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `EffectsEnabled` -Methode bestimmt, ob Effekte aktiviert sind. Wenn Effekte deaktiviert sind, verbleiben sie auf der Zeitachse, werden aber nicht gerendert.

## <a name="syntax"></a>Syntax


```C++
HRESULT EffectsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfEnabled* 
</dt> <dd>

Empfängt einen booleschen Wert, der angibt, ob Effekte aktiviert sind. True **gibt an,** dass Effekte aktiviert sind. False **gibt an,** dass Effekte deaktiviert sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

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

[**IAMTimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




