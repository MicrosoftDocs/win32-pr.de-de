---
title: Modify-Methode der MicrosoftDNS_WINSRType-Klasse
description: Die Modify-Methode aktualisiert einen WINS-Ressourcen Daten Satz (Reverse-Suche).
ms.assetid: 28be0045-5b0d-4434-a2a9-b56191f1e213
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_WINSRType-Klasse
- DNS-MicrosoftDNS_WINSRType Klasse, Methode ändern
topic_type:
- apiref
api_name:
- MicrosoftDNS_WINSRType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02d89c3cd191262136035f9006853e2f1a7f7dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105933"
---
# <a name="modify-method-of-the-microsoftdns_winsrtype-class"></a>Modify-Methode der MicrosoftDNS \_ winsrtype-Klasse

Die **Modify** -Methode aktualisiert einen WINS-Ressourcen Daten Satz (Reverse-Suche).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint32                 MappingFlag,
  [in, optional] uint32                 LookupTimeout,
  [in, optional] uint32                 CacheTimeout,
  [in, optional] string                 ResultDomain,
  [out, ref]     MicrosoftDNS_WINSRType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Mappingflag* \[ in, optional\]
</dt> <dd>

Das WINSR-ZuordnungsFlag, das angibt, ob der Datensatz in die Zonen Replikation eingeschlossen werden muss. Sie kann nur zwei Werte aufweisen: 0x80000000 und 0x00010000 bis, die den Replikations-und No-Replication-Flags (local Record) entsprechen.

</dd> <dt>

*Lookuptimeout* \[ in, optional\]
</dt> <dd>

Timeout (in Sekunden) für einen DNS-Server mit umgekehrter WINS-Suche.

</dd> <dt>

*Cachetimeout* \[ in, optional\]
</dt> <dd>

Die Zeit in Sekunden, in der ein DNS-Server mit WINS-Suche die Antwort des WINS-Servers zwischenspeichern kann.

</dd> <dt>

*Resultdomain* \[ in, optional\]
</dt> <dd>

Domänen Name, der an zurückgegebene NetBIOS-Namen angehängt werden soll.

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

[**MicrosoftDNS \_ winsrtype**](microsoftdns-winsrtype.md)
</dt> <dt>

[**Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ Klasse "winsrtype"**](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





