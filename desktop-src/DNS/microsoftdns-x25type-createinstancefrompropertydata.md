---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_X25Type-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen X. 25 (x25)-Ressourcen Eintrag.
ms.assetid: fe89f829-79b9-457e-b455-899b2706ef04
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_X25Type
- DNS-MicrosoftDNS_X25Type Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_X25Type.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f198bf7b843b5633acd0b1515e9e3573f5ebb55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040755"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_x25type-class"></a>Die Methode "kreateinzustancefrompropertydata" der X25Type-Klasse von MicrosoftDNS \_

Die Methode " **kreatinstancefrompropertydata** " instanziiert einen X. 25 (x25)-Ressourcen Eintrag.

## <a name="syntax"></a>Syntax


```mof
void CreateInstanceFromPropertyData(
  [in]           string               DnsServerName,
  [in]           string               ContainerName,
  [in]           string               OwnerName,
  [in, optional] uint32               RecordClass = 1,
  [in, optional] uint32               TTL,
  [in]           string               PSDNAddress,
  [out, ref]     MicrosoftDNS_X25Type &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dnsservername* \[ in\]
</dt> <dd>

Der voll qualifizierte Name oder die IP-Adresse des DNS-Servers, der diesen RR enthält.

</dd> <dt>

*Containername* \[ in\]
</dt> <dd>

Der Name des Containers für die Zone, den Cache oder die roothints-Instanz, die diese RR enthält.

</dd> <dt>

Besitzer *Name* \[ in\]
</dt> <dd>

Der Besitzer Name für die RR.

</dd> <dt>

*Recordclass* \[ in, optional\]
</dt> <dd>

Die Klasse von RR. Der Standardwert ist 1. Die folgenden Werte sind gültig.



| Wert                                                                                                | Bedeutung                  |
|------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | IN (Internet)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | CS (CSNET)<br/>    |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | CH (Chaos)<br/>    |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | HS (Hesiod)<br/>   |



 

</dd> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Psdnaddress* \[ in\]
</dt> <dd>

PSDN-Adresse des Besitzers der RR.

</dd> <dt>

*RR* \[ Out, Ref\]
</dt> <dd>

Verweis auf das neue-Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS \_ X25Type**](microsoftdns-x25type.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ X25Type-Klasse**](microsoftdns-x25type-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





