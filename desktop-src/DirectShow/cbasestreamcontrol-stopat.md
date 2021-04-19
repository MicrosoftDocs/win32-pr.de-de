---
description: 'Die STOPAT-Methode informiert den PIN, wann die Übermittlung von Daten beendet werden soll. Diese Methode implementiert die iamstreamcontrol:: STOPAT-Methode.'
ms.assetid: cc9f0fdc-253b-4feb-95ce-56ebc575a49b
title: Cbasestreamcontrol. STOPAT-Methode ("strinmctl. h")
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StopAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e6b794f5f05721f403d943252c2aabd48614519
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373564"
---
# <a name="cbasestreamcontrolstopat-method"></a>Cbasestreamcontrol. STOPAT-Methode

Die- `StopAt` Methode informiert den PIN, wann die Übermittlung von Daten beendet werden soll. Diese Methode implementiert die [**iamstreamcontrol:: STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT StopAt(
   const REFERENCE_TIME *ptStop = NULL,
         BOOL           bSendExtra = FALSE,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptstopps* 
</dt> <dd>

Ein Zeiger auf einen [**Verweis \_ Zeitwert**](reference-time.md) , der angibt, wann die PIN die Übermittlung von Daten beenden soll.

</dd> <dt>

*bsendextra* 
</dt> <dd>

Gibt einen booleschen Wert an, der angibt, ob nach der geplanten Endzeit ein zusätzliches Beispiel gesendet werden soll. **True** gibt an, dass die PIN ein zusätzliches Beispiel sendet.

</dd> <dt>

*dwCookie* 
</dt> <dd>

Gibt einen Wert an, der zusammen mit der Start Benachrichtigung gesendet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Strauch. h" (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasestreamcontrol-Klasse**](cbasestreamcontrol.md)
</dt> </dl>

 

 




