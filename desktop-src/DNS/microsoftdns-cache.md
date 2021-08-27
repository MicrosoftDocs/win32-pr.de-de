---
title: MicrosoftDNS_Cache-Klasse
description: Die MicrosoftDNS \_ Cache-Klasse beschreibt einen Cache, der auf einem DNS-Server vorhanden ist.
ms.assetid: 139406eb-70f2-4614-9662-703ada032298
keywords:
- MicrosoftDNS_Cache DNS-Klasse
- MicrosoftDNS_Cache DNS-Klasse , beschrieben
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
ms.openlocfilehash: 03728a82f7668e38e43c92e3edacff1717333c6b073ee3491389723fb63b5f7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077070"
---
# <a name="microsoftdns_cache-class"></a>MicrosoftDNS \_ Cache-Klasse

Die **MicrosoftDNS \_ Cache-Klasse** beschreibt einen Cache, der auf einem DNS-Server vorhanden ist. Diese Klasse vereinfacht das Visualisieren der Containment von DNS-Objekten, anstatt ein echtes Objekt zu darstellen. Die **MicrosoftDNS \_ Cache-Klasse** ist ein Container für die vom DNS-Server zwischengespeicherten Ressourceneinträge. Verwechseln Sie dies nicht mit einer Cachedatei, die Stammhinweise enthält.

Jede Instanz der **MicrosoftDNS \_ Cache-Klasse** muss genau einem DNS-Server zugewiesen werden. Sie kann mehreren Instanzen der [**MicrosoftDNS \_ Domain-**](microsoftdns-domain.md) oder [**MicrosoftDNS \_ ResourceRecord-Klassen zugeordnet**](microsoftdns-resourcerecord.md) sein.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_Cache : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ Cache-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ Cache-Klasse** verfügt über diese Methoden.



| Methode                   | BESCHREIBUNG                                                                                     |
|:-------------------------|:------------------------------------------------------------------------------------------------|
| **ClearCache**           | Leert den DNS-Servercache von Ressourceneinträgen. <br/> Qualifizierer: Implementiert<br/> |
| **GetDistinguishedName** | Ruft den Distinguished Name für die Zone ab. <br/> Qualifizierer: Implementiert<br/>   |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Namespace<br/>                | \\MicrosoftDNS-Stamm<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MicrosoftDNS-Domäne \_**](microsoftdns-domain.md)
</dt> <dt>

[**ClearCache-Methode der MicrosoftDNS \_ Cache-Klasse**](microsoftdns-cache-clearcache.md)
</dt> <dt>

[**GetDistinguishedName-Methode der MicrosoftDNS \_ Cache-Klasse**](microsoftdns-cache-getdistinguishedname.md)
</dt> </dl>

 

 





