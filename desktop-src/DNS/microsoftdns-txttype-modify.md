---
title: Modify-Methode der MicrosoftDNS_TXTType-Klasse
description: Die Modify-Methode aktualisiert einen Textressourceneintrag (TXT).
ms.assetid: af61057e-95be-4290-83da-a63f01ead476
keywords:
- Ändern der DNS-Methode
- Modify method DNS , MicrosoftDNS_TXTType class
- MicrosoftDNS_TXTType-Klasse DNS, Modify-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_TXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e565d4c48b048b4d72b11c939b644752cb14f1993c2810f127bb14f60bec929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957299"
---
# <a name="modify-method-of-the-microsoftdns_txttype-class"></a>Modify-Methode der MicrosoftDNS \_ TXTType-Klasse

Die **Modify-Methode** aktualisiert einen Textressourceneintrag (TXT).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               DescriptiveText,
  [out, ref]     MicrosoftDNS_TXTType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gültigkeitsdauer* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, in der die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*DescriptiveText* \[ In\]
</dt> <dd>

Beschreibender Text, dessen Semantik von der Besitzerdomäne abhängt.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Verweis auf das neue Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Alle nicht angegebenen Parameter bleiben im geänderten Datensatz unverändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\Stamm-MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MicrosoftDNS \_ TXTType**](microsoftdns-txttype.md)
</dt> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ TXTType-Klasse**](microsoftdns-txttype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





