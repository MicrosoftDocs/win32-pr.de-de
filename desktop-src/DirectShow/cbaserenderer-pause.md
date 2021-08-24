---
description: Die Pause-Methode hält den Filter an.
ms.assetid: 9dfd23d1-bf07-424b-9952-13719358d0a5
title: CBaseRenderer.Pause-Methode (Renbase.h)
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
ms.openlocfilehash: 9769a1243fdbd69037e275fc083a9b1b0766f7f404190b2e68920f238e2bf140
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586080"
---
# <a name="cbaserendererpause-method"></a>CBaseRenderer.Pause-Methode

Die `Pause` -Methode hält den Filter an.

## <a name="syntax"></a>Syntax


```C++
HRESULT Pause();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die werte in der folgenden Tabelle.



| Rückgabecode                                                                             | Beschreibung                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | Der Übergang ist abgeschlossen.<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Der Übergang ist nicht abgeschlossen.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBaseFilter::P ause-Methode.**](cbasefilter-pause.md) Sie führt die folgenden Schritte aus:

-   Ruft die **CBaseFilter::P ause-Methode** auf.
-   Commits für die Zuweisung. (Siehe [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)
-   Wenn der vorherige Zustand beendet wurde, gibt der Filter alle Stichproben frei, die er hält. (Das Beispiel ist nicht mehr gültig.)
-   Ruft die [**CBaseRenderer::CompleteStateChange-Methode**](cbaserenderer-completestatechange.md) auf und gibt den Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




