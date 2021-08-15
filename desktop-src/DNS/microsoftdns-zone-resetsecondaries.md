---
title: ResetSecondaries-Methode der MicrosoftDNS_Zone-Klasse
description: Die ResetSecondaries-Methode setzt die IP-Adressen für sekundäre DNS-Server in der Zone zurück.
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- RESETSecondaries-Methode DNS
- ResetSecondaries-Methode DNS , MicrosoftDNS_Zone-Klasse
- MicrosoftDNS_Zone DNS-Klasse, ResetSecondaries-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_Zone.ResetSecondaries
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ab3737bc8143f712560e5ea253237c97da4e2401b98886428642210805ca586
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957289"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a>ResetSecondaries-Methode der \_ MicrosoftDNS-Zonenklasse

Die **ResetSecondaries-Methode** setzt die IP-Adressen für sekundäre DNS-Server in der Zone zurück.

## <a name="syntax"></a>Syntax


```mof
void ResetSecondaries(
  [in]       string            SecondaryServers[],
  [in]       uint32            SecureSecondaries,
  [in]       string            NotifyServers[],
  [in]       uint32            Notify,
  [out, ref] MicrosoftDns_Zone &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*SecondaryServers* \[ In\]
</dt> <dd>

Array von IP-Adressen für sekundäre DNS-Server.

</dd> <dt>

*SecureSecondaries* \[ In\]
</dt> <dd>

Gibt die sicherheit an, die angewendet werden soll, und muss eine der folgenden Sein:

-   ZONE \_ SECSECURE \_ NO \_ SECURITY
-   ZONE \_ SECSECURE \_ NS \_ ONLY
-   ZONE \_ SECSECURE \_ LIST \_ ONLY
-   ZONE \_ SECSECURE \_ NO \_ XFR

</dd> <dt>

*NotifyServers* \[ In\]
</dt> <dd>

IP-Adresse der DNS-Server, die benachrichtigt werden sollen, wenn sich die Zone ändert.

</dd> <dt>

*Benachrichtigen* \[ In\]
</dt> <dd>

Die Benachrichtigungseinstellung und muss eine der folgenden sein:

-   ZONE \_ NOTIFY \_ OFF
-   ZONE \_ NOTIFY \_ ALL \_ SECONDARIES
-   NUR \_ \_ ZONENBENACHRICHTIGUNGSLISTE \_

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

RR vom Typ [**MicrosoftDNS \_ Zone**](microsoftdns-zone.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MicrosoftDNS-Zone \_**](microsoftdns-zone.md)
</dt> <dt>

[**AgeAllRecords-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**ChangeZoneType-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**CreateZone-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**ForceRefresh-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**GetDistinguishedName-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**PauseZone-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**ReloadZone-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**ResumeZone-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**UpdateFromDS-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**WriteBackZone-Methode der \_ MicrosoftDNS-Zonenklasse**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





