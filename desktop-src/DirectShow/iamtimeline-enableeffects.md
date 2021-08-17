---
description: Die EnableEffects-Methode aktiviert oder deaktiviert alle Auswirkungen auf der Zeitachse. Wenn Effekte deaktiviert sind, verbleiben sie auf der Zeitachse, werden aber nicht gerendert.
ms.assetid: 5344cd49-6515-4211-9637-ca58219b3b56
title: IAMTimeline::EnableEffects-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableEffects
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8a6cce5d06b65bb6a7b3b6063e6cf6b9190e268ba7ee5f5abadf4343be2cf64c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401111"
---
# <a name="iamtimelineenableeffects-method"></a>IAMTimeline::EnableEffects-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `EnableEffects` -Methode aktiviert oder deaktiviert alle Auswirkungen auf der Zeitachse. Wenn Effekte deaktiviert sind, verbleiben sie auf der Zeitachse, werden aber nicht gerendert.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnableEffects(
   BOOL fEnabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fEnabled* 
</dt> <dd>

Boolescher Wert, der angibt, ob Effekte aktiviert oder deaktiviert werden. True **gibt an,** dass Effekte aktiviert sind. False **gibt an,** dass Effekte deaktiviert sind.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMTimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




