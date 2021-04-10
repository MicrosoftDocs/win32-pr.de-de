---
title: Modify-Methode der MicrosoftDNS_X25Type-Klasse
description: Die Modify-Methode aktualisiert einen X. 25 (x25)-Ressourcen Daten Satz.
ms.assetid: 2d82d67e-ae29-4ded-86fe-7db0ef5ed74f
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_X25Type-Klasse
- DNS-MicrosoftDNS_X25Type Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10db2fa770d3da8487a712e631c41fdd4256bf7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104409"
---
# <a name="modify-method-of-the-microsoftdns_x25type-class"></a>Modify-Methode der MicrosoftDNS \_ X25Type-Klasse

Die **Modify** -Methode aktualisiert einen X. 25 (x25)-Ressourcen Daten Satz.

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PSDNAddress,
  [out, ref]     MicrosoftDNS_X25Type &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Psdnaddress* \[ in, optional\]
</dt> <dd>

PSDN-Adresse des Besitzers der RR.

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

[**MicrosoftDNS \_ X25Type**](microsoftdns-x25type.md)
</dt> <dt>

[**Die Methode "kreateinzustancefrompropertydata" der X25Type-Klasse von MicrosoftDNS \_**](microsoftdns-x25type-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





