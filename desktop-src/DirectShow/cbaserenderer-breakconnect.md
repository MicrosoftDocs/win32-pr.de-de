---
description: Die breakconnect-Methode gibt die Eingabe-PIN von einer Verbindung frei.
ms.assetid: e295cec1-8c8f-471c-8832-075ac7708cb1
title: Cbaserderderer. breakconnect-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98c1e01c15740616541706ca4d9da3ab5e66538c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366746"
---
# <a name="cbaserendererbreakconnect-method"></a>Cbaserderderer. breakconnect-Methode

Die- `BreakConnect` Methode gibt die Eingabe-PIN von einer Verbindung frei.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.



| Rückgabecode                                                                                         | Beschreibung                            |
|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>             | Die PIN war nicht verbunden.<br/>  |
| <dl> <dt>**S \_ OK**</dt> </dl>                | Erfolg.<br/>                    |
| <dl> <dt>**VFW \_ E \_ nicht \_ angehalten**</dt> </dl> | Der Filter ist noch aktiv.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Die Eingabe-PIN des Filters ruft diese Methode in der eigenen `BreakConnect` Methode auf. (Weitere Informationen finden Sie unter [**cbasepin:: breakconnect**](cbasepin-breakconnect.md).) Der Filter führt eine interne Buchhaltung aus, z. b. das Flag für das Ende des Streams zurücksetzen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




