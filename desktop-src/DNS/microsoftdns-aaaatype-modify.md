---
title: Modify-Methode der MicrosoftDNS_AAAAType-Klasse
description: Die Modify-Methode aktualisiert einen Ressourcen Daten Satz der IPv6-Adresse (AAAA).
ms.assetid: d58f8a88-8473-4b26-89f0-237d2457f00b
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_AAAAType-Klasse
- DNS-MicrosoftDNS_AAAAType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_AAAAType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc216233fe3d41e4f1e31fe0d471e766c4dc8476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858906"
---
# <a name="modify-method-of-the-microsoftdns_aaaatype-class"></a>Modify-Methode der MicrosoftDNS \_ aaaatype-Klasse

Die **Modify** -Methode aktualisiert einen Ressourcen Daten Satz der IPv6-Adresse (AAAA).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                IPv6Address,
  [out, ref]     MicrosoftDNS_AAAAType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*IPv6Address* \[ in, optional\]
</dt> <dd>

IPv6-Adresse für den Host.

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

[**MicrosoftDNS \_ aaaatype**](microsoftdns-aaaatype.md)
</dt> <dt>

[**Methode "kreateinzustancefrompropertydata" der Klasse "MicrosoftDNS \_ aaaatype"**](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





