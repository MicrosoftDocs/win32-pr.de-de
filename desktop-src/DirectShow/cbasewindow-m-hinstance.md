---
description: Handle für die Modulinstanz.
ms.assetid: ad889ebe-2bd8-4456-9517-9e2909697a02
title: CBaseWindow::m_hInstance-Member (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hInstance
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ddf1da2d7f947bbaed9972a40a20497a81f84ebda68dba31cd5518b64f6e8434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016528"
---
# <a name="cbasewindowm_hinstance-member"></a>CBaseWindow::m \_ hInstance-Member

Handle für die Modulinstanz.

## <a name="syntax"></a>Syntax


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a>Hinweise

Die DLL-Einstiegspunktfunktion legt eine globale Variable mit einem Handle für die Modulinstanz fest. Die **CBaseWindow-Klasse** speichert dieses Handle in ihrer Konstruktormethode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseWindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




