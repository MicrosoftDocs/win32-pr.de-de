---
description: Die setoutputfps-Methode legt die nicht komprimierte Ausgabe Frame Rate für diese Gruppe fest.
ms.assetid: 335ea106-d5db-43a1-b771-b027e25164a6
title: 'Iamtimelinegroup:: setoutputfps-Methode (qedit. h)'
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
ms.openlocfilehash: bbec5de572dd2ed2a0e6b3062b208f1084bafd07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373939"
---
# <a name="iamtimelinegroupsetoutputfps-method"></a>Iamtimelinegroup:: setoutputfps-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetOutputFPS` Methode legt die nicht komprimierte Ausgabe Frame Rate für diese Gruppe fest.

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

Ausgabe Frame Rate für diese Gruppe in Frames pro Sekunde. Der Wert kann nicht gleich 0 (null) sein und darf nicht mehr als sieben Ziffern nach der Dezimalstelle enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Die gerenderte Ausgabe dieser Gruppe wird mit der angegebenen Framerate ausgeführt, und alle bearbeitvorgänge im Quellmaterial werden wie durch die Frame Rate definiert auf die nächste Frame Grenze gerundet. Verwenden Sie für eine optimale Leistung die gleiche Framerate für alle Gruppen, Videos und Audiodateien.

Die [**iamtimelinegroup::**](iamtimelinegroup-setsmartrecompressformat.md) -Methode zum Festlegen der Methode überschreibt die Framerate.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iamtimelinegroup-Schnittstelle**](iamtimelinegroup.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




