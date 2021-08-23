---
title: Modify-Methode der MicrosoftDNS_WKSType Klasse
description: Die Modify-Methode aktualisiert einen Well-Known Services -Ressourcendatensatz (WKS).
ms.assetid: 3a9100eb-dc90-45bb-9739-14026da100fd
keywords:
- Ändern der DNS-Methode
- Modify method DNS , MicrosoftDNS_WKSType class
- MicrosoftDNS_WKSType DNS-Klasse, Modify-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_WKSType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d6f58a71b7d3a3237a744d42c90bc437714ed50553639253bafb0b2b9fb2977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692238"
---
# <a name="modify-method-of-the-microsoftdns_wkstype-class"></a>Modify-Methode der MicrosoftDNS \_ WKSType-Klasse

Die **Modify-Methode** aktualisiert einen Well-Known Services -Ressourcendatensatz (WKS).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32               TTL,
  [in, optional] uint32               InternetAddress,
  [in, optional] uint8                IPProtocol,
  [in, optional] uint8                Services,
  [out, ref]     MicrosoftDNS_WKSType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TTL* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, die die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*InternetAddress* \[ in, optional\]
</dt> <dd>

Internet-IP-Adresse für den Besitzer des Datensatzes.

</dd> <dt>

*IPProtocol* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die das IP-Protokoll für diesen Datensatz darstellt. Gültige Werte sind UDP oder TCP.

</dd> <dt>

*Dienste* \[ in, optional\]
</dt> <dd>

Eine Zeichenfolge, die alle dienste enthält, die vom WKS-Datensatz (Well Known Service) verwendet werden.

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

[**MicrosoftDNS \_ WKSType**](microsoftdns-wkstype.md)
</dt> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ WKSType-Klasse**](microsoftdns-wkstype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





