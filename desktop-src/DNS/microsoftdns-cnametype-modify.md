---
title: Modify-Methode der MicrosoftDNS_CNAMEType-Klasse
description: Die Modify-Methode aktualisiert einen kanonischen Namens Ressourcen Daten Satz (CNAME).
ms.assetid: 7e550026-d901-44a0-86ac-520682232ccb
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_CNAMEType-Klasse
- DNS-MicrosoftDNS_CNAMEType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_CNAMEType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ddbe1e1592c4331be808340c216954cd8d7b14f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476761"
---
# <a name="modify-method-of-the-microsoftdns_cnametype-class"></a>Modify-Methode der MicrosoftDNS \_ cnametype-Klasse

Die **Modify** -Methode aktualisiert einen kanonischen Namens Ressourcen Daten Satz (CNAME).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 PrimaryName,
  [out, ref]     MicrosoftDNS_CNAMEType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Primaryname* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die den primären Namen für den CNAME-Datensatz darstellt.

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

[**MicrosoftDNS \_ cnametype**](microsoftdns-cnametype.md)
</dt> <dt>

[**Die Methode "kreatinstancefrompropertydata" der MicrosoftDNS \_ cnametype-Klasse**](microsoftdns-cnametype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





