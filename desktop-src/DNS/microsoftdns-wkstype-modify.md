---
title: Modify-Methode der MicrosoftDNS_WKSType-Klasse
description: Die Modify-Methode aktualisiert einen Well-Known Services (WKT)-Ressourcen Daten Satz.
ms.assetid: 3a9100eb-dc90-45bb-9739-14026da100fd
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_WKSType-Klasse
- DNS-MicrosoftDNS_WKSType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f7cf58a231d93288a3cdc170fa857bb12687af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859038"
---
# <a name="modify-method-of-the-microsoftdns_wkstype-class"></a>Modify-Methode der MicrosoftDNS- \_ Klasse "wkstype"

Die **Modify** -Methode aktualisiert einen Well-Known Services (WKT)-Ressourcen Daten Satz.

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               InternetAddress,
  [in, optional] uint8                IPProtocol,
  [in, optional] uint8                Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Internetadresse* \[ in, optional\]
</dt> <dd>

Internet-IP-Adresse für den Besitzer des Datensatzes.

</dd> <dt>

*Ipprotocol* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die das IP-Protokoll für diesen Datensatz darstellt. Gültige Werte sind UDP oder TCP.

</dd> <dt>

*Dienste* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die alle Dienste enthält, die vom Wi-Datensatz (well known Service) verwendet werden.

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

[**MicrosoftDNS \_ wkstype**](microsoftdns-wkstype.md)
</dt> <dt>

[**Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ Klasse "wkstype"**](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





