---
description: Die Erweiterbarkeit wird erreicht, indem neue Objekt Bezeichner (OIDs), neue Codierungs Typen und neue DLLs verwendet werden.
ms.assetid: 95e992fe-af30-4b4e-b20d-cfe5318d0a38
title: OID-Übersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cc371d18bd144ac68c7bc95d7b3ef71140b2e1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866967"
---
# <a name="oid-overview"></a>OID-Übersicht

Die Erweiterbarkeit wird erreicht, indem neue [*Objekt*](../secgloss/o-gly.md) Bezeichner (OIDs), neue Codierungs Typen und neue DLLs verwendet werden.

CryptoAPI-OIDs können eine der folgenden Formen annehmen:

-   Eine numerische Zeichenfolge, z. b. "1.2.3.500.88"
-   Eine alphanumerische Zeichenfolge, z. b. *MyFunction*
-   Eine Konstante mit einem Wert, der kleiner oder gleich 0xFFFF ist. Diese Konstanten sind häufig mit einem Namen verknüpft, indem eine **\# define** -Anweisung in einer Header Datei verwendet wird.

Erweiterbare Funktionen akzeptieren OID-und Codierungstyp Argumente. Diese Funktionen durchsuchen die Systemregistrierung, um eine DLL zu suchen, die den OID-und Codierungstyp Argumenten der Funktion zugeordnet ist. Wenn eine DLL für die OID, Codierungstyp Kombination gefunden wird, wird die dll geladen, und die zugehörige Funktion wird aufgerufen. Die folgende Abbildung zeigt diesen Ablauf für die [**cryptencodeobject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) -Funktion:

![OID-Fluss](images/oidflow.png)

Dadurch kann die Funktionalität der kryptoapi nach Bedarf erweitert werden. Durch die Verwendung dieser Methodik können Entwickler der neuen Funktionalität den gesamten erforderlichen Code für diese Funktionalität schreiben. Zum Codieren einer neuen Datenstruktur muss z. b. die-Funktion in der DLL den gesamten Codierungsprozess ausführen.

 

 
