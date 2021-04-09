---
title: Bits und System Wiederherstellung
description: Nicht für alle Versionen von Bits wird das gleiche Format zum Speichern von Aufträgen verwendet.
ms.assetid: 97c7fa69-1b35-445b-a0a1-b4d60c3ede42
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: e386084e7556b472c538308b8066875a4287a8d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036502"
---
# <a name="bits-and-system-restore"></a><span data-ttu-id="19bc2-103">Bits und System Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="19bc2-103">BITS and System Restore</span></span>

<span data-ttu-id="19bc2-104">Nicht für alle Versionen von Bits wird das gleiche Format zum Speichern von Aufträgen verwendet.</span><span class="sxs-lookup"><span data-stu-id="19bc2-104">Not all versions of BITS use the same format to store jobs.</span></span> <span data-ttu-id="19bc2-105">Wenn Sie den Computer vor einem Bits-Upgrade an einen Wiederherstellungspunkt zurückgeben, ist die alte Version von Bits möglicherweise nicht in der Lage, die aktuellen Auftrags Informationen zu lesen.</span><span class="sxs-lookup"><span data-stu-id="19bc2-105">If you return the computer to a restore point prior to a BITS upgrade, the old version of BITS may not be able to read the current job information.</span></span> <span data-ttu-id="19bc2-106">Wenn dies der Fall ist, löscht Bits die Auftragsliste und erstellt eine neue leere Auftragsliste.</span><span class="sxs-lookup"><span data-stu-id="19bc2-106">If this happens, BITS will delete the jobs list and create a new empty jobs list.</span></span> <span data-ttu-id="19bc2-107">Folglich werden die der vorherigen Auftragsliste zugeordneten temporären Dateien nicht bereinigt. um den Speicherplatz freizugeben, müssen Sie die Dateien manuell löschen.</span><span class="sxs-lookup"><span data-stu-id="19bc2-107">As a result, the temporary files associated with the previous jobs list are not cleaned up; to reclaim the disk space, you must delete the files manually.</span></span>

<span data-ttu-id="19bc2-108">Benutzer, die mit der Windows-Befehlszeile vertraut sind, können dieses Problem vermeiden, indem Sie das [BITSAdmin-Tool](bitsadmin-tool.md) verwenden, um die Liste der BITS-Aufträge vor der System Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="19bc2-108">Users familiar with the Windows command line can avoid this problem by using the [BITSAdmin tool](bitsadmin-tool.md) to clear the BITS jobs list before running System Restore.</span></span> <span data-ttu-id="19bc2-109">Führen Sie den folgenden Befehl aus, um die Liste der BITS-Aufträge zu löschen:</span><span class="sxs-lookup"><span data-stu-id="19bc2-109">To clear the BITS jobs list, run the following command:</span></span>

<span data-ttu-id="19bc2-110">**biout Admin/Reset/ALLUSERS**</span><span class="sxs-lookup"><span data-stu-id="19bc2-110">**bitsadmin /reset /allusers**</span></span>

<span data-ttu-id="19bc2-111">Beachten Sie, dass Sie über Administratorrechte verfügen müssen, um diesen Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="19bc2-111">Note that you must have administrator privileges to run this command.</span></span>

 

 




