---
title: Abfragen von Gruppen in einer Domäne
description: Gruppen können in einem beliebigen Container oder einer Organisationseinheit in einer Domäne und im Stammverzeichnis der Domäne abgelegt werden.
ms.assetid: 338a93dd-445d-4f74-a6d6-e5c8ba2e765e
ms.tgt_platform: multiple
keywords:
- Abfragen von Gruppen in einer Domänen-AD
- Gruppen anzeigen, Abfragen von Gruppen in einer Domäne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3abd4ec393fbeca1308ed59e08131b9b73e6b1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858126"
---
# <a name="querying-for-groups-in-a-domain"></a>Abfragen von Gruppen in einer Domäne

Gruppen können in einem beliebigen Container oder einer Organisationseinheit in einer Domäne und im Stammverzeichnis der Domäne abgelegt werden. Gruppen dürfen sich nicht immer in einem Container befinden. Daher ist es erforderlich, die gesamte Domäne zu durchsuchen, um alle Gruppen in der Domäne zu finden.

Wenn Sie nach allen Gruppen in einer Domäne suchen möchten, legen Sie den Ausgangspunkt für die Suche auf den Stamm der Domäne fest, legen Sie den Suchbereich auf Unterstruktur fest, und suchen Sie nach allen Objekten, die den [**objectClass**](/windows/desktop/ADSchema/a-objectclass) -Wert "Group" aufweisen.

Wenn Gruppen vorhanden sind, die bestimmte [**ADS- \_ \_ Gruppentyp \_**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) -Enumerationswerte enthalten, können Sie mit dem **\_ \_ \_ bitvergleichs Regel \_ -Bit und** dem passenden Regel Operator nach Gruppen suchen, für die bestimmte Bits im [**GroupType**](/windows/desktop/ADSchema/a-grouptype) -Attribut festgelegt sind. Weitere Informationen zum Verwenden von abgleichsregeln finden Sie unter [Such Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).

Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie Gruppen in einer Domäne suchen, finden Sie unter [Beispielcode für die Suche nach Gruppen in einer Domäne](example-code-for-performing-a-query-in-a-domain.md).

 

 