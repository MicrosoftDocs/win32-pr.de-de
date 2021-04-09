---
title: Modify-Methode der MicrosoftDNS_PTRType-Klasse
description: Die Modify-Methode aktualisiert einen Zeiger (PTR)-Ressourcen Daten Satz.
ms.assetid: 801a6bc9-e384-4912-a73a-6b04a1655002
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_PTRType-Klasse
- DNS-MicrosoftDNS_PTRType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_PTRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 840bf100ea5cdbbb606837e90d8fa9fcebab57fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956623"
---
# <a name="modify-method-of-the-microsoftdns_ptrtype-class"></a>Modify-Methode der MicrosoftDNS \_ ptrtype-Klasse

Die **Modify** -Methode aktualisiert einen Zeiger (PTR)-Ressourcen Daten Satz.

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] string               PTRDomainName,
  [out, ref]     MicrosoftDNS_PTRType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Ptrdomainname* \[ in, optional\]
</dt> <dd>

Die Domänen Namen Adresse des PTR-Einsatzes.

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

[**MicrosoftDNS \_ ptrtype**](microsoftdns-ptrtype.md)
</dt> <dt>

[**Die Methode "kreateinstancefrompropertydata" der Klasse "MicrosoftDNS \_ ptrtype"**](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





