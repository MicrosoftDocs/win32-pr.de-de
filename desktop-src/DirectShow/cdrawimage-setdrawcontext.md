---
description: Die SetDrawContext-Methode legt die Gerätekontexte fest, die zum Zeichnen verwendet werden.
ms.assetid: dd752970-99b3-42bb-95a5-8103cab276da
title: CDrawImage.SetDrawContext-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetDrawContext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 58a10c9f1a485058ed460f4cd30cd4d3894b471415f131d7d4aa59ee757b87d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055970"
---
# <a name="cdrawimagesetdrawcontext-method"></a>CDrawImage.SetDrawContext-Methode

Die `SetDrawContext` -Methode legt die zum Zeichnen verwendeten Gerätekontexte fest.

## <a name="syntax"></a>Syntax


```C++
void SetDrawContext();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode ruft die Fenster- und Speichergerätekontexte aus dem besitzenden [**CBaseWindow-Objekt**](cbasewindow.md) ab. Rufen Sie diese Methode auf, nachdem das Fenster initialisiert wurde, aber bevor Sie mit dem Zeichnen beginnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDrawImage-Klasse**](cdrawimage.md)
</dt> </dl>

 

 




