---
description: Cmspcallmultigraph-Member
ms.assetid: 49451585-3084-4426-8617-79b60eb77518
title: Cmspcallmultigraph-Member
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7ee556efbbdaf679e292b6b3a33b4b0a0b6616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360571"
---
# <a name="cmspcallmultigraph-members"></a>Cmspcallmultigraph-Member

``` syntax
CMSPArray <THREADPOOLWAITBLOCK>     m_ThreadPoolWaitBlocks;
```

Die Warte Blöcke speichern die Informationen über die Wartezeit, die im Thread Pool registriert ist. Sie enthält die vom [**RegisterWaitForSingleObject**](/windows/desktop/api/winbase/nf-winbase-registerwaitforsingleobject) -Befehl zurückgegebenen Wait-Handles und einen Zeiger auf die Kontext Struktur. Jeder Block im Array ist für ein Diagramm in einem der Streamobjekte. Der Offset eines Blocks in diesem Array entspricht dem Offset des Streams, der das Diagramm besitzt.

 

 
