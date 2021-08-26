---
description: 'Das Windows Server 2003-Release von VSS unterstützt Folgendes nicht mehr:'
ms.assetid: 01993cae-433e-4d01-b805-f97592369575
title: Aus Windows Server 2003 entfernte Funktionalität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb7cd2cbfce24717bdd0bf0c36db1c5d8ff7faddebd5b7795cff6640b74df3c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006360"
---
# <a name="functionality-removed-from-windows-server-2003"></a>Aus Windows Server 2003 entfernte Funktionalität

Das Windows Server 2003-Release von VSS unterstützt Folgendes nicht mehr:

-   Writer können bei Wiederherstellungsvorgängen keine neuen Dateiwiederherstellungsziele [*(neue Zielspeicherorte)*](vssgloss-n.md)angeben.
-   Die erneute Bereitstellung einer verfügbar gemachten Schattenkopie als beschreibbares Volume wird nicht mehr unterstützt. Die **IVssBackupComponents::RemountReadWrite-Methode** ist nicht mehr verfügbar.
-   Writer können keine explizit eingeschlossenen Dateien angeben (mit [**IVssCreateWriterMetadata::AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)). Dateien können einer Komponente nur als Teil eines Dateisatzes hinzugefügt werden, indem [**IVssCreateWriterMetadata::AddFilesToFileGroup,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup) [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)oder [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)verwendet werden.

    Dateien können mithilfe von [**IVssCreateWriterMetadata::AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles)weiterhin explizit aus einer Komponente ausgeschlossen werden.

 

 



