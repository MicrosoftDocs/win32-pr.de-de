---
title: Wie Speicher zugeordnet und die Speicherverteilung wieder verfügbar ist
description: Standardmäßig ruft stub-Code, der vom MIDL-Compiler generiert wird, vom Benutzer bereitgestellte Funktionen auf, um Arbeitsspeicher zu reservieren und frei zu geben. Diese Funktionen namens midl user allocate und midl user free müssen vom Entwickler bereitgestellt und \_ mit der Anwendung verknüpft \_ \_ \_ werden.
ms.assetid: 65af7a6d-4cfa-4175-9085-560d97cab41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1e7b4a0fd9a765593fc6f44365e17bc45c10b1244c226abc09ff302e81ec107
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929517"
---
# <a name="how-memory-is-allocated-and-deallocated"></a>Wie Speicher zugeordnet und die Speicherverteilung wieder verfügbar ist

Standardmäßig ruft stub-Code, der vom MIDL-Compiler generiert wird, vom Benutzer bereitgestellte Funktionen auf, um Arbeitsspeicher zu reservieren und frei zu geben. Diese Funktionen namens [**midl \_ user \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) und [**midl \_ user \_ free**](/windows/desktop/Midl/midl-user-free-1)müssen vom Entwickler bereitgestellt und mit der Anwendung verknüpft werden.

Alle Anwendungen müssen Implementierungen von [**midl \_ user \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1) und [**midl \_ user \_ free**](/windows/desktop/Midl/midl-user-free-1)zur Verfügung stellen, obwohl die Namen dieser Funktionen möglicherweise nicht explizit in den Stubs angezeigt werden. Die einzige Ausnahme ist, wenn Sie im OSF-Kompatibilitätsmodus (/osf) kompilieren. Diese vom Benutzer bereitgestellten Funktionen müssen mit einem bestimmten, definierten Funktionsprototyp übereinstimmen. Andernfalls können sie jedoch auf eine beliebige Weise implementiert werden, die für die Anwendung praktisch oder nützlich ist. Alternativ können Anwendungen das RpcSs-Speicherverwaltungspaket verwenden. Die Microsoft RPC-Laufzeitbibliothek stellt diese Gruppe von Funktionen zur Verfügung.

In den folgenden Abschnitten werden die RPC-Speicherverwaltungsfunktionen beschrieben.

-   [**midl \_ user \_ allocate**](/windows/desktop/Midl/midl-user-allocate-1)
-   [**midl \_ user \_ free**](/windows/desktop/Midl/midl-user-free-1)
-   [RpcSs-Speicherverwaltungspaket](rpcss-memory-management-package.md)

 

 