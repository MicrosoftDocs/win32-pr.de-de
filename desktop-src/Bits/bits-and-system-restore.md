---
title: BITS und Systemwiederherstellung
description: Nicht alle Versionen von BITS verwenden das gleiche Format zum Speichern von Aufträgen.
ms.assetid: 97c7fa69-1b35-445b-a0a1-b4d60c3ede42
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 0fbf96cf4d1e3372a9e65cad27c1e1f34ebdb07b6edd976e8b1f36add8a50eb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702100"
---
# <a name="bits-and-system-restore"></a>BITS und Systemwiederherstellung

Nicht alle Versionen von BITS verwenden das gleiche Format zum Speichern von Aufträgen. Wenn Sie den Computer vor einem BITS-Upgrade an einen Wiederherstellungspunkt zurückgeben, kann die alte Version von BITS die aktuellen Auftragsinformationen möglicherweise nicht lesen. In diesem Fall löscht BITS die Liste der Aufträge und erstellt eine neue leere Liste von Aufträgen. Daher werden die temporären Dateien, die der vorherigen Liste von Aufträgen zugeordnet sind, nicht bereinigt. Um speicherplatz freizugeben, müssen Sie die Dateien manuell löschen.

Benutzer, die mit Windows Befehlszeile vertraut sind, können dieses Problem vermeiden, indem sie das [BITSAdmin-Tool](bitsadmin-tool.md) verwenden, um die Liste der BITS-Aufträge vor dem Ausführen der Systemwiederherstellung zu löschen. Führen Sie den folgenden Befehl aus, um die Liste der BITS-Aufträge zu löschen:

**bitsadmin /reset /allusers**

Beachten Sie, dass Sie über Administratorrechte verfügen müssen, um diesen Befehl auszuführen.

 

 




