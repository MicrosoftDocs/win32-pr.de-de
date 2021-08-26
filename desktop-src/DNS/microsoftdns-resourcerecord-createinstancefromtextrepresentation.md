---
title: CreateInstanceFromTextRepresentation-Methode der MicrosoftDNS_ResourceRecord-Klasse
description: Die CreateInstanceFromTextRepresentation-Methode instanziiert ein MicrosoftDNS \_ ResourceRecord-Objekt.
ms.assetid: 19600a9a-f75d-40ad-98e5-f81465d10f79
keywords:
- CreateInstanceFromTextRepresentation-Methode DNS
- CreateInstanceFromTextRepresentation-Methode DNS , MicrosoftDNS_ResourceRecord-Klasse
- MicrosoftDNS_ResourceRecord DNS-Klasse, CreateInstanceFromTextRepresentation-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a8ee7f92db1185fe2762b0b308b4fbafdbdd80e7417c7b615939c72333f15e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104020"
---
# <a name="createinstancefromtextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>CreateInstanceFromTextRepresentation-Methode der MicrosoftDNS \_ ResourceRecord-Klasse

Die **CreateInstanceFromTextRepresentation-Methode** instanziiert ein [**MicrosoftDNS \_ ResourceRecord-Objekt.**](microsoftdns-resourcerecord.md)

## <a name="syntax"></a>Syntax


```mof
void CreateInstanceFromTextRepresentation(
  [in]       string                      DnsServerName,
  [in]       string                      ContainerName,
  [in]       string                      TextRepresentation,
  [out, ref] MicrosoftDNS_ResourceRecord &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DnsServerName* \[ In\]
</dt> <dd>

Name des DNS-Servers, auf dem die RR erstellt werden soll.

</dd> <dt>

*ContainerName* \[ In\]
</dt> <dd>

Name des Containers, in dem die neue RR platziert werden soll.

</dd> <dt>

*TextRepresentation* \[ In\]
</dt> <dd>

Textdarstellung der zu erstellenden RR-Instanz.

</dd> <dt>

*RR* \[ out, ref\]
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

[**GetObjectByTextRepresentation-Methode der MicrosoftDNS \_ ResourceRecord-Klasse**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





