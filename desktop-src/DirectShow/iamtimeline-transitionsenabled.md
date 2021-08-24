---
description: Die TransitionsEnabled-Methode bestimmt, ob Übergänge aktiviert sind.
ms.assetid: c961d8d7-4509-444b-a49f-6ab79fc31f7e
title: IAMTimeline::TransitionsEnabled-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.TransitionsEnabled
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 36d22fa1c19c6a90faa033e6a8ccf100b5042cd2aeeabf9b012ee42f13cd57da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316470"
---
# <a name="iamtimelinetransitionsenabled-method"></a>IAMTimeline::TransitionsEnabled-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die **TransitionsEnabled-Methode** bestimmt, ob Übergänge aktiviert sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT TransitionsEnabled(
   BOOL *pfEnabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfEnabled* 
</dt> <dd>

Empfängt einen booleschen Wert. True **gibt an,** dass Übergänge aktiviert sind. Andernfalls sind Übergänge deaktiviert.

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

[**IAMTimeline::EnableTransitions**](iamtimeline-enabletransitions.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




