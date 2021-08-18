---
title: Modify-Methode der MicrosoftDNS_RPType-Klasse
description: Mit der Modify-Methode wird ein Ressourcendatensatz für eine verantwortliche Person (Responsible Person, RP) aktualisiert.
ms.assetid: a779b905-922c-42ff-b3d9-318b3a848230
keywords:
- Ändern der DNS-Methode
- Modify method DNS , MicrosoftDNS_RPType class
- MicrosoftDNS_RPType-Klasse DNS, Modify-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_RPType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d237879b883e21c3c6289542e4eae7b9703be64931af788f042b6cdbec2ca49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587490"
---
# <a name="modify-method-of-the-microsoftdns_rptype-class"></a>Modify-Methode der MicrosoftDNS \_ RPType-Klasse

Mit der **Modify-Methode** wird ein Ressourcendatensatz für eine verantwortliche Person (Responsible Person, RP) aktualisiert.

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              RPMailbox,
  [in, optional] string              TXTDomainName,
  [out, ref]     MicrosoftDNS_RPType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gültigkeitsdauer* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, in der die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*RPMailbox* \[ in, optional\]
</dt> <dd>

FQDN, der das Postfach für die verantwortliche Person angibt.

</dd> <dt>

*TXTDomainName* \[ in, optional\]
</dt> <dd>

FQDN, für den TXT-Ressourceneinträge vorhanden sind.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MicrosoftDNS \_ RPType**](microsoftdns-rptype.md)
</dt> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ RPType-Klasse**](microsoftdns-rptype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





