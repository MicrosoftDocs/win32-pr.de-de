---
title: Modify-Methode der MicrosoftDNS_MDType-Klasse
description: Die Modify-Methode aktualisiert einen Mail-Agent für die Domäne (MD)-Ressourcen Daten Satz.
ms.assetid: d14c8ada-d715-489f-9956-a940b94006e5
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_MDType-Klasse
- DNS-MicrosoftDNS_MDType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78ed5e3a8d7f819447d256ba3bce31f4eaa6986a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103610"
---
# <a name="modify-method-of-the-microsoftdns_mdtype-class"></a>Modify-Methode der MicrosoftDNS- \_ mdtype-Klasse

Die **Modify** -Methode aktualisiert einen Mail-Agent für die Domäne (MD)-Ressourcen Daten Satz.

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MDHost,
  [out, ref]     MicrosoftDNS_MDType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Mdhost* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die den Mail Übermittlungs Host darstellt.

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

[**MicrosoftDNS- \_ mdtype**](microsoftdns-mdtype.md)
</dt> <dt>

[**Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ mdtype-Klasse**](microsoftdns-mdtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





