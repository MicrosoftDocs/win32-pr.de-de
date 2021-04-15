---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_MDType-Klasse
description: Die Methode "kreatinstancefrompropertydata" instanziiert einen e-Mail-Agent für eine Domänen Ressource (MD).
ms.assetid: 23155a49-e2b3-4a69-8572-5dee61019d8f
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_MDType
- DNS-MicrosoftDNS_MDType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_MDType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b2e2cfdf3d2bb4b853a8e32716e51ca8e4c5b8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476602"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_mdtype-class"></a>Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ mdtype-Klasse

Die Methode " **kreatinstancefrompropertydata** " instanziiert einen e-Mail-Agent für eine Domänen Ressource (MD).

## <a name="syntax"></a>Syntax


```mof
void CreateInstanceFromPropertyData(
  [in]           string              DnsServerName,
  [in]           string              ContainerName,
  [in]           string              OwnerName,
  [in, optional] uint32              RecordClass = 1,
  [in, optional] uint32              TTL,
  [in]           string              MDHost,
  [out, ref]     MicrosoftDNS_MDType &RR
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

*Mdhost* \[ in\]
</dt> <dd>

Hostname der Mail Übermittlung.

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

[**MicrosoftDNS- \_ mdtype**](microsoftdns-mdtype.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS- \_ mdtype-Klasse**](microsoftdns-mdtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





