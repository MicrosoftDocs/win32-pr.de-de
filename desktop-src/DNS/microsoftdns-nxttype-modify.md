---
title: Modify-Methode der MicrosoftDNS_NXTType-Klasse
description: Mit der Modify-Methode wird ein Next-Ressourceneintrag (NXT) aktualisiert.
ms.assetid: 5a21b843-0761-4022-b00a-9dbcd6814454
keywords:
- Ändern der DNS-Methode
- Modify method DNS , MicrosoftDNS_NXTType class
- MicrosoftDNS_NXTType-Klasse DNS, Modify-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_NXTType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e43082ff829a7b8701701e9b099aa0f36d274879bfb6f281272096558f1c8bd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163201"
---
# <a name="modify-method-of-the-microsoftdns_nxttype-class"></a>Modify-Methode der MicrosoftDNS \_ NXTType-Klasse

Mit **der Modify-Methode** wird ein Next-Ressourceneintrag (NXT) aktualisiert.

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in]           string               NextDomainName,
  [in]           string               Types,
  [out, ref]     MicrosoftDNS_NXTType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gültigkeitsdauer* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, in der die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*NextDomainName* \[ In\]
</dt> <dd>

Nächster Domänenname.

</dd> <dt>

*Typen* \[ In\]
</dt> <dd>

Durch Leerzeichen getrennte Liste der Mnemonics vom RR-Typ für den Besitzernamen des NXT-Ressourcendatensatzes.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS \_ NXTType**](microsoftdns-nxttype.md)
</dt> <dt>

[**CreateInstanceFromPropertyData-Methode der \_ MicrosoftDNS-NXTType-Klasse**](microsoftdns-nxttype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





