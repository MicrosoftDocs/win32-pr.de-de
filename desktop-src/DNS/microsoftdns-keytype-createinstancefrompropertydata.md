---
title: CreateInstanceFromPropertyData-Methode der MicrosoftDNS_KEYType-Klasse
description: Die CreateInstanceFromPropertyData-Methode instanziiert einen KEY-Ressourcendatensatz.
ms.assetid: 77d7b800-4077-46da-9199-e2abb5801978
keywords:
- CreateInstanceFromPropertyData-Methode DNS
- CreateInstanceFromPropertyData-Methode DNS, MicrosoftDNS_KEYType-Klasse
- MicrosoftDNS_KEYType-Klasse DNS, CreateInstanceFromPropertyData-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 315ef898a101b3a86fa5a3085e4a171edd8efa28972cf62c006cc0eb87e354b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913140"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_keytype-class"></a>CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ KEYType-Klasse

Die **CreateInstanceFromPropertyData-Methode** instanziiert einen KEY-Ressourcendatensatz.

## <a name="syntax"></a>Syntax


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               Flags,
  [in]           uint16               Protocol,
  [in]           uint16               Algorithm,
  [in]           string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
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

Name des Containers für die Zone, den Cache oder die RootHints-Instanz, die diese RR enthält.

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

*Gültigkeitsdauer* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, in der die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Flags zum Angeben der Zuordnung, wie in IETF RFC 2535 beschrieben.

</dd> <dt>

*Protokoll* \[ In\]
</dt> <dd>

Protokoll, für das der im Ressourcendatensatz angegebene Schlüssel verwendet werden kann. Die zugewiesenen Werte werden in der folgenden Tabelle angezeigt.



| Wert                                                                                                    | Bedeutung                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>     | TLS<br/>           |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>     | E-Mail<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>     | Dnssec<br/>        |
| <span id="4"></span><dl> <dt>**4**</dt> </dl>     | IPsec<br/>         |
| <span id="255"></span><dl> <dt>**255**</dt> </dl> | Alle Protokolle<br/> |



 

</dd> <dt>

*Algorithmus* \[ In\]
</dt> <dd>

Algorithmus, der mit dem im Ressourcendatensatz angegebenen Schlüssel verwendet wird. Die zugewiesenen Werte werden in der folgenden Tabelle angezeigt.



| Wert                                                                                                | Bedeutung                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Kryptografie der elliptischen Kurve<br/> |



 

</dd> <dt>

*PublicKey* \[ In\]
</dt> <dd>

Öffentlicher Schlüssel, dargestellt in Basis 64, wie in Anhang A von RFC 2535 beschrieben.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Verweis auf das neue Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\Stamm-MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS \_ KEYType**](microsoftdns-keytype.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ KEYType-Klasse**](microsoftdns-keytype-modify.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





