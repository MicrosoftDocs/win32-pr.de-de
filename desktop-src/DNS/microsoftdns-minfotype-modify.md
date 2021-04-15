---
title: Modify-Methode der MicrosoftDNS_MINFOType-Klasse
description: Die Modify-Methode aktualisiert einen Ressourcen Daten Satz für e-Mail-Informationen (MINFO).
ms.assetid: fbec0cd3-f735-44c6-b010-80f35cc33d98
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_MINFOType-Klasse
- DNS-MicrosoftDNS_MINFOType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b59d7d1231ed88e61a0ecf94cef50041ca772f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475882"
---
# <a name="modify-method-of-the-microsoftdns_minfotype-class"></a>Modify-Methode der MicrosoftDNS- \_ minfotype-Klasse

Die **Modify** -Methode aktualisiert einen Ressourcen Daten Satz für e-Mail-Informationen (MINFO).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 ResponsibleMailbox,
  [in, optional] string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

" *Verantworblemailbox* \[ " in, optional\]
</dt> <dd>

Der voll qualifizierte Name ist ein Postfach, das für die Mailingliste oder das Postfach zuständig ist, die im Besitzer Namen des Datensatzes angegeben sind.

</dd> <dt>

*Errormailbox* \[ in, optional\]
</dt> <dd>

FQDN, der ein Postfach für den Empfang von Fehlermeldungen in Bezug auf die Mailingliste oder das Postfach angibt, das durch den Besitzer Namen des MINFO-Datensatzes angegeben wird.

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

[**MicrosoftDNS- \_ minfotype**](microsoftdns-minfotype.md)
</dt> <dt>

[**Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ minfotype-Klasse**](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





