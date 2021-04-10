---
title: Resetsecon-Replikats-Methode der MicrosoftDNS_Zone-Klasse
description: Die resetsecon-Methode setzt die IP-Adressen für sekundäre DNS-Server in der Zone zurück.
ms.assetid: b9a47714-f180-40cf-831a-f59e804a4ca2
keywords:
- Resetsecon-Methode (DNS)
- Resetsecon-Methode (DNS), MicrosoftDNS_Zone-Klasse
- DNS-MicrosoftDNS_Zone Klasse, resetseconreplikat-Methode
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
ms.openlocfilehash: 3a78d65b2153782c38d6d91d34f642860e896ed1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956787"
---
# <a name="resetsecondaries-method-of-the-microsoftdns_zone-class"></a>Resetsecon-Replikats-Methode der MicrosoftDNS- \_ Zonen Klasse

Die **resetsecon-** Methode setzt die IP-Adressen für sekundäre DNS-Server in der Zone zurück.

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

*Secondaryservers* \[ in\]
</dt> <dd>

Array von IP-Adressen für sekundäre DNS-Server.

</dd> <dt>

*Securesecon-* \[ Replikate in\]
</dt> <dd>

Gibt die anzuwendende Sicherheit an und muss eine der folgenden sein:

-   Zone \_ secsecure \_ No \_ Security
-   \_nur Zonen secsecure \_ NS \_
-   nur Zonen- \_ secsecure- \_ Liste \_
-   Zone \_ secsecure \_ No \_ XFR

</dd> <dt>

*Notifyservers* \[ in\]
</dt> <dd>

IP-Adresse der DNS-Server, die benachrichtigt werden sollen, wenn die Zone geändert wird.

</dd> <dt>

*Benachrichtigen* \[ in\]
</dt> <dd>

Benachrichtigungs Einstellung und muss eine der folgenden sein:

-   Benachrichtigung über Zonen \_ Benachrichtigung \_
-   Zonen \_ Benachrichtigung für \_ alle \_ sekundären Datenbanken
-   \_nur Zonen Benachrichtigungs \_ Liste \_

</dd> <dt>

*RR* \[ Out, Ref\]
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
| MOF<br/>                      | <dl> <dt>Dnsprov. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS- \_ Zone**](microsoftdns-zone.md)
</dt> <dt>

[**AgeAllRecords-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-ageallrecords.md)
</dt> <dt>

[**Changezonetype-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-changezonetype.md)
</dt> <dt>

[**Die Methode "kreatezone" der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-createzone.md)
</dt> <dt>

[**ForceRefresh-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-forcerefresh.md)
</dt> <dt>

[**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-getdistinguishedname.md)
</dt> <dt>

[**Pauzzone-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-pausezone.md)
</dt> <dt>

[**Reloadzone-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-reloadzone.md)
</dt> <dt>

[**Resumezone-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-resumezone.md)
</dt> <dt>

[**Updatefromds-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-updatefromds.md)
</dt> <dt>

[**"Write Backzone"-Methode der MicrosoftDNS- \_ Zonen Klasse**](microsoftdns-zone-writebackzone.md)
</dt> </dl>

 

 





