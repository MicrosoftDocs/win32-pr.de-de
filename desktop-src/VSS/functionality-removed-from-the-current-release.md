---
description: 'Die Windows Server 2003-Version von VSS unterstützt nicht mehr Folgendes:'
ms.assetid: 01993cae-433e-4d01-b805-f97592369575
title: Aus Windows Server 2003 entfernte Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181d053420f0fc947ebad024c0eaf2bbaf32f3e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343451"
---
# <a name="functionality-removed-from-windows-server-2003"></a>Aus Windows Server 2003 entfernte Funktionen

Die Windows Server 2003-Version von VSS unterstützt nicht mehr Folgendes:

-   Writer können bei Wiederherstellungs Vorgängen keine neuen Datei Wiederherstellungs Ziele ([*neue Zielspeicher Orte*](vssgloss-n.md)) angeben.
-   Das erneute Bereitstellen einer verfügbar gemachten Schatten Kopie als beschreibbares Volume wird nicht mehr unterstützt. Die **IVssBackupComponents:: remountreadwrite** -Methode ist nicht mehr verfügbar.
-   Writer können nicht explizit enthaltene Dateien angeben (mithilfe von [**ivsskreatewritermetadata:: addincludefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)). Dateien können einer Komponente nur als Teil eines Datei Satzes mithilfe von [**ivsskreateschreitermetadata:: addfilestofilegroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**ivsskreateschreitermetadata:: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)oder [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)hinzugefügt werden.

    Dateien können mithilfe von [**ivsskreateschreitermetadata:: addexcludefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles)weiterhin explizit aus einer Komponente ausgeschlossen werden.

 

 



