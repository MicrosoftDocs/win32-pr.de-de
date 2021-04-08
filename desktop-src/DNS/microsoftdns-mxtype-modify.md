---
title: Modify-Methode der MicrosoftDNS_MXType-Klasse
description: Die Modify-Methode aktualisiert einen e-Mail-Austausch Ressourcen Daten Satz (Mr).
ms.assetid: 40267ac9-0392-4e08-a5d2-145ee9639c39
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_MXType-Klasse
- DNS-MicrosoftDNS_MXType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_MXType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a665d0673e048eff684b4c985b54a1c57e030a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957143"
---
# <a name="modify-method-of-the-microsoftdns_mxtype-class"></a>Modify-Methode der MicrosoftDNS- \_ mxtype-Klasse

Die **Modify** -Methode aktualisiert einen e-Mail-Austausch Ressourcen Daten Satz (Mr).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] uint16              Preference,
  [in, optional] string              MailExchange,
  [out, ref]     MicrosoftDNS_MXType &RR
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

*Mailexchange* \[ in, optional\]
</dt> <dd>

FQDN, der einen Host angibt, der als e-Mail-Austausch für den Namen des Besitzers fungieren soll.

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

[**MicrosoftDNS- \_ mxtype**](microsoftdns-mxtype.md)
</dt> <dt>

[**Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ mxtype-Klasse**](microsoftdns-mxtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





