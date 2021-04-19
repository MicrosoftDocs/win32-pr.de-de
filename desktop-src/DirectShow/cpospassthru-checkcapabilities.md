---
description: 'Die Checkfunktionen-Methode fragt ab, ob ein Stream Suchfunktionen angegeben hat. Diese Methode implementiert die imediaseeking:: Checkfunktionen-Methode.'
ms.assetid: 48096af6-bbce-4a1f-be9a-fd150ed4536e
title: Cpospassthru. Checkfunktionen-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 33f7a685684667d2f5d465b14070a595c70b178c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355946"
---
# <a name="cpospassthrucheckcapabilities-method"></a>Cpospassthru. Checkfunktionen-Methode

Die- `CheckCapabilities` Methode fragt ab, ob ein Stream Suchfunktionen angegeben hat. Diese Methode implementiert die [**imediaseeking:: Checkfunktionen**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfunktionen* 
</dt> <dd>

Zeiger auf eine bitweise Kombination von einem oder mehreren Suchfunktionen, die [**\_ \_ Such \_ Funktionen**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) suchen. Wenn die-Methode zurückgibt, gibt der Wert an, welches dieser Attribute verfügbar ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT** -Wert aus der verbundenen PIN zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpospassthru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




