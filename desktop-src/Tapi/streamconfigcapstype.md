---
description: Der "streamconfigcapstype"-Enumerationstyp wird von der TAPI \_ \_ -Struktur "Stream config \_ Caps" als Switch verwendet, um anzugeben, ob ein Audiostreaming oder Video Streaming beteiligt ist.
ms.assetid: c3eec6b2-ce3b-49b1-a0ba-f450d60a1477
title: Streamconfigcapstype-Enumeration (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14649edb7e451cdc7d955f2028a77c247148182b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369304"
---
# <a name="streamconfigcapstype-enumeration"></a>Streamconfigcapstype-Enumeration

\[ Diese Enumeration ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Der " **streamconfigcapstype** "-Enumerationstyp wird von der TAPI-Struktur " [**\_ Stream \_ config \_ Caps**](tapi-stream-config-caps.md) " als Switch verwendet, um anzugeben, ob ein Audiostreaming oder Video Streaming beteiligt ist.

## <a name="syntax"></a>Syntax


```C++
} StreamConfigCapsType;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="AudioStreamConfigCaps"></span><span id="audiostreamconfigcaps"></span><span id="AUDIOSTREAMCONFIGCAPS"></span>**Audiostreamconfigcaps**
</dt> <dd>

Audiostreamingkonfiguration.

</dd> <dt>

<span id="VideoStreamConfigCaps"></span><span id="videostreamconfigcaps"></span><span id="VIDEOSTREAMCONFIGCAPS"></span>**Videostreamconfigcaps**
</dt> <dd>

Videostreamingkonfiguration.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,1<br/>                                                       |
| Header<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TAPI \_ - \_ streamkonfigurationscaps \_**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




