---
title: Modify-Methode der MicrosoftDNS_SIGType-Klasse
description: Die Modify-Methode aktualisiert eine Signatur (SIG) RR.
ms.assetid: 6a7017da-d3f1-4aba-a53a-96f578518304
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_SIGType-Klasse
- DNS-MicrosoftDNS_SIGType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80fbaa25ec3b6a52aae06f99ed02d50430745dca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475543"
---
# <a name="modify-method-of-the-microsoftdns_sigtype-class"></a>Modify-Methode der MicrosoftDNS- \_ sigtype-Klasse

Die **Modify** -Methode aktualisiert eine Signatur (SIG) RR.

## <a name="syntax"></a>Syntax


```mof
void Modify(
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

## <a name="remarks"></a>Bemerkungen

Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.

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

[**Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ Signatur Type-Klasse**](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





