---
title: Modify-Methode der MicrosoftDNS_MFType-Klasse
description: Die Modify-Methode aktualisiert einen e-Mail-Weiterleitungs-Agent für eine Domänen Ressource (MF).
ms.assetid: b4bc43a5-6f43-487d-ad6c-3e01d5b2b6b8
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_MFType-Klasse
- DNS-MicrosoftDNS_MFType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_MFType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec0a363290580c7cecf47dbe00c6dd7895d23dbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477841"
---
# <a name="modify-method-of-the-microsoftdns_mftype-class"></a>Modify-Methode der MicrosoftDNS \_ mftype-Klasse

Die **Modify** -Methode aktualisiert einen e-Mail-Weiterleitungs-Agent für eine Domänen Ressource (MF).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32              TTL,
  [in, optional] string              MFHost,
  [out, ref]     MicrosoftDNS_MFType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*MF-Host* \[ in, optional\]
</dt> <dd>

Der Name des Hosts, der den postweiterleitungs-Agent bereitstellt.

</dd> <dt>

*RR* \[ Out, Ref\]
</dt> <dd>

Verweis auf das geänderte Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Alle Parameter, die nicht angegeben sind, bleiben im geänderten Datensatz unverändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS- \_ mftype**](microsoftdns-mftype.md)
</dt> <dt>

[**Methode "kreateinzustancefrompropertydata" der MicrosoftDNS- \_ Klasse "mftype"**](microsoftdns-mftype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





