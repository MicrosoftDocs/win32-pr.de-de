---
description: Handle für die Modul Instanz.
ms.assetid: ad889ebe-2bd8-4456-9517-9e2909697a02
title: 'Cbasewindow:: m_hInstance Member (winutil. h)'
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
ms.openlocfilehash: 6482aac80c1298ea403019f43ddc4effdc30b00a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373663"
---
# <a name="cbasewindowm_hinstance-member"></a>Cbasewindow:: m \_ HINSTANCE-Member

Handle für die Modul Instanz.

## <a name="syntax"></a>Syntax


```C++
HINSTANCE m_hInstance;
```



## <a name="remarks"></a>Bemerkungen

Die Funktion "DLL-Einstiegspunkt" legt eine globale Variable mit einem Handle für die Modul Instanz fest. Die **cbasewindow** -Klasse speichert dieses Handle in seiner Konstruktormethode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasewindow-Klasse**](cbasewindow.md)
</dt> </dl>

 

 




