---
description: Die H245 \_ -funktionsenum beschreibt die Unterstützung für Audioformate und Videoformate.
ms.assetid: 76aeb3a1-3233-4425-b9db-efacbedc309e
title: H245_CAPABILITY-Enumeration (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7a6f81f87480f221f87680d9cf086120deb2de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372479"
---
# <a name="h245_capability-enumeration"></a>H245- \_ funktionsenumeration

\[**H245 \_ Die Funktion** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **H245 \_** -funktionsenum beschreibt die Unterstützung für Audioformate und Videoformate.

## <a name="syntax"></a>Syntax


```C++
} H245_CAPABILITY;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="HC_G711"></span><span id="hc_g711"></span>**HC \_ G711**
</dt> <dd>

Das G. 711-Audioprotokoll wird unterstützt.

</dd> <dt>

<span id="HC_G723"></span><span id="hc_g723"></span>**HC \_ g723**
</dt> <dd>

Das G. 723-Audioprotokoll wird unterstützt.

</dd> <dt>

<span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**HC \_ H263QCIF**
</dt> <dd>

Das H. 263 Video-Protokoll wird unterstützt.

</dd> <dt>

<span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**HC \_ H261QCIF**
</dt> <dd>

Das H. 263 Video-Protokoll wird unterstützt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>H323priv. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IH323LineEx:: setdefaultcapabilityprefergenz**](ih323lineex-setdefaultcapabilitypreferrence.md)
</dt> </dl>

 

 




