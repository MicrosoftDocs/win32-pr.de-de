---
description: 'Die Member der typisierten Info-Enumeration für den Teilnehmer \_ \_ identifizieren den Typ der Teilnehmer Informationen, die von der itparticipants:: get- \_ Methode "participanttypdinfo" abgerufen werden. Diese Enumeration wird von Anwendungen verwendet, die auf die ipconf-MSP zugreifen.'
ms.assetid: ca933d8c-bfb4-4a92-b412-112e228ccca2
title: PARTICIPANT_TYPED_INFO-Enumeration (confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ab94a487f0ea098ee9b92144874057dc463036
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370665"
---
# <a name="participant_typed_info-enumeration"></a>Teilnehmer mit \_ typisierter \_ Enumeration

\[**Teilnehmer \_ Typisierte \_ Informationen** sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die Member der **\_ typisierten \_ Info** -Enumeration für den Teilnehmer identifizieren den Typ der Teilnehmer Informationen, die von der [**itparticipants:: Get-Methode " \_ participanttypdinfo**](itparticipant-get-participanttypedinfo.md) " abgerufen werden. Diese Enumeration wird von Anwendungen verwendet, die auf die [ipconf-MSP](ipconf-msp.md)zugreifen.

## <a name="syntax"></a>Syntax


```C++
} PARTICIPANT_TYPED_INFO;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI \_ CanonicalName**
</dt> <dd>

Kanonischer Name des Teilnehmers, z someone@example.com . b..

</dd> <dt>

<span id="PTI_NAME"></span><span id="pti_name"></span>**PTI- \_ Name**
</dt> <dd>

Anzeigbarer Name des Teilnehmers.

</dd> <dt>

<span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**PTI \_ EmailAddress**
</dt> <dd>

E-Mail-Adresse des Teilnehmers

</dd> <dt>

<span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI- \_ PhoneNumber**
</dt> <dd>

Telefon Adresse des Teilnehmers.

</dd> <dt>

<span id="PTI_LOCATION"></span><span id="pti_location"></span>**PTI- \_ Speicherort**
</dt> <dd>

Geografische Adresse des Teilnehmers.

</dd> <dt>

<span id="PTI_TOOL"></span><span id="pti_tool"></span>**PTI- \_ Tool**
</dt> <dd>

Die Anwendung des Teilnehmers.

</dd> <dt>

<span id="PTI_NOTES"></span><span id="pti_notes"></span>**PTI- \_ Notizen**
</dt> <dd>

Hinweise zum Teilnehmer.

</dd> <dt>

<span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI \_ Privat**
</dt> <dd>

Definiert eine experimentelle oder anwendungsspezifische Erweiterung der Quell Beschreibung (SDES). Weitere Informationen finden Sie in RFC 1889.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>"Confpriv. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Itteilnehmer:: get \_ participanttypdinfo**](itparticipant-get-participanttypedinfo.md)
</dt> <dt>

[Ipconf-msp](ipconf-msp.md)
</dt> <dt>

[Ipconf-MSP-Schnittstellen](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




