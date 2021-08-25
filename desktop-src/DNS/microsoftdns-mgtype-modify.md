---
title: Modify-Methode der MicrosoftDNS_MGType-Klasse
description: Mit der Modify-Methode wird ein Ressourceneintrag für eine E-Mail-Gruppe (MG) aktualisiert.
ms.assetid: c7d42964-19fb-410d-a434-85af20754e20
keywords:
- Ändern der DNS-Methode
- Modify method DNS , MicrosoftDNS_MGType class
- MicrosoftDNS_MGType-Klasse DNS, Modify-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_MGType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db26f33e56ecc8553af1e34513a085b6eb6666ca99e2f91ec19383756094d6f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874910"
---
# <a name="modify-method-of-the-microsoftdns_mgtype-class"></a>Modify-Methode der MicrosoftDNS \_ MGType-Klasse

Mit **der Modify-Methode** wird ein Ressourceneintrag für eine E-Mail-Gruppe (MG) aktualisiert.

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MGMailbox,
  [out, ref]     MicrosoftDNS_MGType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gültigkeitsdauer* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, in der die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*MGMailbox* \[ in, optional\]
</dt> <dd>

FQDN, der ein Postfach angibt, das Mitglied der E-Mail-Gruppe ist, die durch den Besitzernamen des Datensatzes angegeben wird.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Verweis auf das geänderte Objekt.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS \_ MGType**](microsoftdns-mgtype.md)
</dt> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ MGType-Klasse**](microsoftdns-mgtype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





