---
title: MicrosoftDNS_RootHints-Klasse
description: Die MicrosoftDNS \_ RootHints-Klasse beschreibt die RootHints, die in einer Cachedatei auf einem DNS-Server gespeichert sind. Diese Klasse vereinfacht das Visualisieren der Containment von DNS-Objekten, anstatt ein echtes Objekt zu darstellen.
ms.assetid: d6dbce97-cffd-476a-ba61-c070d8245f0a
keywords:
- MicrosoftDNS_RootHints DNS-Klasse
- MicrosoftDNS_RootHints DNS-Klasse , beschrieben
topic_type:
- apiref
api_name:
- MicrosoftDNS_RootHints
- MicrosoftDNS_RootHints.WriteBackRootHintDatafile
- MicrosoftDNS_RootHints.GetDistinguishedName
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 050da9acb1d3865fb490035b6de57fcc1279a45b6f9d78c57df305993d590c02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913000"
---
# <a name="microsoftdns_roothints-class"></a>MicrosoftDNS \_ RootHints-Klasse

Die **MicrosoftDNS \_ RootHints-Klasse** beschreibt die RootHints, die in einer Cachedatei auf einem DNS-Server gespeichert sind. Diese Klasse vereinfacht das Visualisieren der Containment von DNS-Objekten, anstatt ein echtes Objekt zu darstellen.

**MicrosoftDNS \_ RootHints ist** ein Container für die Ressourceneinträge, die vom DNS-Server in einer Cachedatei gespeichert werden. Jede Instanz der **MicrosoftDNS \_ RootHints-Klasse** muss genau einem DNS-Server zugewiesen werden. Sie kann mehreren Instanzen der [**MicrosoftDNS \_ ResourceRecord-Klasse zugeordnet**](microsoftdns-resourcerecord.md) sein.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
class MicrosoftDNS_RootHints : MicrosoftDNS_Domain
{
};
```

## <a name="members"></a>Member

Die **MicrosoftDNS \_ RootHints-Klasse** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **MicrosoftDNS \_ RootHints-Klasse** verfügt über diese Methoden.



| Methode                        | BESCHREIBUNG                                                                                     |
|:------------------------------|:------------------------------------------------------------------------------------------------|
| **GetDistinguishedName**      | Ruft den Distinguished Name für die Zone ab. <br/> Qualifizierer: Implementiert<br/>   |
| **WriteBackRootHintDatafile** | Schreibt die RootHints zurück in die DNS-Cachedatei. <br/> Qualifizierer: Implementiert<br/> |



 

## <a name="requirements"></a>Anforderungen



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

[**WriteBackRootHintDatafile-Methode der MicrosoftDNS \_ RootHints-Klasse**](microsoftdns-roothints-writebackroothintdatafile.md)
</dt> <dt>

[**GetDistinguishedName-Methode der MicrosoftDNS \_ RootHints-Klasse**](microsoftdns-roothints-getdistinguishedname.md)
</dt> </dl>

 

 





