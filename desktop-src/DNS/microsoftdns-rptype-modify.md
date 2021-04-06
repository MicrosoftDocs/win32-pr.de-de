---
title: Modify-Methode der MicrosoftDNS_RPType-Klasse
description: Die Modify-Methode aktualisiert einen Ressourcen Daten Satz für Verantwortliche Personen (RP).
ms.assetid: a779b905-922c-42ff-b3d9-318b3a848230
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_RPType-Klasse
- DNS-MicrosoftDNS_RPType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ec575424e6e26c79f8d6a27e62732cad6ddc57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858991"
---
# <a name="modify-method-of-the-microsoftdns_rptype-class"></a>Modify-Methode der MicrosoftDNS- \_ rptype-Klasse

Die **Modify** -Methode aktualisiert einen Ressourcen Daten Satz für Verantwortliche Personen (RP).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              RPMailbox,
  [in, optional] string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Rpmailbox* \[ in, optional\]
</dt> <dd>

Vollständiger vollständiger vollständiger Name des Postfachs.

</dd> <dt>

*TxtDomainName* \[ in, optional\]
</dt> <dd>

Der voll qualifizierte Daten Satz, für den txt-Ressourcen Einträge vorhanden sind.

</dd> <dt>

*RR* \[ Out, Ref\]
</dt> <dd>

Verweis auf das geänderte Objekt.

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

[**MicrosoftDNS- \_ rptype**](microsoftdns-rptype.md)
</dt> <dt>

[**Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ rptype-Klasse**](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





