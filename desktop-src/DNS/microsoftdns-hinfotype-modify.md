---
title: Modify-Methode der MicrosoftDNS_HINFOType-Klasse
description: Die Modify-Methode aktualisiert einen hinfo-Ressourcen Daten Satz (Host Information).
ms.assetid: 8f8148f3-804f-4f99-8e79-606cd3cea660
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_HINFOType-Klasse
- DNS-MicrosoftDNS_HINFOType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_HINFOType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29a01eb94d82d080142d3496bab5f7f0b9acac8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741545"
---
# <a name="modify-method-of-the-microsoftdns_hinfotype-class"></a>Modify-Methode der MicrosoftDNS- \_ hinfotype-Klasse

Die **Modify** -Methode aktualisiert einen hinfo-Ressourcen Daten Satz (Host Information).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] string                 CPU,
  [in, optional] string                 OS,
  [out, ref]     MicrosoftDNS_HINFOType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*CPU* \[ in, optional\]
</dt> <dd>

Der CPU-Typ des Daten Satz Besitzers.

</dd> <dt>

*Betriebssystem* \[ in, optional\]
</dt> <dd>

Das Betriebssystem des Daten Satz Besitzers.

</dd> <dt>

*RR* \[ Out, Ref\]
</dt> <dd>

Verweis auf das neue-Objekt.

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

[**MicrosoftDNS \_ hinfotype**](microsoftdns-hinfotype.md)
</dt> <dt>

[**Methode "kreateinstancefrompropertydata" der "hinfotype"-Klasse von MicrosoftDNS \_**](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





