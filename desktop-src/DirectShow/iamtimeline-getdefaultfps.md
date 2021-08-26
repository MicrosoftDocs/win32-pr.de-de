---
description: Die GetDefaultFPS-Methode ruft die Standardausgabebildrate in Frames pro Sekunde (FPS) ab. Gruppen verwenden diesen Wert als Standardbildfrequenz. Um die Bildfrequenz einer Gruppe festzulegen, rufen Sie die IAMTimelineGroup::SetOutputFPS-Methode für die Gruppe auf.
ms.assetid: 91c83512-4295-440e-b3b2-09fe3629f827
title: IAMTimeline::GetDefaultFPS-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 38f12abe47829544453d0aed9b8f08bffd2b5864f78fc35c873622d960387931
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107850"
---
# <a name="iamtimelinegetdefaultfps-method"></a>IAMTimeline::GetDefaultFPS-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetDefaultFPS` -Methode ruft die Standardausgabebildrate in Frames pro Sekunde (FPS) ab. Gruppen verwenden diesen Wert als Standardbildfrequenz. Um die Bildfrequenz einer Gruppe festzulegen, rufen Sie die [**IAMTimelineGroup::SetOutputFPS-Methode**](iamtimelinegroup-setoutputfps.md) für die Gruppe auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pfps* 
</dt> <dd>

Empfängt die Standardbildfrequenz in Frames pro Sekunde.

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

[**IAMTimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




