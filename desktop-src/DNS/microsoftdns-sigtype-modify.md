---
title: Modify-Methode der MicrosoftDNS_SIGType Klasse
description: Die Modify-Methode aktualisiert eine Signatur-RR (SIG).
ms.assetid: 6a7017da-d3f1-4aba-a53a-96f578518304
keywords:
- Ändern der DNS-Methode
- Modify method DNS , MicrosoftDNS_SIGType class
- MicrosoftDNS_SIGType DNS-Klasse, Modify-Methode
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
ms.openlocfilehash: be64eb494eb72ace437aeade8d7d01a6675f99b2b44c4fa461a8e60c8ed3de1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692280"
---
# <a name="modify-method-of-the-microsoftdns_sigtype-class"></a>Modify-Methode der MicrosoftDNS \_ SIGType-Klasse

Die **Modify-Methode** aktualisiert eine Signatur-RR (SIG).

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

*TTL* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, die die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*TypeCovered* \[ In\]
</dt> <dd>

Der RR-Typ, der von dieser SIG abgedeckt wird.

</dd> <dt>

*Algorithmus* \[ In\]
</dt> <dd>

Algorithmus, der mit dem im Ressourcendatensatz angegebenen Schlüssel verwendet wird. Die zugewiesenen Werte sind in der folgenden Tabelle aufgeführt.



| Wert                                                                                                | Bedeutung                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Kryptografie mit elliptischen Kurven<br/> |



 

</dd> <dt>

*Bezeichnungen* \[ In\]
</dt> <dd>

Anzahl der Bezeichnungen ohne Vorzeichen im ursprünglichen SIG RR-Besitzernamen. Die Anzahl enthält weder die NULL-Bezeichnung für den Stamm noch anfängliche Platzhalter.

</dd> <dt>

*OriginalTTL* \[ In\]
</dt> <dd>

TTL des RR-Sets, das vom SIG signiert wurde.

</dd> <dt>

*SignatureExpiration* \[ In\]
</dt> <dd>

Ablaufdatum der Signatur, ausgedrückt in Sekunden seit dem Anfang des 1. Januar 1970, Greenwich Mean Time (GMT), ohne Schaltsekunden.

</dd> <dt>

*SignatureInception* \[ In\]
</dt> <dd>

Datum und Uhrzeit der Gültigkeit der Signatur, ausgedrückt in Sekunden seit Dem Anfang des 1. Januar 1970, Greenwich Mean Time (GMT), ohne Schaltsekunden.

</dd> <dt>

*KeyTag* \[ In\]
</dt> <dd>

Methode zum Auswählen eines Schlüssels, der eine SIG überprüft. Informationen zur Methode zum Berechnen eines KeyTags finden Sie unter RFC 2535, Anhang C.

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

Verweis auf das neue -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Nicht angegebene Parameter bleiben im geänderten Datensatz unverändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS \_ SIGType**](microsoftdns-sigtype.md)
</dt> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ SIGType-Klasse**](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





