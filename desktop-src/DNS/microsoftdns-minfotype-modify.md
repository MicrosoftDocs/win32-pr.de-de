---
title: Modify-Methode der MicrosoftDNS_MINFOType Klasse
description: Die Modify-Methode aktualisiert einen MINFO-Ressourcendatensatz (Mail Information).
ms.assetid: fbec0cd3-f735-44c6-b010-80f35cc33d98
keywords:
- Ändern der DNS-Methode
- Modify method DNS , MicrosoftDNS_MINFOType class
- MicrosoftDNS_MINFOType DNS-Klasse, Modify-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_MINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 954015ffdb01a8655a7762d3c364abe3440a8cfd19ec7eabf5ad8db5cf11c8c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692560"
---
# <a name="modify-method-of-the-microsoftdns_minfotype-class"></a>Modify-Methode der MicrosoftDNS \_ MINFOType-Klasse

Die **Modify-Methode** aktualisiert einen MINFO-Ressourcendatensatz (Mail Information).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 ResponsibleMailbox,
  [in, optional] string                 ErrorMailbox,
  [out, ref]     MicrosoftDNS_MINFOType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TTL* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, die die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*ResponsibleMailbox* \[ in, optional\]
</dt> <dd>

FQDN, der ein Postfach an, das für die Adressenliste oder das Postfach zuständig ist, die im Besitzernamen des Datensatzes angegeben ist.

</dd> <dt>

*ErrorMailbox* \[ in, optional\]
</dt> <dd>

FQDN, der ein Postfach zum Empfangen von Fehlermeldungen im Zusammenhang mit der Adressenliste oder dem Postfach an, das durch den Besitzernamen des MINFO-Datensatzes angegeben wird.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS \_ MINFOType**](microsoftdns-minfotype.md)
</dt> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ MINFOType-Klasse**](microsoftdns-minfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





