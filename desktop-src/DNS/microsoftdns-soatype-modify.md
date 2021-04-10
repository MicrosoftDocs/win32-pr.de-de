---
title: Modify-Methode der MicrosoftDNS_SOAType-Klasse
description: Die Modify-Methode aktualisiert einen Start of Authority (SOA)-Ressourcen Daten Satz.
ms.assetid: 531b770d-9ac9-43da-8595-fbc175b51b23
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_SOAType-Klasse
- DNS-MicrosoftDNS_SOAType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_SOAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff40abc7f4e93b7122a1c48889c17f9efc4f625
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040227"
---
# <a name="modify-method-of-the-microsoftdns_soatype-class"></a>Modify-Methode der MicrosoftDNS- \_ soatype-Klasse

Die **Modify** -Methode aktualisiert einen Start of Authority (SOA)-Ressourcen Daten Satz.

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               SerialNumber,
  [in, optional] string               PrimaryServer,
  [in, optional] string               ResponsibleParty,
  [in, optional] uint32               RefreshInterval,
  [in, optional] uint32               RetryDelay,
  [in, optional] uint32               ExpireLimit,
  [in, optional] uint32               MinimumTTL,
  [out, ref]     MicrosoftDNS_SOAType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*SerialNumber* \[ in, optional\]
</dt> <dd>

Eine SOA-Seriennummer, die angibt, wie oft die Zone aktualisiert wurde, und wird von [*sekundären Servern*](s-gly.md) verwendet, um zu bestimmen, ob eine Zonen Übertragung notwendig ist.

</dd> <dt>

*Primaryserver* \[ in, optional\]
</dt> <dd>

Der Name des primären Servers.

</dd> <dt>

*Verantwortliche Partei* \[ in, optional\]
</dt> <dd>

Post Fach Adresse der verantwortlichen Partei in Form von Alias. Domain, z. b. xyz.Microsoft.com. Beachten Sie die Verwendung eines Zeitraums anstelle eines bei-Symbol (@).

</dd> <dt>

*Aktuerfrischendes Intervall* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, bevor die Zone, in der dieser Datensatz enthalten ist, aktualisiert werden soll.

</dd> <dt>

*RetryDelay* \[ in, optional\]
</dt> <dd>

Die Zeit (in Sekunden), die der DNS-Server zwischen namens Auflösungs versuchen verzögert werden soll.

</dd> <dt>

*Expirelimit* \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die sekundäre Server auf eine Antwort vom primären Server warten sollten, bevor die Kopien der Zonendatei als ungültig verworfen werden.

</dd> <dt>

*Minimumttl* \[ in, optional\]
</dt> <dd>

TTL-Zeit (in Sekunden), die auf Ressourcen Einträge in der Zone angewendet wird, die nicht Ihre eigene Gültigkeitsdauer angeben.

</dd> <dt>

*RR* \[ Out, Ref\]
</dt> <dd>

Verweis auf das geänderte Objekt

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS- \_ soatype**](microsoftdns-soatype.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





