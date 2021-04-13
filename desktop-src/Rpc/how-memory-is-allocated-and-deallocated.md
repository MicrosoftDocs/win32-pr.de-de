---
title: Zuordnen und Aufheben der Zuordnung von Arbeitsspeicher
description: Standardmäßig ruft der von dem Mittelwert Compiler generierte Stub-Code vom Benutzer bereitgestellte Funktionen zum Zuordnen und Freigeben von Arbeitsspeicher auf. Diese Funktionen mit dem Namen "Mittel l \_ \_ -Benutzer zuweisen" und "mittlere \_ Benutzer Kosten" \_ müssen vom Entwickler bereitgestellt und mit der Anwendung verknüpft werden.
ms.assetid: 65af7a6d-4cfa-4175-9085-560d97cab41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 331c32ac4d33fbd67f617f79125921ddfffc0de5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390716"
---
# <a name="how-memory-is-allocated-and-deallocated"></a>Zuordnen und Aufheben der Zuordnung von Arbeitsspeicher

Standardmäßig ruft der von dem Mittelwert Compiler generierte Stub-Code vom Benutzer bereitgestellte Funktionen zum Zuordnen und Freigeben von Arbeitsspeicher auf. Diese Funktionen mit dem Namen " [**Mittel l- \_ Benutzer \_ zuweisen**](/windows/desktop/Midl/midl-user-allocate-1) " und " [**mittlere \_ Benutzer \_ Kosten**](/windows/desktop/Midl/midl-user-free-1)" müssen vom Entwickler bereitgestellt und mit der Anwendung verknüpft werden.

Alle Anwendungen müssen Implementierungen von [**mittlerer l- \_ Benutzer \_**](/windows/desktop/Midl/midl-user-allocate-1) Zuordnungen und [**mittlerer l- \_ Benutzer \_ kostenlos**](/windows/desktop/Midl/midl-user-free-1)bereitstellen, auch wenn die Namen dieser Funktionen möglicherweise nicht explizit in den stubzeichen angezeigt werden. Die einzige Ausnahme ist die Kompilierung im OSF-Kompatibilitätsmodus (/OSF). Diese vom Benutzer bereitgestellten Funktionen müssen mit einem bestimmten, definierten Funktionsprototyp in beliebiger Weise implementiert werden, die für die Anwendung praktisch oder nützlich ist. Alternativ können Anwendungen das RPCSS-Speicher Verwaltungspaket verwenden. Die Microsoft RPC-Lauf Zeit Bibliothek stellt diese Gruppe von Funktionen bereit.

In den folgenden Abschnitten werden die RPC-Speicherverwaltungsfunktionen beschrieben.

-   [**mittlere Benutzer Zuordnungen \_ \_**](/windows/desktop/Midl/midl-user-allocate-1)
-   [**mittlerer l- \_ Benutzer \_ kostenlos**](/windows/desktop/Midl/midl-user-free-1)
-   [RPCSS-Speicher Verwaltungspaket](rpcss-memory-management-package.md)

 

 