---
description: 'Die GetInfo-Methode ruft Informationen über die aktuellen streamsteuerungseinstellungen ab, einschließlich der Start-und Endzeiten. Diese Methode implementiert die iamstreamcontrol:: GetInfo-Methode.'
ms.assetid: 3bc9bb32-eb33-4752-b22c-9033c28b41f7
title: Cbasestreamcontrol. GetInfo-Methode ("strinmctl. h")
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
ms.openlocfilehash: ab0ba31fa5692a6bc92372860ec1a28ab776206f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369214"
---
# <a name="cbasestreamcontrolgetinfo-method"></a>Cbasestreamcontrol. GetInfo-Methode

Die- `GetInfo` Methode ruft Informationen zu den aktuellen streamsteuerungseinstellungen ab, einschließlich der Start-und Endzeiten. Diese Methode implementiert die [**iamstreamcontrol:: GetInfo**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-getinfo) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetInfo(
   AM_STREAM_INFO *pInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinfo* 
</dt> <dd>

Ein Zeiger auf eine [**am- \_ Stream- \_ Informations**](/windows/desktop/api/strmif/ns-strmif-am_stream_info) Struktur, die vom Aufrufer zugeordnet wird und die die aktuellen streamsteuerungseinstellungen empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den S \_ OK-oder E- \_ Zeiger zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Strauch. h" (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasestreamcontrol-Klasse**](cbasestreamcontrol.md)
</dt> </dl>

 

 




