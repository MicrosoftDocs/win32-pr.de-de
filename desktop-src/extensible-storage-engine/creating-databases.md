---
description: 'Weitere Informationen finden Sie hier: Erstellen von Datenbanken'
title: Erstellen von Datenbanken
TOCTitle: Creating Databases
ms:assetid: d221144d-f777-4f8a-80ca-2ebdb77108dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294100(v=EXCHG.10)
ms:contentKeyID: 32765715
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: eac708b64837fc79fa8a5060df7deb93ec552e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356549"
---
# <a name="creating-databases"></a>Erstellen von Datenbanken


_**Gilt für:** Windows | Windows Server_

## <a name="creating-databases"></a>Erstellen von Datenbanken

Die ESE-Datenbank umfasst eine oder mehrere Tabellen, die Daten nach Spalten und Zeilen organisieren. Die ESE-Datenbank wird anhand des Namens und der Datenbank-ID identifiziert. Eine ESE-Datenbank sieht wie eine einzelne Datei zum Microsoft Windows-Betriebssystem aus. Intern wird die Datenbank jedoch als Sammlung von Seiten gespeichert. Diese Seiten enthalten Metadaten, die die Daten in der Datenbank, die Daten selbst und einen oder mehrere Indizes beschreiben, in denen unterschiedliche Datenreihen gespeichert werden. Die Datenbank kann bis zu 2 ^ 31 Seiten oder 16 Terabyte an Daten für eine Datenbank mit 8-KB-Seiten enthalten.

Die Anwendung erstellt eine Instanz der Datenbank-Engine, erstellt dann eine Datenbank und fügt Sie an die Instanz an. Bis zu 6 Datenbanken können gleichzeitig an eine Instanz mit [jetkreatedatabase](./jetcreatedatabase-function.md) oder [jetattachdatabase](./jetattachdatabase-function.md)angefügt werden. In der Datenbank sollte mindestens eine Sitzung gestartet werden, da alle nachfolgenden ESE-Vorgänge im Kontext einer Sitzung ausgeführt werden. Für jeden Thread sollte mithilfe von ESE eine separate Sitzung geöffnet werden.

Mit diesem Verfahren werden ESE initialisiert und eine Datenbank erstellt.

### <a name="to-initialize-ese-and-create-a-database"></a>So initialisieren Sie ESE und erstellen eine Datenbank

1.  [Jetkreateinstance](./jetcreateinstance-function.md): erstellt eine Instanz der Datenbank-Engine.
    
    **Windows XP und höher:** Diese Funktion ist in Windows XP und höher verfügbar. Unter Windows 2000 wird nur eine Instanz unterstützt, und diese Instanz wird implizit erstellt.

2.  [Jetsetsystemparameter](./jetsetsystemparameter-function.md): System Parameter, die das physische Layout beeinflussen, z. b. die JET_paramLogFilePath und JET_paramSystemPath, müssen vor dem Initialisieren der Instanz mit [jetinit](./jetinit-function.md)festgelegt werden. Die in dieser Phase festgelegten Parameter werden für alle in der Instanz erstellten Datenbanken festgelegt. [Jetsetsystemparameter](./jetsetsystemparameter-function.md) ist die einzige Funktion, die die Instanz verwenden kann, bevor Sie mit [jetinit](./jetinit-function.md)initialisiert wird.

3.  [Jetinit](./jetinit-function.md): initialisiert die-Instanz. Die Instanz muss mit [jetinit](./jetinit-function.md) initialisiert werden, bevor Sie mit anderen Funktionen verwendet werden kann.

4.  [Jetbeginsession](./jetbeginsession-function.md): erstellt die Sitzung für alle nachfolgenden Transaktionen. Alle Datenbanktransaktionen erfolgen im Kontext der Sitzung ([JET_SESID](./jet-sesid.md)).

5.  [Jetkreatedatabase](./jetcreatedatabase-function.md): erstellt die Datenbank und gibt ein Handle für die Datenbank-ID ([JET_DBID](./jet-dbid.md)) zurück.
    
    Wenn die Datenbank bereits vorhanden ist, wird Schritt 5 oben durch die folgenden beiden Schritte ersetzt:
    
    1.  [Jetattachdatabase](./jetattachdatabase-function.md): fügt die Datenbank nach Namen an die Sitzung an.
    
    2.  [Jetopendatabase](./jetopendatabase-function.md): gibt die Datenbank-ID zurück, die in nachfolgenden Daten Bank Vorgängen verwendet wird.

Eine Datenbank kann von einer ESE-Instanz mithilfe von [jetdetachdatabase](./jetdetachdatabase-function.md) getrennt und später mit [jetattachdatabase](./jetattachdatabase-function.md)an eine andere Instanz angefügt werden. Wenn die Datenbank getrennt wird, kann Sie mithilfe der standardmäßigen Windows-Hilfsprogramme als einzelne Datei kopiert werden. Wenn die Datenbank jedoch an eine ESE-Instanz angefügt ist, kann Sie nicht kopiert werden, da ESE ausschließlich Datenbankdateien öffnet. Wenn die Instanz abstürzt, kann die Datenbankdatei auch nicht allein kopiert werden, da Sie die zugehörigen Transaktionsprotokoll Dateien benötigt, um diesen Absturz wiederherzustellen.
