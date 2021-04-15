---
title: Modify-Methode der MicrosoftDNS_NXTType-Klasse
description: Die Modify-Methode aktualisiert einen nächsten (NXT) Ressourcen Daten Satz.
ms.assetid: 5a21b843-0761-4022-b00a-9dbcd6814454
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_NXTType-Klasse
- DNS-MicrosoftDNS_NXTType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bab7bf8480c7e18914cac4f7ae0deb8a608090f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475879"
---
# <a name="modify-method-of-the-microsoftdns_nxttype-class"></a>Modify-Methode der MicrosoftDNS- \_ nxttype-Klasse

Die **Modify** -Methode aktualisiert einen nächsten (NXT) Ressourcen Daten Satz.

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Nextdomainname* \[ in\]
</dt> <dd>

Der nächste Domänen Name.

</dd> <dt>

*Typen* \[ in\]
</dt> <dd>

Durch Leerzeichen getrennte Liste der RR-Type-mnetmonics für den Besitzer Namen des NXT-Ressourcen Datensatzes.

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

[**MicrosoftDNS \_ nxttype**](microsoftdns-nxttype.md)
</dt> <dt>

[**Die Methode "kreateinzustancefrompropertydata" der Klasse "MicrosoftDNS \_ nxttype"**](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





