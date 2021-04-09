---
description: In den folgenden Themen werden Symbol Dateien und die von den dbghelp-Funktionen bereitgestellten Funktionen beschrieben.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: Informationen zu dbghelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634633d44d0c9e8202d99fd16140dd0a506453ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126247"
---
# <a name="about-dbghelp"></a>Informationen zu dbghelp

In den folgenden Themen werden Symbol Dateien und die von den [dbghelp-Funktionen](dbghelp-functions.md)bereitgestellten Funktionen beschrieben.

-   [Dbghelp-Versionen](dbghelp-versions.md)
-   [Symbol Dateien](symbol-files.md)
-   [Symbol Behandlung](symbol-handling.md)
-   [Symbol Server und Symbol Speicher](symbol-servers-and-symbol-stores.md)
-   [Minidumpdateien](minidump-files.md)
-   [Quellserver](source-server-and-source-indexing.md)
-   [Aktualisierte Plattformunterstützung](updated-platform-support.md)

Beachten Sie, dass alle [dbghelp-Funktionen](dbghelp-functions.md) Single Thread sind. Daher führen Aufrufe von mehr als einem Thread zu dieser Funktion wahrscheinlich zu unerwartetem Verhalten oder einer Beschädigung des Arbeitsspeichers. Um dies zu vermeiden, müssen Sie alle gleichzeitigen Aufrufe von mehr als einem Thread an diese Funktion synchronisieren.

 

 



