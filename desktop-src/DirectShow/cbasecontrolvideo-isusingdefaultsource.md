---
description: Die IsUsingDefaultSource-Methode bestimmt, ob der Renderer das Standardquellfenster verwendet.
ms.assetid: f68d47e7-6602-4321-8e9e-373d354077a1
title: CBaseControlVideo.IsUsingDefaultSource-Methode (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsUsingDefaultSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dce06ffa85b3736eca17f1ecb8303a41afb142fcc8b0d369e1f264a0cf47b2d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955209"
---
# <a name="cbasecontrolvideoisusingdefaultsource-method"></a>CBaseControlVideo.IsUsingDefaultSource-Methode

Die `IsUsingDefaultSource` -Methode bestimmt, ob der Renderer das Standardquellfenster verwendet.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT IsUsingDefaultSource() = 0;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn der Renderer die Standardquelle verwendet, andernfalls S \_ FALSE.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




