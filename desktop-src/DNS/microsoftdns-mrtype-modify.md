---
title: Modify-Methode der MicrosoftDNS_MRType-Klasse
description: Die Modify-Methode aktualisiert einen Ressourcen Daten Satz für Post Fach Umbenennungen (Mr).
ms.assetid: eb833735-d485-4603-9976-305244537acd
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_MRType-Klasse
- DNS-MicrosoftDNS_MRType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_MRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 996692301e8446b3fd67e20eca036cd085e83b03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476593"
---
# <a name="modify-method-of-the-microsoftdns_mrtype-class"></a>Modify-Methode der MicrosoftDNS- \_ mrtype-Klasse

Die **Modify** -Methode aktualisiert einen Ressourcen Daten Satz für Post Fach Umbenennungen (Mr).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in]           string              MRMailbox,
  [out, ref]     MicrosoftDNS_MRType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Mrmailbox* \[ in\]
</dt> <dd>

Der voll qualifizierte Name des Postfachs, bei dem es sich um den ordnungsgemäßen Umbenennen des im Namen des Datensatzes angegebenen Postfachs handelt

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

[**MicrosoftDNS- \_ mrtype**](microsoftdns-mrtype.md)
</dt> <dt>

[**Methode "kreateinstancefrompropertydata" der Klasse "MicrosoftDNS \_ mrtype"**](microsoftdns-mrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





