---
title: Modify-Methode der MicrosoftDNS_NSType-Klasse
description: Die Modify-Methode aktualisiert einen Name Server (NS)-Ressourcen Daten Satz.
ms.assetid: da625231-cf4e-4526-b713-737e6b9f5831
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_NSType-Klasse
- DNS-MicrosoftDNS_NSType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_NSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3dd26b7c0f1c31ef3ea742f20f70df8646a087b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479401"
---
# <a name="modify-method-of-the-microsoftdns_nstype-class"></a>Modify-Methode der MicrosoftDNS- \_ nstype-Klasse

Die **Modify** -Methode aktualisiert einen Name Server (NS)-Ressourcen Daten Satz.

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              NSHost,
  [out, ref]     MicrosoftDNS_NSType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*NSHost* \[ in, optional\]
</dt> <dd>

Autorisierender Host für die Domäne.

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

 

 





