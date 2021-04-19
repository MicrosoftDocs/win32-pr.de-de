---
description: Die preparerender-Methode wird aufgerufen, bevor der Filter ein Beispiel rendert.
ms.assetid: 0b137da9-eac0-469f-b457-719a36569c82
title: Cbaserderderer. preparerender-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee5739a839222900458ae334de6f97fb6d18876b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106374013"
---
# <a name="cbaserendererpreparerender-method"></a>Cbaserderderer. preparerender-Methode

Die- `PrepareRender` Methode wird aufgerufen, bevor der Filter eine Stichprobe rendert.

## <a name="syntax"></a>Syntax


```C++
virtual void PrepareRender();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der Filter ruft diese Methode auf, bevor die [**cbaserdenderer:: onreceivefirstsample**](cbaserenderer-onreceivefirstsample.md) -Methode oder die [**cbaserdenderer:: Rendering**](cbaserenderer-render.md) -Methode aufgerufen wird. `PrepareRender` führt in der Basisklasse keine Aktionen aus. Die abgeleitete Klasse kann Sie außer Kraft setzen, um vor dem Rendering erforderliche Aktionen auszuführen. Ein Videorenderer kann diese Methode z. b. überschreiben, um die Palette zu erkennen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




