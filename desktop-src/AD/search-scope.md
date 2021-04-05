---
title: Angeben des Suchbereichs
description: Sie können den Bereich einer Suche entweder als Basis-, einebenen-oder Unterstruktur Suche angeben.
ms.assetid: b02354c2-7b95-4911-8ae3-4a261d3ca2d3
ms.tgt_platform: multiple
keywords:
- Festlegen des Suchbereichs AD
- Active Directory, suchen, angeben des Suchbereichs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7ff076e0410088c69eace25f204241c1c51c6fb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724433"
---
# <a name="specifying-the-search-scope"></a>Angeben des Suchbereichs

Sie können den Bereich einer Suche entweder als Basis-, einebenen-oder Unterstruktur Suche angeben. Verwenden Sie das **AD \_ searchpref- \_ suchbereichsflag \_** mit den Werten der [**ADS \_ scopeenumeration**](/windows/win32/api/iads/ne-iads-ads_scopeenum) -Enumeration, um den Suchbereich anzugeben. Die folgende Liste enthält Beschreibungen der Suchtypen:

-   **Basis**. Eine Basis Suche beschränkt die Suche auf das Basisobjekt. Die maximale Anzahl von zurückgegebenen Objekten ist immer 1. Diese Suche ist hilfreich, um zu überprüfen, ob ein Objekt zum Abrufen der Gruppenmitgliedschaft vorhanden ist. Wenn Sie z. b. über einen definierten Objektnamen verfügen und das vorhanden sein des Objekts basierend auf dem Pfad überprüfen müssen, können Sie eine Suche auf einer einzelnen Ebene verwenden. Wenn bei der Suche ein Fehler auftritt, können Sie davon ausgehen, dass das Objekt möglicherweise umbenannt oder an einen anderen Speicherort verschoben wurde, oder Sie haben die falschen Informationen über das Objekt erhalten. Beachten Sie, dass Sie die Globally Unique Identifier (GUID) des Objekts anstelle des Distinguished Name speichern sollten, wenn Sie ein Objekt überprüfen möchten. Der GUID verweist immer auf dasselbe Objekt, unabhängig davon, wo sich das Objekt in der Verzeichnishierarchie befindet.
-   **Eine Ebene**. Eine einstufige Suche ist auf die unmittelbaren untergeordneten Elemente eines Basis Objekts beschränkt, schließt jedoch das Basisobjekt selbst aus. Mit dieser Einstellung kann eine gezielte Suche nach unmittelbar untergeordneten Objekten eines übergeordneten Objekts durchgeführt werden. Angenommen, das übergeordnete Objekt P1 und seine unmittelbaren untergeordneten Elemente sind: C1, C2 und C3. Eine einstufige Suche wertet C1, C2 und C3 mit den Suchkriterien aus, wertet P1 jedoch nicht aus. Verwenden Sie eine Suche auf einer Ebene, um alle untergeordneten Elemente eines Objekts aufzulisten. Eine [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) -Enumeration wird in eine einstufige Suche übersetzt.
-   **Unterstruktur**. Eine Unterstruktur Suche (oder eine Tiefe Suche) umfasst alle untergeordneten Objekte sowie das Basisobjekt. Sie können den LDAP-Anbieter anfordern, Verweise auf andere LDAP-Verzeichnisdienste zu überarbeiten, einschließlich anderer Verzeichnis Domänen oder Gesamtstrukturen.

 

 