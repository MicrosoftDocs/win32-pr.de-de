---
description: Die CheckCapabilities-Methode fragt ab, ob ein Stream über angegebene Suchfunktionen verfügt. Diese Methode implementiert die IMediaSeeking::CheckCapabilities-Methode.
ms.assetid: 48096af6-bbce-4a1f-be9a-fd150ed4536e
title: CPosPassThru.CheckCapabilities-Methode (Ctlutil.h)
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
ms.openlocfilehash: f1146e11097dbb2d717bd025d414b4510a219cc5f131e2fa7d56687128ddfd98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108420"
---
# <a name="cpospassthrucheckcapabilities-method"></a>CPosPassThru.CheckCapabilities-Methode

Die `CheckCapabilities` -Methode fragt ab, ob ein Stream über angegebene Suchfunktionen verfügt. Diese Methode implementiert die [**IMediaSeeking::CheckCapabilities-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities)

## <a name="syntax"></a>Syntax


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCapabilities* 
</dt> <dd>

Zeiger auf eine bitweise Kombination aus einem oder mehreren [**AM \_ SEEKING SEEKING \_ \_ CAPABILITIES-Attributen.**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) Wenn die Methode zurückgegeben wird, gibt der Wert an, welche dieser Attribute verfügbar sind.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den **HRESULT-Wert** aus dem verbundenen Pin zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CPosPassThru-Klasse**](cpospassthru.md)
</dt> </dl>

 

 




