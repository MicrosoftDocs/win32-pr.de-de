---
title: Modify-Methode der MicrosoftDNS_AAAAType Klasse
description: Die Modify-Methode aktualisiert einen Ressourcendatensatz der IPv6-Adresse (AAAA).
ms.assetid: d58f8a88-8473-4b26-89f0-237d2457f00b
keywords:
- Ändern der DNS-Methode
- Modify method DNS , MicrosoftDNS_AAAAType class
- MicrosoftDNS_AAAAType DNS-Klasse, Modify-Methode
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
ms.openlocfilehash: 417275b9e5fdf1c499f34fd49af3c40f8e208d43673a5d53dc9ba4c3b1ef2c95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967401"
---
# <a name="modify-method-of-the-microsoftdns_aaaatype-class"></a>Modify-Methode der MicrosoftDNS \_ AAAAType-Klasse

Die **Modify-Methode** aktualisiert einen Ressourcendatensatz der IPv6-Adresse (AAAA).

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

*TTL* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, die die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*IPv6Address* \[ in, optional\]
</dt> <dd>

IPv6-Adresse für den Host.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Verweis auf das neue -Objekt.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS \_ AAAAType**](microsoftdns-aaaatype.md)
</dt> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ AAAAType-Klasse**](microsoftdns-aaaatype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





