---
title: Modify-Methode der MicrosoftDNS_HINFOType-Klasse
description: Die Modify-Methode aktualisiert einen HINFO-Ressourceneintrag (Host Information).
ms.assetid: 8f8148f3-804f-4f99-8e79-606cd3cea660
keywords:
- Ändern der DNS-Methode
- Modify method DNS , MicrosoftDNS_HINFOType class
- MicrosoftDNS_HINFOType-Klasse DNS, Modify-Methode
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
ms.openlocfilehash: 344177f0e0a18da22294faef24a6d1c4e61598b4b5e8a804081bdd3a592cf440
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984640"
---
# <a name="modify-method-of-the-microsoftdns_hinfotype-class"></a>Modify-Methode der MicrosoftDNS \_ HINFOType-Klasse

Die **Modify-Methode** aktualisiert einen HINFO-Ressourceneintrag (Host Information).

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

*Gültigkeitsdauer* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, in der die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*CPU* \[ in, optional\]
</dt> <dd>

CPU-Typ des Datensatzbesitzers.

</dd> <dt>

*Betriebssystem* \[ in, optional\]
</dt> <dd>

Betriebssystem des Datensatzbesitzers.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MicrosoftDNS \_ HINFOType**](microsoftdns-hinfotype.md)
</dt> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ HINFOType-Klasse**](microsoftdns-hinfotype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





