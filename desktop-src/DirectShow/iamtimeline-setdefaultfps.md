---
description: Die SetDefaultFPS-Methode legt die Standardausgabeframerate in Frames pro Sekunde fest. Gruppen verwenden diesen Wert als Standardbildrate. Rufen Sie zum Festlegen der Framerate einer Gruppe die IAMTimelineGroup::SetOutputFPS-Methode für die Gruppe auf.
ms.assetid: a164f4b9-fbed-45ea-9156-cc64f0b21423
title: IAMTimeline::SetDefaultFPS-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d98b4ea7a69f527f0a79ddbe559d3602afecd06e4728da23ef3627ed7a313a15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052810"
---
# <a name="iamtimelinesetdefaultfps-method"></a>IAMTimeline::SetDefaultFPS-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `SetDefaultFPS` -Methode legt die Standardausgabebildrate in Frames pro Sekunde fest. Gruppen verwenden diesen Wert als Standardbildrate. Rufen Sie zum Festlegen der Framerate einer Gruppe die [**IAMTimelineGroup::SetOutputFPS-Methode**](iamtimelinegroup-setoutputfps.md) für die Gruppe auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FPS* 
</dt> <dd>

Standardbildrate in Frames pro Sekunde.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMTimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




