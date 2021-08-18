---
title: Modify-Methode der MicrosoftDNS_AFSDBType Klasse
description: Die Modify-Methode aktualisiert einen Ressourcendatensatz des Andrew File System Database Server (AFSDB).
ms.assetid: 9b98a3cf-cc2b-4497-921b-eaca4d13d6a1
keywords:
- Ändern der DNS-Methode
- Modify method DNS , MicrosoftDNS_AFSDBType class
- MicrosoftDNS_AFSDBType DNS-Klasse, Modify-Methode
topic_type:
- apiref
api_name:
- MicrosoftDNS_AFSDBType.Modify
api_location:
- Root\MicrosoftDNS
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 385b80d853c3b610971803c0b1d80a81b7b7c2335186fe4585e63f60c3e3cca3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104060"
---
# <a name="modify-method-of-the-microsoftdns_afsdbtype-class"></a>Modify-Methode der MicrosoftDNS \_ AFSDBType-Klasse

Die **Modify-Methode** aktualisiert einen Ressourcendatensatz des Andrew File System Database Server (AFSDB).

## <a name="syntax"></a>Syntax


```mof
void Modify(
  [in, optional] uint32                 TTL,
  [in, optional] uint16                 Subtype,
  [in, optional] string                 ServerName,
  [out, ref]     MicrosoftDNS_AFSDBType &RR
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*TTL* \[ in, optional\]
</dt> <dd>

Zeit in Sekunden, die die RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Untertyp* \[ in, optional\]
</dt> <dd>

Untertyp des AFS-Hostservers. Für Untertyp 1 (Wert=1) verfügt der Host über einen Volumespeicherortserver der AFS-Version 3.0 für die benannte AFS-Zelle. Im Fall von Untertyp 2 (Wert =2) verfügt der Host über einen authentifizierten Namenserver, der den Zellenstammverzeichnisknoten für die benannte DCE/NCA-Zelle enthält.

</dd> <dt>

*ServerName* \[ in, optional\]
</dt> <dd>

FQDN, der einen Host an gibt, der über einen Server für die AFS-Zelle verfügt, die im Besitzernamen angegeben ist.

</dd> <dt>

*RR* \[ out, ref\]
</dt> <dd>

Verweis auf das geänderte Objekt.

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

[**MicrosoftDNS \_ AFSDBType**](microsoftdns-afsdbtype.md)
</dt> <dt>

[**CreateInstanceFromPropertyData-Methode der MicrosoftDNS \_ AFSDBType-Klasse**](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





