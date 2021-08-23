---
title: GetObjectByTextRepresentation-Methode der MicrosoftDNS_ResourceRecord Klasse
description: Die GetObjectByTextRepresentation-Methode ruft eine vorhandene Instanz der MicrosoftDNS \_ ResourceRecord-Klasse ab.
ms.assetid: d25e10de-81fa-4220-b2b8-d9a65298b629
keywords:
- GetObjectByTextRepresentation-Methode DNS
- GetObjectByTextRepresentation-Methode DNS , MicrosoftDNS_ResourceRecord-Klasse
- MicrosoftDNS_ResourceRecord DNS-Klasse, GetObjectByTextRepresentation-Methode
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
ms.openlocfilehash: 08e3b824ccabe86e842d4ef6f61799b33110b5d28a58658a6d4cbedc824c134b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692420"
---
# <a name="getobjectbytextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>GetObjectByTextRepresentation-Methode der MicrosoftDNS \_ ResourceRecord-Klasse

Die **GetObjectByTextRepresentation-Methode** ruft eine vorhandene Instanz der [**MicrosoftDNS \_ ResourceRecord-Klasse**](microsoftdns-resourcerecord.md) ab.

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

*DnsServerName* \[ In\]
</dt> <dd>

Name des DNS-Servers, von dem die RR abgerufen werden soll.

</dd> <dt>

*ContainerName* \[ In\]
</dt> <dd>

Name des Containers, aus dem die RR erhalten werden soll.

</dd> <dt>

*TextRepresentation* \[ In\]
</dt> <dd>

Textdarstellung der abzurufenden RR.

</dd> <dt>

*RR* \[ out\]
</dt> <dd>

Verweis auf die instanziierte RR.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**CreateInstanceFromTextRepresentation-Methode der MicrosoftDNS \_ ResourceRecord-Klasse**](microsoftdns-resourcerecord-createinstancefromtextrepresentation.md)
</dt> </dl>

 

 





