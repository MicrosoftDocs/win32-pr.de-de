---
title: Devicepair-Server Eigenschaft (asptlb. h)
description: Ruft den Server für das aktive Basic-Geräte Paar ab.
ms.assetid: 25FD523F-36C7-4165-BBB2-6A3410D896EF
keywords:
- Server Eigenschaft Medien Streaming-API
- Server Eigenschaft Medien Streaming-API, devicepair-Schnittstelle
- Devicepair Interface Medien Streaming-API, Server Eigenschaft
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
ms.openlocfilehash: eec2c28e8118f6cf11e89c7ab4a5ba04abd8b8f5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371960"
---
# <a name="devicepairserver-property"></a>Devicepair:: Server-Eigenschaft

Ruft den Server für das aktive Basic-Geräte Paar ab.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Server(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a>Eigenschaftswert

Empfängt ein [**activebasicdevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) -Objekt, das das Server Gerät darstellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Asptlb. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Devicepair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))
</dt> </dl>

 

