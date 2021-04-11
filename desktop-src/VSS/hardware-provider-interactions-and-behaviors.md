---
description: Interaktionen und Verhalten von Hardware Anbietern
ms.assetid: 059968cf-43e5-4442-b757-80afdd66799f
title: Interaktionen und Verhalten von Hardware Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa30add6b34a7f3a0c45c88346c32c43e99398e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215547"
---
# <a name="hardware-provider-interactions-and-behaviors"></a>Interaktionen und Verhalten von Hardware Anbietern

Hardware Anbieter unterstützen möglicherweise die Schatten Kopien Copy-on-Write und/oder Full Copy Mirror (differenzielle und/oder Plex). Die Ressourcen Zuordnung für Schatten Kopien sollte dem Kontext folgen, der von der Anforderer im [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext)-enumeriert durch den [**\_ VSS- \_ Momentaufnahme \_ Kontext**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context)für den Schattenkopiesatz angegeben wird.

-   Wenn die anfordernde Person einen schattenkopiekontext angibt, der vom Anbieter unterstützt wird, sollte der Anbieter mithilfe dieser Methode eine Schatten Kopie erstellen.
-   Wenn die anfordernde Person einen schattenkopiekontext angibt, der vom Anbieter nicht unterstützt wird, sollte der Anbieter nicht versuchen, die Schatten Kopie zu erstellen und mit dem *pbissupported* -Parameter in [**ivsshardwaresnapshotprovider:: arelunssupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported) **false** zurückzugeben.
-   Wenn der Anforderer nicht explizit einen schattenkopieskontext angibt, sollte der Anbieter ein angemessenes Standardverhalten für die Erstellung von Schatten Kopien verwenden.

Hardware Anbieter, die San-RAID-Subsystemen zugeordnet sind, sollten austauschen-Schatten Kopien unterstützen, um eine Verschiebung zwischen Hosts in einem San zuzulassen.

Hardware Anbieter, die auf mehreren Computern in einem SAN ausgeführt werden und das gleiche RAID-Subsystem verwalten, müssen nicht zwischen Anbietern in einem San koordiniert werden. Der Koordinator behält jeden notwendigen Zustand bei. Zwei Arten von Zuständen werden erkannt:

-   Der Status, der zur Unterstützung des Datenzugriffs auf die auf einer Hardware Schatten Kopie enthaltenen Volumes erforderlich ist. Dies schließt alle Tags eines Volumes als schreibgeschützt oder ausgeblendet ein. Dieser Status muss sich auf der Hardware-LUN befinden und mit der LUN unterwegs sein. Dieser Status wird über Start-und/oder Geräte Ermittlung hinweg beibehalten. VSS verwaltet diesen Zustand für die Lebensdauer der Schatten Kopie.
-   Der Status, der erforderlich ist, um ein bestimmtes Volume als Teil eines schattenkopiesatzes zu erkennen. Dieser Status wird von VSS in Verbindung mit dem Anforderer beibehalten, der ursprünglich den Schattenkopiesatz erstellt hat.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Der Erstellungs Vorgang für Schatten Kopien](the-shadow-copy-creation-process.md)
-   [Erforderliches Verhalten für Schattenkopieanbieter](required-behaviors-for-shadow-copy-providers.md)
-   [Zustandsübergänge in schattenkopieanbietern](state-transitions-in-shadow-copy-providers.md)
-   [Fehlerbehandlung bei schattenkopieanbietern](error-handling-in-shadow-copy-providers.md)

 

 



