---
description: In den folgenden Themen werden Symboldateien und die von den DbgHelp-Funktionen bereitgestellten Funktionen beschrieben.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: Informationen zu DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 958a139a7dcbffb8ee1b3b3d030d170fc821e6022038cab6a704b3b04f820f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162698"
---
# <a name="about-dbghelp"></a>Informationen zu DbgHelp

In den folgenden Themen werden Symboldateien und die von den [DbgHelp-Funktionen bereitgestellten](dbghelp-functions.md)Funktionen beschrieben.

-   [DbgHelp-Versionen](dbghelp-versions.md)
-   [Symboldateien](symbol-files.md)
-   [Symbolbehandlung](symbol-handling.md)
-   [Symbolserver und Symbolspeicher](symbol-servers-and-symbol-stores.md)
-   [Minidumpdateien](minidump-files.md)
-   [Quellserver](source-server-and-source-indexing.md)
-   [Aktualisierte Plattformunterstützung](updated-platform-support.md)

Beachten Sie, dass alle [DbgHelp-Funktionen](dbghelp-functions.md) singlethreaded sind. Daher führen Aufrufe von mehr als einem Thread an diese Funktion wahrscheinlich zu unerwartetem Verhalten oder Speicherbeschädigungen. Um dies zu vermeiden, müssen Sie alle gleichzeitigen Aufrufe von mehr als einem Thread mit dieser Funktion synchronisieren.

 

 



