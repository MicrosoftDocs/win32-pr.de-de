---
description: Die Pause-Methode hält den Filter an.
ms.assetid: 9dfd23d1-bf07-424b-9952-13719358d0a5
title: Cbaserderderer. Pause-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e0b422882c07808f560f5256f67d01054d097726
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362152"
---
# <a name="cbaserendererpause-method"></a>Cbaserderderer. Pause-Methode

Die `Pause` Methode hält den Filter an.

## <a name="syntax"></a>Syntax


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                             | Beschreibung                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Der Übergang ist fertiggestellt.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl> | Der Übergang ist nicht durchgeführt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbasefilter::P ause**](cbasefilter-pause.md) -Methode. Sie führt die folgenden Schritte aus:

-   Ruft die **cbasefilter::P ause** -Methode auf.
-   Führt einen Commit für die Zuweisung aus. (Weitere Informationen finden Sie unter [**imemzuordcator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)
-   Wenn der vorherige Zustand beendet wurde, gibt der Filter jedes enthaltene Beispiel frei. (Das Beispiel ist nicht mehr gültig.)
-   Ruft die [**cbaserenderer:: completestatechange**](cbaserenderer-completestatechange.md) -Methode auf und gibt den Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




