---
title: Modify-Methode der MicrosoftDNS_KEYType Klasse
description: Die Modify-Methode aktualisiert einen KEY-Ressourcendatensatz.
ms.assetid: 0ea1e0e5-ccd1-4800-b0c3-27795c36250c
keywords:
- Ändern der DNS-Methode
- Modify method DNS , MicrosoftDNS_KEYType class
- MicrosoftDNS_KEYType DNS-Klasse, Modify-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_KEYType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff5b657e940716a7afa2113dcbdc6836ab3680c1dfe37b88a454d9bdd0c7bc28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163256"
---
# <a name="modify-method-of-the-microsoftdns_keytype-class"></a>Modify-Methode der MicrosoftDNS \_ KEYType-Klasse

Die **Modify-Methode** aktualisiert einen KEY-Ressourcendatensatz.

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint16               Flags,
  [in, optional] uint16               Protocol,
  [in, optional] uint16               Algorithm,
  [in, optional] string               PublicKey,
  [out, ref]     MicrosoftDNS_KEYType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TTL* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, die die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Flags* \[ in, optional\]
</dt> <dd>

Flags, die zum Angeben der Zuordnung verwendet werden, wie in IETF RFC 2535 beschrieben.

</dd> <dt>

*Protokoll* \[ in, optional\]
</dt> <dd>

Protokoll, für das der in der RR angegebene Schlüssel verwendet werden kann. Die zugewiesenen Werte sind in der folgenden Tabelle aufgeführt.



| Wert                                                                                                    | Bedeutung                  |
|----------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl>     | TLS<br/>           |
| <span id="2"></span><dl> <dt>**2**</dt> </dl>     | E-Mail<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl>     | Dnssec<br/>        |
| <span id="4"></span><dl> <dt>**4**</dt> </dl>     | IPsec<br/>         |
| <span id="255"></span><dl> <dt>**255**</dt> </dl> | Alle Protokolle<br/> |



 

</dd> <dt>

*Algorithmus* \[ in, optional\]
</dt> <dd>

Algorithmus, der mit dem im Ressourcendatensatz angegebenen Schlüssel verwendet wird. Die zugewiesenen Werte sind in der folgenden Tabelle aufgeführt.



| Wert                                                                                                | Bedeutung                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Kryptografie mit elliptischen Kurven<br/> |



 

</dd> <dt>

*PublicKey* \[ in, optional\]
</dt> <dd>

Öffentlicher Schlüssel, dargestellt in Base64, wie in Anhang A von RFC 2535 beschrieben.

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

[**MicrosoftDNS \_ KEYType**](microsoftdns-keytype.md)
</dt> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ KEYType-Klasse**](microsoftdns-keytype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





