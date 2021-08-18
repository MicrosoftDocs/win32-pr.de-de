---
title: Modify-Methode der MicrosoftDNS_AType Klasse
description: Mit der Modify-Methode werden die Tl und die IP-Adresse eines Ressourcendatensatzes der Hostadresse (A) aktualisiert.
ms.assetid: fe01549d-7135-499d-a5a5-cd31ea106f53
keywords:
- Ändern der DNS-Methode
- Modify method DNS , MicrosoftDNS_AType class
- MicrosoftDNS_AType DNS-Klasse, Modify-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_AType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d9f4740aeec92726796943e53b4d2143a6378341b061aaa7d3f3f6bf6dc7d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163481"
---
# <a name="modify-method-of-the-microsoftdns_atype-class"></a>Modify-Methode der MicrosoftDNS \_ AType-Klasse

Mit **der Modify-Methode** werden die Tl und die IP-Adresse eines Ressourcendatensatzes der Hostadresse (A) aktualisiert.

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32             TTL,
  [in, optional] string             IPAddress,
  [out, ref]     MicrosoftDNS_AType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TTL* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, die die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*IPAddress* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die die IP-Adresse des Hosts darstellt.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ AType-Klasse**](microsoftdns-atype-createinstancefrompropertydata.md)
</dt> </dl>

 

 





