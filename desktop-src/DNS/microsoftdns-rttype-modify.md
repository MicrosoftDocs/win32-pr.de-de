---
title: Modify-Methode der MicrosoftDNS_RTType-Klasse
description: Die Modify-Methode aktualisiert einen Route-through-Ressourcen Daten Satz (RT).
ms.assetid: 80053ae6-8ce8-4aa1-be2b-aac9daa5dae3
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_RTType-Klasse
- DNS-MicrosoftDNS_RTType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_RTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8267bf1dc256ec95a456978643226ab5c01af93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517939"
---
# <a name="modify-method-of-the-microsoftdns_rttype-class"></a>Modify-Methode der MicrosoftDNS \_ rttype-Klasse

Die **Modify** -Methode aktualisiert einen Route-through-Ressourcen Daten Satz (RT).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              IntermediateHost,
  [out, ref]     MicrosoftDNS_RTType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Bevorzugen* \[ in, optional\]
</dt> <dd>

Die Einstellung, die diesem RR unter anderem beim gleichen Besitzer zugewiesen wird. Niedrigere Werte werden bevorzugt.

</dd> <dt>

*Intermediatehost* \[ in, optional\]
</dt> <dd>

FQDN, der einen Host angibt, der als zwischengeschalteter Host zum Erreichen des vom Besitzer angegebenen Hosts dienen soll.

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

[**MicrosoftDNS- \_ rttype**](microsoftdns-rttype.md)
</dt> <dt>

[**Methode "kreateinzustancefrompropertydata" der Klasse "MicrosoftDNS \_ rttype"**](microsoftdns-rttype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





