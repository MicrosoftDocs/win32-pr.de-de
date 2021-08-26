---
description: Die SetOutputFPS-Methode legt die unkomprimierte Ausgabebildrate für diese Gruppe fest.
ms.assetid: 335ea106-d5db-43a1-b771-b027e25164a6
title: IAMTimelineGroup::SetOutputFPS-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 332e9ea33e0ca559800e560409066946247d1cff34b8e6b48fd1fadbdb91e38f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052700"
---
# <a name="iamtimelinegroupsetoutputfps-method"></a>IAMTimelineGroup::SetOutputFPS-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SetOutputFPS` -Methode legt die unkomprimierte Ausgabebildrate für diese Gruppe fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetOutputFPS(
   double FPS
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*FPS* 
</dt> <dd>

Ausgabebildrate für diese Gruppe in Frames pro Sekunde. Der Wert darf nicht gleich 0 (null) sein und darf nach der Dezimalstelle nicht mehr als sieben Ziffern enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Die gerenderte Ausgabe dieser Gruppe wird mit der angegebenen Bildfrequenz ausgeführt, und alle Bearbeitungen am Quellmaterial werden auf die nächste Framegrenze gerundet, wie durch die Bildfrequenz definiert. Um eine optimale Leistung zu erzielen, verwenden Sie die gleiche Bildfrequenz für alle Gruppen, Videos und Audiodaten.

Die [**IAMTimelineGroup::SetSmartRecompressFormat-Methode**](iamtimelinegroup-setsmartrecompressformat.md) überschreibt die Bildfrequenz.

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

 

 




