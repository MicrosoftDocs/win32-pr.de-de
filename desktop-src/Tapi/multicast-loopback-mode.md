---
description: Die Multicast- \_ Loopback \_ Modus-Enumeration beschreibt den Multicast-Loopback Modus.
ms.assetid: bf9c3665-71cc-4cde-9ad4-1a8b62eddf9f
title: MULTICAST_LOOPBACK_MODE-Enumeration (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a15505efcd1a9e399866b104da0582ccf846689
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355058"
---
# <a name="multicast_loopback_mode-enumeration"></a>Multicast- \_ Loopback \_ Modus-Enumeration

\[**Multicast \_ Der Loopback \_ Modus** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **Multicast- \_ Loopback \_ Modus** -Enumeration beschreibt den Multicast-Loopback Modus.

## <a name="syntax"></a>Syntax


```C++
} MULTICAST_LOOPBACK_MODE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM \_ kein \_ Loopback**
</dt> <dd>

Multicast Loopback ist deaktiviert. Dies bedeutet, dass zwei Anwendungen auf dem gleichen Computer, die derselben Multicast Gruppe beitreten, die Pakete der anderen Anwendungen erhalten können.

</dd> <dt>

<span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**\_vollständiges \_ Loopback von mm**
</dt> <dd>

Alle gesendeten Pakete werden ebenfalls in eine Schleife zurückgeleitet. Dieser Modus ist nur für Tests nützlich.

</dd> <dt>

<span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**selektive mm- \_ \_ Loopback**
</dt> <dd>

Selektives Loopback ist aktiviert. Dies bedeutet, dass die Aktivierung mehrerer Anwendungen auf einem Computer ohne Verwirrung in die gleiche Multicast Gruppe eingebunden werden kann. Die Pakete werden vom Stapel zurückgeleitet, und jede RTP-Sitzung ist für das Herausfiltern unerwünschter Pakete zuständig.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>"Confpriv. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imulticastcontrol:: get \_ loopbackmode**](imulticastcontrol-get-loopbackmode.md)
</dt> <dt>

[**Imulticastcontrol::p UT- \_ Loopbackmodus**](imulticastcontrol-put-loopbackmode.md)
</dt> </dl>

 

 




