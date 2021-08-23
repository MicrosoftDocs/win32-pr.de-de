---
title: CreateInstanceFromPropertyData-Methode der MicrosoftDNS_SIGType-Klasse
description: Die CreateInstanceFromPropertyData-Methode instanziiert einen Signaturressourceneintrag (SIG).
ms.assetid: 8e83e56f-d2b3-4b71-be70-7d2640d49845
keywords:
- CreateInstanceFromPropertyData-Methode DNS
- CreateInstanceFromPropertyData-Methode DNS, MicrosoftDNS_SIGType-Klasse
- MicrosoftDNS_SIGType-Klasse DNS, CreateInstanceFromPropertyData-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90501af2f6e492e56d17f88fb6bc74cc72522503760688457832a2374918100e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076724"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_sigtype-class"></a>CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ SIGType-Klasse

Die **CreateInstanceFromPropertyData-Methode** instanziiert einen Signaturressourceneintrag (SIG).

## <a name="syntax"></a>Syntax


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           uint16               TypeCovered,
  [in]           uint16               Algorithm,
  [in]           uint16               Labels,
  [in]           uint32               OriginalTTL,
  [in]           uint32               SignatureExpiration,
  [in]           uint32               SignatureInception,
  [in]           uint16               KeyTag,
  [in]           string               SignerName,
  [in]           string               Signature,
  [out, ref]     MicrosoftDNS_SIGType &RR
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

*TypeCovered* \[ In\]
</dt> <dd>

RR-Typ, der von diesem SIG abgedeckt wird.

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

*Bezeichnungen* \[ In\]
</dt> <dd>

Anzahl der Bezeichnungen ohne Vorzeichen im ursprünglichen SIG RR-Besitzernamen. Die Anzahl enthält weder die NULL-Bezeichnung für den Stamm noch anfängliche Platzhalter.

</dd> <dt>

*OriginalTTL* \[ In\]
</dt> <dd>

Gültigkeitsdauer des von der SIG signierten RR-Satzes.

</dd> <dt>

*SignatureExpiration* \[ In\]
</dt> <dd>

Signaturablaufdatum, ausgedrückt in Sekunden seit dem 1. Januar 1970, Greenwich Mean Time (GMT), ohne Schaltsekunden.

</dd> <dt>

*SignatureInception* \[ In\]
</dt> <dd>

Datum und Uhrzeit, zu der die Signatur gültig wird, ausgedrückt in Sekunden seit Dem 1. Januar 1970, Greenwich Mean Time (GMT), ohne Schaltsekunden.

</dd> <dt>

*KeyTag* \[ In\]
</dt> <dd>

Methode zum Auswählen eines Schlüssels, der eine SIG überprüft. Informationen zur Methode zum Berechnen eines KeyTag finden Sie unter RFC 2535, Anhang C.

</dd> <dt>

*SignerName* \[ In\]
</dt> <dd>

Domänenname des Signierers, der die SIG RR generiert hat.

</dd> <dt>

*Signatur* \[ In\]
</dt> <dd>

Signatur, dargestellt in Basis 64, formatiert gemäß RFC 2535, Anhang A.

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

[**MicrosoftDNS \_ SIGType**](microsoftdns-sigtype.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ SIGType-Klasse**](microsoftdns-sigtype-modify.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





