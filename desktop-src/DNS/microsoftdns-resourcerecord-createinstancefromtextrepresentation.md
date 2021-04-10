---
title: Methode "kreateinzustancefromtextrepresentation" der MicrosoftDNS_ResourceRecord-Klasse
description: Die Methode "kreateinstancefromtextrepresentation" instanziiert ein MicrosoftDNS \_ resourcerecord-Objekt.
ms.assetid: 19600a9a-f75d-40ad-98e5-f81465d10f79
keywords:
- Methode "samateinzustancefromtextrepresentation" (DNS)
- Methode "-DNS", "MicrosoftDNS_ResourceRecord"-Klasse
- DNS-MicrosoftDNS_ResourceRecord Klasse, Methode "kreateinzustancefromtextrepresentation"
topic_type:
- apiref
api_name:
- MicrosoftDNS_ResourceRecord.CreateInstanceFromTextRepresentation
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a578d036180ecb1dc8a5e66bf853eec8845583f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040717"
---
# <a name="createinstancefromtextrepresentation-method-of-the-microsoftdns_resourcerecord-class"></a>Methode "kreateinzustancefromtextrepresentation" der MicrosoftDNS \_ resourcerecord-Klasse

Die Methode " **kreateinstancefromtextrepresentation** " instanziiert ein [**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md) -Objekt.

## <a name="syntax"></a>Syntax


```mof
void CreateInstanceFromTextRepresentation(
  [in]       string                      DnsServerName,
  [in]       string                      ContainerName,
  [in]       string                      TextRepresentation,
  [out, ref] MicrosoftDNS_ResourceRecord &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dnsservername* \[ in\]
</dt> <dd>

Der Name des DNS-Servers, auf dem die RR-Datei erstellt werden soll.

</dd> <dt>

*Containername* \[ in\]
</dt> <dd>

Der Name des Containers, in den das neue RR eingefügt werden soll.

</dd> <dt>

*Textrepresentation* \[ in\]
</dt> <dd>

Text Darstellung der zu erstellenden RR-Instanz.

</dd> <dt>

*RR* \[ Out, Ref\]
</dt> <dd>

Verweis auf den instanziierten RR.

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

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> <dt>

[**Getobjectbytextrepresentation-Methode der MicrosoftDNS \_ resourcerecord-Klasse**](microsoftdns-resourcerecord-getobjectbytextrepresentation.md)
</dt> </dl>

 

 





