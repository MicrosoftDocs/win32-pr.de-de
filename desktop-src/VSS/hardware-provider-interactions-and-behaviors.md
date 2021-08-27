---
description: Interaktionen und Verhaltensweisen von Hardwareanbietern
ms.assetid: 059968cf-43e5-4442-b757-80afdd66799f
title: Interaktionen und Verhaltensweisen von Hardwareanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c8029b32ee3387b86519da8630d995820bf3dab5da79769ca26f618ef32660
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122059"
---
# <a name="hardware-provider-interactions-and-behaviors"></a>Interaktionen und Verhaltensweisen von Hardwareanbietern

Hardwareanbieter unterstützen möglicherweise Kopier-bei-Schreib- und/oder vollständige Kopierspiegelungen (differenzielle und/oder plexe) Schattenkopien. Die Ressourcenzuordnung für Schattenkopien sollte dem Kontext folgen, der vom Anfordernden in [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext)angegeben wird, der von [**\_ VSS \_ SNAPSHOT \_ CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)für den Schattenkopiesatz aufzählt wird.

-   Wenn der Anfordernde einen Schattenkopiekontext angibt, der vom Anbieter unterstützt wird, sollte der Anbieter mit dieser Methode eine Schattenkopie erstellen.
-   Wenn der Anfordernde einen Schattenkopiekontext angibt, der vom Anbieter nicht unterstützt wird, sollte der Anbieter nicht versuchen, die Schattenkopie zu erstellen und **FALSE** über den *parameter pbIsSupported* in [**IVssHardwareSnapshotProvider::AreLunsSupported zurückgibt.**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported)
-   Wenn der Anfordernde nicht explizit einen Schattenkopiekontext an gibt, sollte der Anbieter ein angemessenes Standardverhalten für die Erstellung von Schattenkopien verwenden.

Hardwareanbieter, die SAN-RAID-Subsystemen zugeordnet sind, sollten transportierbare Schattenkopien unterstützen, um die Bewegung zwischen Hosts in einem SAN zu ermöglichen.

Hardwareanbieter, die auf mehreren Computern in einem SAN ausgeführt werden und dasselbe RAID-Subsystem verwalten, müssen sich nicht zwischen Anbietern in einem SAN koordinieren. Der Koordinator behält jeden erforderlichen Zustand bei. Zwei Arten von Status werden erkannt:

-   Zustand, der erforderlich ist, um den Datenzugriff auf die Volumes zu unterstützen, die in einer Hardwareschattenkopie enthalten sind. Dies schließt alle Markierungen eines Volumes als schreibgeschützt oder ausgeblendet ein. Dieser Zustand muss sich in der Hardware-LUN und mit der LUN befingen. Dieser Zustand wird über Startepochen und/oder Die Geräteermittlung hinweg beibehalten. VSS verwaltet diesen Zustand für die Lebensdauer der Schattenkopie.
-   Der Zustand, der erforderlich ist, um ein bestimmtes Volume als Teil eines Schattenkopiesets zu erkennen. Dieser Zustand wird von VSS in Verbindung mit dem Anfordernden beibehalten, der ursprünglich den Schattenkopiesatz erstellt hat.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Erstellungsprozess für Schattenkopien](the-shadow-copy-creation-process.md)
-   [Erforderliches Verhalten für Schattenkopieanbieter](required-behaviors-for-shadow-copy-providers.md)
-   [Zustandsübergänge in Schattenkopieanbietern](state-transitions-in-shadow-copy-providers.md)
-   [Fehlerbehandlung bei Schattenkopieanbietern](error-handling-in-shadow-copy-providers.md)

 

 



