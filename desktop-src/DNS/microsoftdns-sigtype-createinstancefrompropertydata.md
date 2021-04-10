---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_SIGType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen Ressourcen Eintrag der Signatur (SIG).
ms.assetid: 8e83e56f-d2b3-4b71-be70-7d2640d49845
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_SIGType
- DNS-MicrosoftDNS_SIGType Klasse, Methode "Methode"
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
ms.openlocfilehash: c21660572d9557e6425b459c5694a7eeee4722cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040229"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_sigtype-class"></a>Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ Signatur Type-Klasse

Die Methode " **kreatinstancefrompropertydata** " instanziiert einen Ressourcen Eintrag der Signatur (SIG).

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

*Dnsservername* \[ in\]
</dt> <dd>

Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.

</dd> <dt>

*Containername* \[ in\]
</dt> <dd>

Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.

</dd> <dt>

Besitzer *Name* \[ in\]
</dt> <dd>

Der Besitzer Name für die RR.

</dd> <dt>

*Recordclass* \[ in, optional\]
</dt> <dd>

Die Klasse von RR. Der Standardwert ist 1. Die folgenden Werte sind gültig.



| Wert                                                                                                | Bedeutung                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | IN (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (Chaos)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Typecovered* \[ in\]
</dt> <dd>

Der Typ von RR, der von diesem SIG abgedeckt wird.

</dd> <dt>

*Algorithmus* \[ in\]
</dt> <dd>

Der Algorithmus, der mit dem im Ressourcen Daten Satz angegebenen Schlüssel verwendet wird. Die zugewiesenen Werte sind in der folgenden Tabelle aufgeführt.



| Wert                                                                                                | Bedeutung                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Kryptografie mit elliptischer Kurve<br/> |



 

</dd> <dt>

*Bezeichnungen* \[ in\]
</dt> <dd>

Anzahl nicht signierter Bezeichnungen im ursprünglichen SIG RR-Besitzer Namen. Die Anzahl enthält nicht die NULL-Bezeichnung für den Stamm und keine anfänglichen Platzhalter.

</dd> <dt>

*Originalttl* \[ in\]
</dt> <dd>

Gültigkeitsdauer der von SIG signierten RR-Menge.

</dd> <dt>

*Signatureablauf* \[ in\]
</dt> <dd>

Das Ablaufdatum der Signatur, ausgedrückt in Sekunden seit dem 1. Januar 1970, Greenwich Mean Time (GMT), ohne Schaltsekunden.

</dd> <dt>

*SignatureInception* \[ in\]
</dt> <dd>

Datum und Uhrzeit, zu der die Signatur gültig wird, ausgedrückt in Sekunden seit dem 1. Januar 1970, Greenwich Mean Time (GMT), mit Ausnahme von Schaltsekunden.

</dd> <dt>

*Keytag* \[ in\]
</dt> <dd>

Methode, die zum Auswählen eines Schlüssels verwendet wird, der einen SIG überprüft. Informationen zur Methode, mit der ein keytag berechnet wird, finden Sie in RFC 2535, Anhang C.

</dd> <dt>

*Signatur Name* \[ in\]
</dt> <dd>

Der Domänen Name des Signatur Gebers, der die SIG RR generiert hat.

</dd> <dt>

*Signatur* \[ in\]
</dt> <dd>

Die in Basis 64 dargestellte Signatur, wie in RFC 2535, Anhang A, formatiert.

</dd> <dt>

*RR* \[ Out, Ref\]
</dt> <dd>

Verweis auf das neue-Objekt.

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

[**MicrosoftDNS- \_ sigtype**](microsoftdns-sigtype.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS- \_ sigtype-Klasse**](microsoftdns-sigtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





