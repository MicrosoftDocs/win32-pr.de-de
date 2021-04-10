---
title: MicrosoftDNS_Cache-Klasse
description: Die MicrosoftDNS- \_ Cache Klasse beschreibt einen Cache, der auf einem DNS-Server vorhanden ist.
ms.assetid: 139406eb-70f2-4614-9662-703ada032298
keywords:
- DNS-MicrosoftDNS_Cache Klasse
- DNS-MicrosoftDNS_Cache Klasse, beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_Cache
- MicrosoftDNS_Cache.ClearCache
- MicrosoftDNS_Cache.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e55bda9c38d889fe1b84ef28432b18e5724af09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040618"
---
# <a name="microsoftdns_cache-class"></a>MicrosoftDNS- \_ Cache Klasse

Die **MicrosoftDNS- \_ Cache** Klasse beschreibt einen Cache, der auf einem DNS-Server vorhanden ist. Diese Klasse vereinfacht die Visualisierung der Kapselung von DNS-Objekten, anstatt ein reales Objekt darzustellen. Die **MicrosoftDNS- \_ Cache** Klasse ist ein Container für die Ressourcen Datensätze, die vom DNS-Server zwischengespeichert werden. Verwechseln Sie dies nicht mit einer Cache Datei, die Root-Hinweise enthält.

Jede Instanz der **MicrosoftDNS \_** -Klasse muss genau einem DNS-Server zugewiesen werden. Sie ist möglicherweise mehreren Instanzen der [**MicrosoftDNS- \_ Domäne**](microsoftdns-domain.md) oder der [**MicrosoftDNS- \_ resourcerecord**](microsoftdns-resourcerecord.md) -Klasse zugeordnet.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_Cache : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS- \_ Cache** Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS- \_ Cache** Klasse verfügt über diese Methoden.



| Methode                   | BESCHREIBUNG                                                                                     |
|:-------------------------|:------------------------------------------------------------------------------------------------|
| **ClearCache**           | Löscht den DNS-Server Cache von Ressourcen Datensätzen. <br/> Qualifizierer: Implementiert<br/> |
| **Getchilshedname** | Ruft den Distinguished Name für die Zone ab. <br/> Qualifizierer: Implementiert<br/>   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov. MOF</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS- \_ Domäne**](microsoftdns-domain.md)
</dt> <dt>

[**ClearCache-Methode der MicrosoftDNS- \_ Cache Klasse**](microsoftdns-cache-clearcache.md)
</dt> <dt>

[**Geterkennbar shedname-Methode der MicrosoftDNS- \_ Cache Klasse**](microsoftdns-cache-getdistinguishedname.md)
</dt> </dl>

 

 





