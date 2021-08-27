---
description: Die Member der MEMBER TYPED INFO-Enum identifizieren den Typ der Teilnehmerinformationen, die von der \_ \_ ITParticipant::get \_ ParticipantTypedInfo-Methode abgerufen werden. Diese Enum wird von Anwendungen verwendet, die auf den IPConf-MSP zugreifen.
ms.assetid: ca933d8c-bfb4-4a92-b412-112e228ccca2
title: PARTICIPANT_TYPED_INFO -Enumeration (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de57331cd0774409118b7253fd5705879e3b3504b04b20a16aa2df269504512
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100570"
---
# <a name="participant_typed_info-enumeration"></a>PARTICIPANT \_ TYPED \_ INFO-Enumeration

\[**TEILNEHMER \_ TYPED \_ INFO** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet ähnliche Funktionen.\]

Die Member der **MEMBER \_ TYPED INFO-Enum \_** identifizieren den Typ der Teilnehmerinformationen, die von der [**ITParticipant::get \_ ParticipantTypedInfo-Methode abgerufen**](itparticipant-get-participanttypedinfo.md) werden. Diese Enum wird von Anwendungen verwendet, die auf [den IPConf MSP zugreifen.](ipconf-msp.md)

## <a name="syntax"></a>Syntax


```C++
} PARTICIPANT_TYPED_INFO;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="PTI_CANONICALNAME"></span><span id="pti_canonicalname"></span>**PTI \_ CANONICALNAME**
</dt> <dd>

Kanonischer Name des Teilnehmers, z. someone@example.com B. .

</dd> <dt>

<span id="PTI_NAME"></span><span id="pti_name"></span>**\_PTI-NAME**
</dt> <dd>

Der anzeigebare Name des Teilnehmers.

</dd> <dt>

<span id="PTI_EMAILADDRESS"></span><span id="pti_emailaddress"></span>**PTI \_ EMAILADDRESS**
</dt> <dd>

Die E-Mail-Adresse des Teilnehmers.

</dd> <dt>

<span id="PTI_PHONENUMBER"></span><span id="pti_phonenumber"></span>**PTI \_ PHONENUMBER**
</dt> <dd>

Telefonnummer des Teilnehmers.

</dd> <dt>

<span id="PTI_LOCATION"></span><span id="pti_location"></span>**\_PTI-SPEICHERORT**
</dt> <dd>

Geografische Adresse des Teilnehmers.

</dd> <dt>

<span id="PTI_TOOL"></span><span id="pti_tool"></span>**\_PTI-TOOL**
</dt> <dd>

Anwendung des Teilnehmers.

</dd> <dt>

<span id="PTI_NOTES"></span><span id="pti_notes"></span>**\_PTI-HINWEISE**
</dt> <dd>

Hinweise zum Teilnehmer.

</dd> <dt>

<span id="PTI_PRIVATE"></span><span id="pti_private"></span>**PTI \_ PRIVATE**
</dt> <dd>

Definiert eine experimentelle oder anwendungsspezifische SDES-Erweiterung (Source Description). Weitere Informationen finden Sie unter RFC 1889.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3.0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ITParticipant::get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md)
</dt> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[IPConf-MSP-Schnittstellen](ipconf-msp-interfaces.md)
</dt> </dl>

 

 




