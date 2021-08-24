---
title: Modify-Methode der MicrosoftDNS_SOAType-Klasse
description: Die Modify-Methode aktualisiert einen SOA-Ressourceneintrag (Start Of Authority).
ms.assetid: 531b770d-9ac9-43da-8595-fbc175b51b23
keywords:
- Ändern der DNS-Methode
- Modify method DNS , MicrosoftDNS_SOAType class
- MicrosoftDNS_SOAType-Klasse DNS, Modify-Methode
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
ms.openlocfilehash: 74785804ebed8266443f0dd708a5d122e350a6cf88b91f228d2ce266481dffaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825080"
---
# <a name="modify-method-of-the-microsoftdns_soatype-class"></a>Modify-Methode der \_ MicrosoftDNS-SOAType-Klasse

Die **Modify-Methode** aktualisiert einen SOA-Ressourceneintrag (Start Of Authority).

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

*Gültigkeitsdauer* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, in der die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*SerialNumber* \[ in, optional\]
</dt> <dd>

SOA-Seriennummer, die die Anzahl der Aktualisierungen der Zone darstellt und von [*sekundären Servern*](s-gly.md) verwendet wird, um zu bestimmen, ob eine Zonenübertragung erforderlich ist.

</dd> <dt>

*PrimaryServer* \[ in, optional\]
</dt> <dd>

Name des primären Servers.

</dd> <dt>

*ResponsibleParty* \[ in, optional\]
</dt> <dd>

Postfachadresse der verantwortlichen Partei in Form von alias.domain, z. B. xyz.microsoft.com. Beachten Sie die Verwendung eines Punkts anstelle eines at-Symbols (@).

</dd> <dt>

*RefreshInterval* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, bevor die Zone, die diesen Datensatz enthält, aktualisiert werden soll.

</dd> <dt>

*RetryDelay* \[ in, optional\]
</dt> <dd>

Die Zeit in Sekunden, die der DNS-Server zwischen den Namensauflösungsversuchen verzögern sollte.

</dd> <dt>

*ExpireLimit* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, in der sekundäre Server auf eine Antwort vom primären Server warten sollten, bevor ihre Kopien der Zonendatei als ungültig verworfen werden.

</dd> <dt>

*MinimumTTL* \[ in, optional\]
</dt> <dd>

Die Gültigkeitsdauer (in Sekunden) wird auf Ressourcendatensätze in der Zone angewendet, die keine eigene Gültigkeitsdauer angeben.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Verweis auf das geänderte Objekt

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Alle nicht angegebenen Parameter bleiben im geänderten Datensatz unverändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\Stamm-MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS \_ SOAType**](microsoftdns-soatype.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





