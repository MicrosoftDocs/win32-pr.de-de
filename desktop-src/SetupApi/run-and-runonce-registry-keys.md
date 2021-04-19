---
description: Ausführen und RunOnce-Registrierungsschlüssel bewirken, dass Programme jedes Mal ausgeführt werden, wenn sich ein Benutzer anmeldet.
ms.assetid: 5a6c17f1-d4c0-4005-9b26-036d8b27703a
title: Ausführen und RunOnce-Registrierungsschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89cf51ad3c7e2096aeffbbd6ed98c02a202f2ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363403"
---
# <a name="run-and-runonce-registry-keys"></a>Ausführen und RunOnce-Registrierungsschlüssel

Ausführen und RunOnce-Registrierungsschlüssel bewirken, dass Programme jedes Mal ausgeführt werden, wenn sich ein Benutzer anmeldet. Der Datenwert für einen Schlüssel ist eine Befehlszeile, die nicht länger als 260 Zeichen ist. Registrieren Sie die Programme, die ausgeführt werden sollen, indem Sie Einträge in der - *zeichenfolgenzeichenfolge* =  Sie können mehrere Einträge unter einem Schlüssel schreiben. Wenn mehr als ein Programm unter einem bestimmten Schlüssel registriert ist, ist die Reihenfolge, in der diese Programme ausgeführt werden, unbestimmt.

Die Windows-Registrierung umfasst die folgenden vier Run-und RunOnce-Schlüssel:

-   **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run**
-   **HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run**
-   **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**
-   **HKEY \_ Current \_ User \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**

Standardmäßig wird der Wert einer RunOnce-Taste gelöscht, bevor die Befehlszeile ausgeführt wird. Sie können einem RunOnce-Wertnamen ein Ausrufezeichen (!) als Präfix voranstellen, um das Löschen des Werts zu verzögern, bis der Befehl ausgeführt wird. Ohne das Ausrufezeichen-Präfix wird das zugehörige Programm beim nächsten Start des Computers nicht aufgefordert, beim nächsten Start des Computers ausgeführt zu werden.

Standardmäßig werden diese Schlüssel ignoriert, wenn der Computer im abgesicherten Modus gestartet wird. Der Wertname von RunOnce-Schlüsseln kann ein Sternchen () vorangestellt werden \* , um zu erzwingen, dass das Programm auch im abgesicherten Modus ausgeführt wird.

Ein Programm, das von einem dieser Schlüssel ausgeführt wird, sollte während der Ausführung nicht in den Schlüssel schreiben, da dies die Ausführung anderer Programme, die unter dem Schlüssel registriert sind, beeinträchtigt. Anwendungen sollten den RunOnce-Schlüssel nur für vorübergehende Bedingungen verwenden, z. b. zum Ausführen des Anwendungs Setups. Eine Anwendung darf Einträge unter RunOnce nicht fortlaufend neu erstellen, da dies die Windows Setup beeinträchtigt.
