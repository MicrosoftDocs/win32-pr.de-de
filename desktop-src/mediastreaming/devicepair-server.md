---
title: DevicePair-Servereigenschaft (Asptlb.h)
description: Ruft den Server für das aktive Basisgerätepaar ab.
ms.assetid: 25FD523F-36C7-4165-BBB2-6A3410D896EF
keywords:
- Servereigenschaft Media Streaming-API
- Servereigenschaft Media Streaming-API, DevicePair-Schnittstelle
- DevicePair-Schnittstelle Medienstreaming-API, Servereigenschaft
topic_type:
- apiref
api_name:
- DevicePair.Server
- DevicePair.get_Server
api_location:
- asptlb.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0939a27d96de8f2c8ff53ffd7b0bd766292b873450fb138d0877e916c691f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100724"
---
# <a name="devicepairserver-property"></a>DevicePair::Server-Eigenschaft

Ruft den Server für das aktive Basisgerätepaar ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Server(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a>Eigenschaftswert

Empfängt ein [**ActiveBasicDevice-Objekt,**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) das das Servergerät darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Asptlb.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))
</dt> </dl>

 

