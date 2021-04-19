---
description: Die Run-Methode führt den Filter aus.
ms.assetid: 83251137-83f8-45a3-b3f2-d7b45f43f7f8
title: Cbaserderderer. Run-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc298cbe3f2a0b8063caaa3bdb69fd0d8a88f556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362151"
---
# <a name="cbaserendererrun-method"></a>Cbaserderderer. Run-Methode

Die- `Run` Methode führt den Filter aus.

## <a name="syntax"></a>Syntax


```C++
HRESULT Run();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbasefilter:: Run**](cbasefilter-run.md) -Methode. Es führt die folgenden Aktionen aus:

-   Ruft die **cbasefilter:: Run** -Methode auf.
-   Führt einen Commit für die Zuweisung aus. (Weitere Informationen finden Sie unter [**imemzuordcator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)
-   Wenn der vorherige Zustand beendet wurde, gibt der Filter jedes enthaltene Beispiel frei. (Das Beispiel ist nicht mehr gültig.)
-   Ruft die [**cbaserenderer:: startstreaming**](cbaserenderer-startstreaming.md) -Methode auf und gibt das Ergebnis zurück. Wenn eine Stichprobe aussteht, plant die **startstreaming** -Methode Sie für das Rendering.

Wenn der Filter nicht verbunden ist, sendet er sofort ein [**EC \_ Complete**](ec-complete.md) -Ereignis.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




