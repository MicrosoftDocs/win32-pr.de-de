---
title: Abfragen von Gruppen in einer Domäne
description: Gruppen können in einem beliebigen Container oder einer Organisationseinheit in einer Domäne sowie im Stammverzeichnis der Domäne platziert werden.
ms.assetid: 338a93dd-445d-4f74-a6d6-e5c8ba2e765e
ms.tgt_platform: multiple
keywords:
- Abfragen von Gruppen in einem Domänen-AD
- Gruppen AD , Abfragen von Gruppen in einer Domäne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6079050519fca00a8e689d8af5c3fae9ce6baec2c02406ae56bccc3616a50bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184914"
---
# <a name="querying-for-groups-in-a-domain"></a>Abfragen von Gruppen in einer Domäne

Gruppen können in einem beliebigen Container oder einer Organisationseinheit in einer Domäne sowie im Stammverzeichnis der Domäne platziert werden. Gruppen befinden sich möglicherweise nicht immer in einem Container. Daher ist es erforderlich, die gesamte Domäne zu durchsuchen, um alle Gruppen in der Domäne zu finden.

Um nach allen Gruppen in einer Domäne zu suchen, legen Sie den Startpunkt der Suche auf den Stamm der Domäne fest, legen Sie den Suchbereich auf Unterstruktur fest, und suchen Sie nach allen Objekten, die über den [**objectClass-Wert**](/windows/desktop/ADSchema/a-objectclass) "group" verfügen.

Wenn Gruppen gefunden werden müssen, die bestimmte [**ADS \_ GROUP \_ \_ TYPE-ENUM-Werte**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) enthalten, kann der **LDAP MATCHING RULE BIT \_ \_ \_ AND-Abgleichsregeloperator \_** verwendet werden, um nach Gruppen zu suchen, für die bestimmte Bits im [**groupType-Attribut**](/windows/desktop/ADSchema/a-grouptype) festgelegt sind. Weitere Informationen zur Verwendung von Abgleichsregeln finden Sie unter [Suchfiltersyntax.](/windows/desktop/ADSI/search-filter-syntax)

Weitere Informationen und ein Codebeispiel, das zeigt, wie Nach Gruppen in einer Domäne gesucht wird, finden Sie unter [Beispielcode für die Suche nach Gruppen in einer Domäne.](example-code-for-performing-a-query-in-a-domain.md)

 

 