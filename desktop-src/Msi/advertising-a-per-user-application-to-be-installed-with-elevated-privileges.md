---
description: 'Verwenden Sie die Richtlinien in der folgenden Liste, um eine Anwendung pro Benutzer-Installation anzukündigen, wenn die Anwendung erhöhte Rechte (d. h. Systemrechte) für die Installation erfordert:'
ms.assetid: 0d2bd2d9-0eac-4519-862c-15f0ee5cbc40
title: Ankündigen einer Per-User Anwendung, die mit erhöhten Rechten installiert werden soll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7d9888714f28282e060b3a1e7eea0291b4e0e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347961"
---
# <a name="advertising-a-per-user-application-to-be-installed-with-elevated-privileges"></a>Ankündigen einer Per-User Anwendung, die mit erhöhten Rechten installiert werden soll

Verwenden Sie die Richtlinien in der folgenden Liste, um eine Anwendung pro Benutzer-Installation anzukündigen, wenn die Anwendung erhöhte Rechte (d. h. Systemrechte) für die Installation erfordert:

-   Dabei muss es sich um einen Dienst handeln, der unter dem Systemkonto "LocalSystem" unter Windows XP oder höher ausgeführt wird.
-   Generieren Sie ein Ankündigungs Skript, indem Sie [**msiankünderproduct**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproducta) oder [**msiankünabproductex**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)aufrufen.
-   Ihr Prozess muss die Identität des Benutzers annehmen, der das Ziel für die Ankündigung ist.
-   Rufen Sie [**msiappsescript**](/windows/desktop/api/Msi/nf-msi-msiadvertisescripta)auf, und verwenden Sie die Flags scriptflags \_ Cacheinfo \| scriptflags \_ regdata \_ appinfo \| scriptflags \_ regdata \_ cnfginfo \| scriptflags \_ -Verknüpfungen.

Wenn Sie den Richtlinien folgen, wird eine Anwendung für einen angegebenen Benutzer angekündigt, und wenn der Benutzer sich für die Installation entscheidet, wird die Anwendung mit erhöhten Rechten installiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Patchen von verwalteten Anwendungen pro Benutzer](patching-per-user-managed-applications.md)
</dt> </dl>

 

 



