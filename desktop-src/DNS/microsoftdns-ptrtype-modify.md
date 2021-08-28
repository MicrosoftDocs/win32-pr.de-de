---
title: Modify-Methode der MicrosoftDNS_PTRType Klasse
description: Die Modify-Methode aktualisiert einen Zeigerressourcendatensatz (PTR).
ms.assetid: 801a6bc9-e384-4912-a73a-6b04a1655002
keywords:
- Ändern der DNS-Methode
- Modify method DNS , MicrosoftDNS_PTRType class
- MicrosoftDNS_PTRType DNS-Klasse, Modify-Methode
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
ms.openlocfilehash: cbda85610e34fa6208bac5f8b9ba196be1b24fcadf8a53d87cea627718e9bd04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432823"
---
# <a name="modify-method-of-the-microsoftdns_ptrtype-class"></a>Modify-Methode der MicrosoftDNS \_ PTRType-Klasse

Die **Modify-Methode** aktualisiert einen Zeigerressourcendatensatz (PTR).

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

*TTL* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, die die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*PTRDomainName* \[ in, optional\]
</dt> <dd>

Domänennamenadresse des PTR-Eintrags.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Verweis auf das geänderte Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Nicht angegebene Parameter bleiben im geänderten Datensatz unverändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**MicrosoftDNS \_ PTRType**](microsoftdns-ptrtype.md)
</dt> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ PTRType-Klasse**](microsoftdns-ptrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





