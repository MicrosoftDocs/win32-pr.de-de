---
title: Getobjectbytextrepresentation-Methode der MicrosoftDNS_ResourceRecord-Klasse
description: Die getobjectbytextrepresentation-Methode ruft eine vorhandene Instanz der MicrosoftDNS \_ resourcerecord-Klasse ab.
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- Getobjectbytextrepresentation-Methode (DNS)
- Getobjectbytextrepresentation-Methode (DNS), MicrosoftDNS_ResourceRecord-Klasse
- MicrosoftDNS_ResourceRecord-Klasse DNS, getobjectbytextrepresentation-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.GetObjectByTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aea2588a70ff4bdab89eae58b65715152d6c7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477277"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>Getobjectbytextrepresentation-Methode der MicrosoftDNS \_ resourcerecord-Klasse

Die **getobjectbytextrepresentation** -Methode ruft eine vorhandene Instanz der [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) -Klasse ab.

## <a name="syntax"></a>Syntax


```mof
void GetObjectByTextRepresentation(
  [in]  string                      DnsServerName,
  [in]  string                      ContainerName,
  [in]  string                      TextRepresentation,
  [out] MicrosoftDns_ResourceRecord RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dnsservername* \[ in\]
</dt> <dd>

Der Name des DNS-Servers, von dem die RR-Datei abgerufen werden soll.

</dd> <dt>

*Containername* \[ in\]
</dt> <dd>

Der Name des Containers, von dem die RR abgerufen werden soll.

</dd> <dt>

*Textrepresentation* \[ in\]
</dt> <dd>

Text Darstellung des zu abzurufenden RR-Werts.

</dd> <dt>

*RR* \[ vorgenommen\]
</dt> <dd>

Verweis auf den instanziierten RR.

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

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Methode "kreateinzustancefromtextrepresentation" der MicrosoftDNS \_ resourcerecord-Klasse**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 





