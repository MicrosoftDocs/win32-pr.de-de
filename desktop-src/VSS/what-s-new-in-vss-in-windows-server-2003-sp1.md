---
description: 'Die folgende Liste gibt Ergänzungen und Änderungen an der Volumeschattenkopie-Dienst-Schnittstelle in Windows Server 2003 mit Service Pack 1 (SP1) an:'
ms.assetid: 9e0dba98-5d23-444d-bd2f-cb72de8fb2d2
title: Neues in VSS unter Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559b51d5b019d9d57aa154c4728ef5c8f4bb19d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485019"
---
# <a name="whats-new-in-vss-in-windows-server-2003-sp1"></a>Neues in VSS unter Windows Server 2003 SP1

Die folgende Liste gibt Ergänzungen und Änderungen an der Volumeschattenkopie-Dienst-Schnittstelle in Windows Server 2003 mit Service Pack 1 (SP1) an:

## <a name="auto-recovery"></a>Automatische Wiederherstellung

Die [*Automatische Wiederherstellung*](vssgloss-a.md) ermöglicht Writer eine Zeit zum Aktualisieren von Komponenten in einer Schatten Kopie, bevor die Schatten Kopie dauerhaft in schreibgeschützt geändert wird. Beispielsweise muss eine Datenbank möglicherweise unvollständige Transaktionen für alle Schatten Kopien zurücksetzen (der datenbankwriter würde das **VSS CF- \_ \_ \_ sicherungswiederherstellungsflag** für die Datenbankkomponenten festlegen). Die automatische Wiederherstellung, die von der anfordernden Person initiiert wurde, ermöglicht eine differenzierte Wiederherstellung (z. b. das Wiederherstellen einer Tabelle in einer Datenbank oder eines Ordners auf einem e-Mail-Server) oder das Rollback zur Unterstützung von Data Mining zur Durchführung von Analysen, die für einen Produktions **Server zu langsam \_ \_ \_ \_** sind. Die automatische Wiederherstellung ist nicht mit transportfähigen Schatten Kopien kompatibel, aber die gleiche Funktionalität wird durch die Verwendung der [schnellen Wiederherstellung mithilfe von austauschen schattenkopierten Volumes](fast-recovery-using-transportable-shadow-copied-volumes.md)unterstützt.

Die folgenden Programmier Elemente haben Änderungen zur Unterstützung der automatischen Wiederherstellung:

Klassen Methoden

-   [**CVssWriter:: geznapshotdevicename**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   [**CVssWriter:: OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

Enumerationen

-   [**VSS \_ - \_ Komponentenflags**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
-   [**\_VSS \_ - \_ volumesnapshotattribute \_**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

Schnittstellen Methoden

-   [**Ivssproviderkreatesnapshotset::P Verfeinerungs Momentaufnahmen**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots)
-   [**Ivssproviderkreatesnapshotset::P ostfinalcommitsnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots)

## <a name="full-support-for-transportable-shadow-copies"></a>Vollständige Unterstützung für transportable-Schatten Kopien

Transportable-Schatten Kopien werden in allen Editionen von Windows Server 2003 mit SP1 unterstützt. Weitere Informationen finden Sie unter [importieren transportable-Schattenkopievolumes](importing-transportable-shadow-copied-volumes.md).

## <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>Schnelle Wiederherstellung mithilfe von transportable schattenkopierten Volumes

[Schnelle Wiederherstellung mithilfe von transportable schattenkopierten Volumes](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copy-storage-area-management"></a>Schatten Kopie-Speicherbereichs Verwaltung

[**IVssSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 



