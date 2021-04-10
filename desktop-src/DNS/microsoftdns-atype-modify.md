---
title: Modify-Methode der MicrosoftDNS_AType-Klasse
description: Die Modify-Methode aktualisiert die Gültigkeitsdauer und die IP-Adresse eines Ressourcen Datensatzes für die Host Adresse (a).
ms.assetid: fe01549d-7135-499d-a5a5-cd31ea106f53
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_AType-Klasse
- DNS-MicrosoftDNS_AType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffda093ed843cfd655711100321c9876120519c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040619"
---
# <a name="modify-method-of-the-microsoftdns_atype-class"></a>Modify-Methode der MicrosoftDNS- \_ atyp-Klasse

Die **Modify** -Methode aktualisiert die Gültigkeitsdauer und die IP-Adresse eines Ressourcen Datensatzes für die Host Adresse (a).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32             TTL,
  [in, optional] string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*IPAddress* \[ in, optional\]
</dt> <dd>

Zeichenfolge, die die IP-Adresse des Hosts darstellt.

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

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Methode "kreateinzustancefrompropertydata" der Klasse "MicrosoftDNS \_ aType"**](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> </dl>

 

 





