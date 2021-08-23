---
title: Modify-Methode der MicrosoftDNS_WINSRType-Klasse
description: Die Modify-Methode aktualisiert einen WINSR-Ressourceneintrag (Reverse Look up).
ms.assetid: 28be0045-5b0d-4434-a2a9-b56191f1e213
keywords:
- Ändern der DNS-Methode
- Modify method DNS , MicrosoftDNS_WINSRType class
- MicrosoftDNS_WINSRType-Klasse DNS, Modify-Methode
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
ms.openlocfilehash: 9db7865110b0e79642dc91671094c06dfbd10e07cd89684dab58623a9456cca9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076664"
---
# <a name="modify-method-of-the-microsoftdns_winsrtype-class"></a>Modify-Methode der MicrosoftDNS \_ WINSRType-Klasse

Die **Modify-Methode** aktualisiert einen WINSR-Ressourceneintrag (Reverse Look up).

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

*Gültigkeitsdauer* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, in der die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*MappingFlag* \[ in, optional\]
</dt> <dd>

WINSR-Zuordnungsflag, das angibt, ob der Datensatz in die Zonenreplikation eingeschlossen werden muss. Sie kann nur zwei Werte aufweisen: 0x80000000 und 0x00010000 entsprechend den Replikationsflags bzw. Flags ohne Replikation (lokaler Datensatz).

</dd> <dt>

*LookupTimeout* \[ in, optional\]
</dt> <dd>

Time out in Sekunden für einen DNS-Server mit WINS Reverse Look up.

</dd> <dt>

*CacheTimeout* \[ in, optional\]
</dt> <dd>

Die Zeit in Sekunden, die ein DNS-Server mit WINS-Suche verwendet, kann die Antwort des WINS-Servers zwischenspeichern.

</dd> <dt>

*ResultDomain* \[ in, optional\]
</dt> <dd>

Domänenname, der an zurückgegebene NetBIOS-Namen angefügt werden soll.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS \_ WINSRType**](microsoftdns-winsrtype.md)
</dt> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ WINSRType-Klasse**](microsoftdns-winsrtype-createinstancefrompropertydata.md)
</dt> <dt>

[**\_MicrosoftDNS-RessourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





