---
description: Sperre zum Schutz der Erstellung von Objekten innerhalb des Filters.
ms.assetid: ad1d2584-0d9e-42a8-83ea-0c1907ddcf33
title: 'Cbaserenderer:: m_ObjectCreationLock Member (renbase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ObjectCreationLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e344b20b4924ac26ebe6253f5388136b350abefe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356056"
---
# <a name="cbaserendererm_objectcreationlock-member"></a>Cbaserenderer:: m \_ objectkreationlock-Member

Sperre zum Schutz der Erstellung von Objekten innerhalb des Filters. Der Filter enthält diese Sperre, wenn er die Eingabe-PIN ([**cbaserenderer:: m \_ pinputpin**](cbaserenderer-m-pinputpin.md)) oder das [**crendererpospassthru**](crendererpospassthru.md) -Objekt ([**cbaserenderer:: m \_ pposition**](cbaserenderer-m-pposition.md)) erstellt. Diese Sperre verhindert, dass mehrere Threads gleichzeitig versuchen, eines dieser Objekte zu erstellen.

## <a name="syntax"></a>Syntax


```C++
CCritSec m_ObjectCreationLock;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




