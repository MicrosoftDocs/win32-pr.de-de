---
title: CreateInstanceFromPropertyData-Methode der MicrosoftDNS_MRType Klasse
description: Die CreateInstanceFromPropertyData-Methode instanziiert einen MR-Ressourcendatensatz (Mailbox Rename).
ms.assetid: 7dab86e0-bf05-4e98-b1f8-e1daecd4425c
keywords:
- CreateInstanceFromPropertyData-Methode DNS
- CreateInstanceFromPropertyData-Methode DNS , MicrosoftDNS_MRType-Klasse
- MicrosoftDNS_MRType DNS-Klasse, CreateInstanceFromPropertyData-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d08ca8b36f65b25f0ab35d3aba531d4d734c1a768f3b4d092e2b4be0075c7889
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967280"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mrtype-class"></a>CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ MRType-Klasse

Die **CreateInstanceFromPropertyData-Methode** instanziiert einen MR-Ressourcendatensatz (Mailbox Rename).

## <a name="syntax"></a>Syntax


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MRMailbox,
  [out, ref]     MicrosoftDNS_MRType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DnsServerName* \[ In\]
</dt> <dd>

FQDN oder IP-Adresse des DNS-Servers, der diese RR enthält.

</dd> <dt>

*ContainerName* \[ In\]
</dt> <dd>

Name des Containers für die Zone-, Cache- oder RootHints-Instanz, die diese RR enthält.

</dd> <dt>

*OwnerName* \[ In\]
</dt> <dd>

Besitzername für die RR.

</dd> <dt>

*RecordClass* \[ in, optional\]
</dt> <dd>

Klasse der RR. Der Standardwert ist 1. Die folgenden Werte sind gültig.



| Wert                                                                                                | Bedeutung                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | IN (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (CHAOS)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

*TTL* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, die die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*MRMailbox* \[ In\]
</dt> <dd>

Der FQDN gibt ein Postfach an, das die richtige Umbenennung des Postfachs ist, das im Besitzernamen des Datensatzes angegeben ist.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Verweis auf das neue -Objekt.

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

[**MicrosoftDNS \_ MRType**](microsoftdns-mrtype.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ MRType-Klasse**](microsoftdns-mrtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





