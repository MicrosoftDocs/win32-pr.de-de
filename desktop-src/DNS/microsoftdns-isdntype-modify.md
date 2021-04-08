---
title: Modify-Methode der MicrosoftDNS_ISDNType-Klasse
description: Die Modify-Methode aktualisiert einen ISDN-Ressourcen Daten Satz.
ms.assetid: 09e23853-ca92-43a3-8bd9-7de10eb5eddc
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_ISDNType-Klasse
- DNS-MicrosoftDNS_ISDNType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_ISDNType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c369a6650c834ff9f35af6389c346daec86a954
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949445"
---
# <a name="modify-method-of-the-microsoftdns_isdntype-class"></a>Modify-Methode der MicrosoftDNS- \_ isdntype-Klasse

Die **Modify** -Methode aktualisiert einen ISDN-Ressourcen Daten Satz.

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32                TTL,
  [in, optional] string                ISDNNumber,
  [in, optional] string                SubAddress,
  [out, ref]     MicrosoftDNS_ISDNType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Isdnnumber* \[ in, optional\]
</dt> <dd>

ISDN-Nummer und DDI für den Besitzer des Datensatzes.

</dd> <dt>

*Unter Adresse* \[ in, optional\]
</dt> <dd>

Die untergeordnete Adresse des Besitzers, sofern definiert.

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

[**MicrosoftDNS \_ isdntype**](microsoftdns-isdntype.md)
</dt> <dt>

[**Die Methode "kreateinstancefrompropertydata" der Klasse "MicrosoftDNS \_ isdntype"**](microsoftdns-isdntype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





