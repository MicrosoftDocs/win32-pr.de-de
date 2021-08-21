---
description: Die GetInfo-Methode ruft Informationen zu den aktuellen Streamsteuerelementeinstellungen ab, einschließlich der Start- und Beendigungszeiten. Diese Methode implementiert die IAMStreamControl::GetInfo-Methode.
ms.assetid: 3bc9bb32-eb33-4752-b22c-9033c28b41f7
title: CBaseStreamControl.GetInfo-Methode (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.GetInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96bc59b6dc55d73aa16b08f53f831428ae2d2fb7b181d3bb255b61a323b236a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157217"
---
# <a name="cbasestreamcontrolgetinfo-method"></a>CBaseStreamControl.GetInfo-Methode

Die `GetInfo` -Methode ruft Informationen zu den aktuellen Streamsteuerelementeinstellungen ab, einschließlich der Start- und Beendigungszeiten. Diese Methode implementiert die [**IAMStreamControl::GetInfo-Methode.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo)

## <a name="syntax"></a>Syntax


```C++
HRESULT GetInfo(
   AM_STREAM_INFO *pInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Pinfo* 
</dt> <dd>

Zeiger auf eine VOM Aufrufer zugeordnete [**AM \_ STREAM \_ INFO-Struktur,**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) die die aktuellen Streamsteuerelementeinstellungen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder E POINTER \_ zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Strmctl.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseStreamControl-Klasse**](cbasestreamcontrol.md)
</dt> </dl>

 

 




