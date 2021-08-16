---
description: 'Die folgende Liste enthält Ergänzungen und Änderungen an der Volumeschattenkopie-Dienst-Schnittstelle in Windows Server 2003 mit Service Pack 1 (SP1):'
ms.assetid: 9e0dba98-5d23-444d-bd2f-cb72de8fb2d2
title: Neuerungen in VSS in Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baed6cde05eb1aabe1bc43f48aa035146e020f23d215e7902d3544414619b4e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344196"
---
# <a name="whats-new-in-vss-in-windows-server-2003-sp1"></a>Neuerungen in VSS in Windows Server 2003 SP1

Die folgende Liste enthält Ergänzungen und Änderungen an der Volumeschattenkopie-Dienst-Schnittstelle in Windows Server 2003 mit Service Pack 1 (SP1):

## <a name="auto-recovery"></a>Automatische Wiederherstellung

[*Die automatische Wiederherstellung*](vssgloss-a.md) ermöglicht Writern eine Zeit zum Aktualisieren von Komponenten in einer Schattenkopie, bevor die Schattenkopie dauerhaft in schreibgeschützt geändert wird. Beispielsweise muss eine Datenbank möglicherweise ein Rollback für unvollständige Transaktionen für alle Schattenkopien durchführen (der Datenbankwriter würde das **VSS \_ CF BACKUP \_ \_ RECOVERY-Flag** für die Datenbankkomponenten festlegen). Die vom Anfordernden initiierte automatische Wiederherstellung ermöglicht sowohl eine differenzierte Wiederherstellung (z. B. das Wiederherstellen einer Tabelle in einer Datenbank oder eines Ordners auf einem E-Mail-Server) als auch das Rollback zur Unterstützung von Data Mining, um Analysen durchzuführen, die für einen Produktionsserver zu langsam wären (der Anforderer würde **VSS \_ VOLSNAP \_ ATTR \_ ROLLBACK \_ RECOVERY** zum Schattenkopiekontext hinzufügen).) Die automatische Wiederherstellung ist nicht mit transportierbaren Schattenkopien kompatibel, aber die gleiche Funktionalität wird durch die Verwendung der [schnellen Wiederherstellung mit transportierbaren volumes mit Schattenkopien](fast-recovery-using-transportable-shadow-copied-volumes.md)unterstützt.

Die folgenden Programmierelemente haben Änderungen zur Unterstützung der automatischen Wiederherstellung:

Klassenmethoden

-   [**CVssWriter::GetSnapshotDeviceName**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   [**CVssWriter::OnPostSnapshot**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

Enumerationen

-   [**\_ \_ VSS-KOMPONENTENFLAGS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
-   [**\_\_ \_ VSS-VOLUMEMOMENTAUFNAHMEATTRIBUTE \_**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

Schnittstellenmethoden

-   [**IVssProviderCreateSnapshotSet::P reFinalCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots)
-   [**IVssProviderCreateSnapshotSet::P ostFinalCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots)

## <a name="full-support-for-transportable-shadow-copies"></a>Vollständige Unterstützung für transportierbare Schattenkopien

Transportierbare Schattenkopien werden in allen Editionen von Windows Server 2003 mit SP1 unterstützt. Weitere Informationen finden Sie unter [Importieren von transportierbaren Schattenkopievolumes.](importing-transportable-shadow-copied-volumes.md)

## <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>Schnelle Wiederherstellung mit transportierbaren Schattenkopievolumes

[Schnelle Wiederherstellung mit transportierbaren Schattenkopievolumes](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copy-storage-area-management"></a>Schattenkopiespeicherbereichsverwaltung

[**IVssSnapshotMgmt2**](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 



