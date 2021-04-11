---
title: Modify-Methode der MicrosoftDNS_MGType-Klasse
description: Die Modify-Methode aktualisiert einen e-Mail-Gruppen Ressourcen-Datensatz (mg).
ms.assetid: c7d42964-19fb-410d-a434-85af20754e20
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_MGType-Klasse
- DNS-MicrosoftDNS_MGType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 706502569687a3c035c943e0a9dcc04aa1732492
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104738"
---
# <a name="modify-method-of-the-microsoftdns_mgtype-class"></a>Modify-Methode der MicrosoftDNS- \_ mgtype-Klasse

Die **Modify** -Methode aktualisiert einen e-Mail-Gruppen Ressourcen-Datensatz (mg).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Mgmailbox* \[ in, optional\]
</dt> <dd>

FQDN, der ein Postfach angibt, das Mitglied der durch den Besitzer Namen des Datensatzes angegebenen e-Mail-Gruppe ist.

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

[**MicrosoftDNS- \_ mgtype**](microsoftdns-mgtype.md)
</dt> <dt>

[**Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ mgtype-Klasse**](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





