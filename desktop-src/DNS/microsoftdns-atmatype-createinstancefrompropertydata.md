---
title: Die Methode "kreateinzustancefrompropertydata" der MicrosoftDNS_ATMAType-Klasse
description: Die Methode "kreateinstancefrompropertydata" instanziiert einen Atma-Ressourcen Eintrag (ATM Address to Name).
ms.assetid: 0f3270fe-40d0-43f7-b4fc-95d96f9dd9f9
keywords:
- Methode "samateinzustancefrompropertydata" (DNS)
- Methode "-DNS", "MicrosoftDNS_ATMAType
- DNS-MicrosoftDNS_ATMAType Klasse, Methode "Methode"
topic_type:
- apiref
api_name:
- MicrosoftDNS_ATMAType.CreateInstanceFromPropertyData
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39fada3759e6384ae6f42a78bd132b9b8ad16f35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340333"
---
# <a name="createinstancefrompropertydata-method-of-the-microsoftdns_atmatype-class"></a>Methode "kreateinzustancefrompropertydata" der MicrosoftDNS \_ atmatype-Klasse

Die Methode " **kreateinstancefrompropertydata** " instanziiert einen Atma-Ressourcen Eintrag (ATM Address to Name).

## <a name="syntax"></a>Syntax


```mof
void CreateInstanceFromPropertyData(
  [in]           string                DnsServerName,
  [in]           string                ContainerName,
  [in]           string                OwnerName,
  [in, optional] uint32                RecordClass = 1,
  [in, optional] uint32                TTL,
  [in]           uint16                Format,
  [in]           string                ATMAddress,
  [out, ref]     MicrosoftDNS_ATMAType &RR
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

*Format* \[ in\]
</dt> <dd>

ATM-Adressformat. Zwei mögliche Werte für das Format sind: 0, was das AESA-Format (ATM End System Address) angibt, und 1 gibt das E. 164-Format an.

</dd> <dt>

*Atmaddress* \[ in\]
</dt> <dd>

Zeichenfolge mit variabler Länge von Oktetten, die die ATM-Adresse des Knotens bzw. Besitzers enthält, auf den sich diese RR bezieht. Die ersten vier Bytes des Arrays werden verwendet, um die Größe der Oktett-Zeichenfolge zu speichern. Das signifikanteste Byte wird in Byte 0 gespeichert.

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

[**MicrosoftDNS- \_ atmatype**](microsoftdns-atmatype.md)
</dt> <dt>

[**Modify-Methode der MicrosoftDNS \_ atmatype-Klasse**](microsoftdns-atmatype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





