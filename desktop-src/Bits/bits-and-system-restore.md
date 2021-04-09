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
# <a name="bits-and-system-restore"></a>Bits und System Wiederherstellung

Nicht für alle Versionen von Bits wird das gleiche Format zum Speichern von Aufträgen verwendet. Wenn Sie den Computer vor einem Bits-Upgrade an einen Wiederherstellungspunkt zurückgeben, ist die alte Version von Bits möglicherweise nicht in der Lage, die aktuellen Auftrags Informationen zu lesen. Wenn dies der Fall ist, löscht Bits die Auftragsliste und erstellt eine neue leere Auftragsliste. Folglich werden die der vorherigen Auftragsliste zugeordneten temporären Dateien nicht bereinigt. um den Speicherplatz freizugeben, müssen Sie die Dateien manuell löschen.

Benutzer, die mit der Windows-Befehlszeile vertraut sind, können dieses Problem vermeiden, indem Sie das [BITSAdmin-Tool](bitsadmin-tool.md) verwenden, um die Liste der BITS-Aufträge vor der System Wiederherstellung Führen Sie den folgenden Befehl aus, um die Liste der BITS-Aufträge zu löschen:

**biout Admin/Reset/ALLUSERS**

Beachten Sie, dass Sie über Administratorrechte verfügen müssen, um diesen Befehl auszuführen.

 

 




