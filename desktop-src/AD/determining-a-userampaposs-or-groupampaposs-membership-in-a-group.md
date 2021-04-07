---
title: Bestimmen der Mitgliedschaft eines Benutzers oder einer Gruppe in einer Gruppe
description: Die IADsGroup. IsMember-Methode kann verwendet werden, um zu bestimmen, ob ein Objekt ein Mitglied einer Gruppe ist.
ms.assetid: c7168781-4ae4-4ce3-8d8a-2eefc7def62b
ms.tgt_platform: multiple
keywords:
- Bestimmen der Mitgliedschaft eines Benutzers oder einer Gruppe in einer Gruppen Anzeige
- Gruppen anzeigen, bestimmen der Mitgliedschaft eines Benutzers oder einer Gruppe in einer Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b520146079fdfaa5fa1adc99975b3b25d2e78c05
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038769"
---
# <a name="determining-a-users-or-groups-membership-in-a-group"></a>Bestimmen der Mitgliedschaft eines Benutzers oder einer Gruppe in einer Gruppe

Die [**IADsGroup. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) -Methode kann verwendet werden, um zu bestimmen, ob ein Objekt ein Mitglied einer Gruppe ist. Diese Methode gibt **true** zurück, wenn das angegebene Objekt ein direkter Member der Gruppe ist, d. h., die Member-Eigenschaft der Gruppe enthält das angegebene Objekt.

Eine Gruppe kann andere Gruppen enthalten. Die [**IADsGroup. IsMember**](/windows/desktop/api/iads/nf-iads-iadsgroup-ismember) -Methode überprüft die Mitglieder von Gruppen in der zugehörigen Element Eigenschaft, Gruppen innerhalb dieser Gruppen usw. nicht rekursiv. Wenn Sie rekursiv überprüfen möchten, ob ein Objekt ein Mitglied einer Gruppe ist, auflisten Sie die Gruppen in der Element Eigenschaft, überprüfen Sie die Mitglieder dieser Gruppen, um festzustellen, ob das Objekt ein Element ist, und wenn diese Gruppen andere Gruppen enthalten, überprüfen Sie Ihre Member usw.

> [!Note]  
> Da Gruppen gruppiert werden können, kann die Gruppenmitgliedschaft über Schleifen verfügen. Jedes Skript, das viele Gruppen auflistet, sollte eine interne Liste von Gruppen zum Beenden der Rekursion behalten, wenn eine Gruppe bereits besucht wurde.

 

 

 