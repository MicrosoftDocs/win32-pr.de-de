---
title: Modify-Methode der MicrosoftDNS_AFSDBType-Klasse
description: Die Modify-Methode aktualisiert einen Ressourcen Daten Satz für den Andrew File System Database Server (AFSDB).
ms.assetid: 9b98a3cf-cc2b-4497-921b-eaca4d13d6a1
keywords:
- DNS-Methode ändern
- Modify-Methode (DNS), MicrosoftDNS_AFSDBType-Klasse
- DNS-MicrosoftDNS_AFSDBType Klasse, Methode ändern
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
ms.openlocfilehash: 4752910ab9e8117bfdaf27f93d32be3377158ba5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339155"
---
# <a name="modify-method-of-the-microsoftdns_afsdbtype-class"></a>Modify-Methode der MicrosoftDNS \_ afsdbtype-Klasse

Die **Modify** -Methode aktualisiert einen Ressourcen Daten Satz für den Andrew File System Database Server (AFSDB).

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

Gültigkeitsdauer  \[ in, optional\]
</dt> <dd>

Zeit (in Sekunden), die der RR von einem DNS-Resolver zwischengespeichert werden kann.

</dd> <dt>

*Untertyp* \[ in, optional\]
</dt> <dd>

Der Untertyp des Host-AFS-Servers. Für den Untertyp 1 (Wert = 1) verfügt der Host über einen mespeicherort-Server der Version 3,0 für die benannte AFS-Zelle. Im Fall von Untertyp 2 (Wert = 2) verfügt der Host über einen authentifizierten Namen Server, der den Zellen Stammverzeichnis-Knoten für die benannte DCE/NCA-Zelle enthält.

</dd> <dt>

*Servername* \[ in, optional\]
</dt> <dd>

Ein voll qualifizierter Host, der einen Host mit einem Server für die im Besitzer Namen angegebene AFS-Zelle angibt.

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

[**MicrosoftDNS \_ afsdbtype**](microsoftdns-afsdbtype.md)
</dt> <dt>

[**Die Methode "kreateinstancefrompropertydata" der MicrosoftDNS- \_ afsdbtype-Klasse**](microsoftdns-afsdbtype-createinstancefrompropertydata.md)
</dt> <dt>

[**MicrosoftDNS \_ resourcerecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





