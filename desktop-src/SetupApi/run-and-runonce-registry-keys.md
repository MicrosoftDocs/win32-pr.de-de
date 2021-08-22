---
description: Run- und RunOnce-Registrierungsschlüssel bewirken, dass Programme jedes Mal ausgeführt werden, wenn sich ein Benutzer anmeldet.
ms.assetid: 5a6c17f1-d4c0-4005-9b26-036d8b27703a
title: Run- und RunOnce-Registrierungsschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e69559a1034e3dcdb6eae215400d475fb9ca8be4025a38d064e914837af8544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665240"
---
# <a name="run-and-runonce-registry-keys"></a>Run- und RunOnce-Registrierungsschlüssel

Run- und RunOnce-Registrierungsschlüssel bewirken, dass Programme jedes Mal ausgeführt werden, wenn sich ein Benutzer anmeldet. Der Datenwert für einen Schlüssel ist eine Befehlszeile, die nicht länger als 260 Zeichen ist. Registrieren Sie die auszuführenden Programme, indem Sie Einträge der Befehlszeile der *Formularbeschreibungszeichenfolge* -  = *hinzufügen.* Sie können mehrere Einträge unter einem Schlüssel schreiben. Wenn mehrere Programme unter einem bestimmten Schlüssel registriert sind, ist die Reihenfolge, in der diese Programme ausgeführt werden, unbestimmt.

Die Windows-Registrierung enthält die folgenden vier Run- und RunOnce-Schlüssel:

-   **HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Run**
-   **HKEY \_ CURRENT USER Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Run**
-   **HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ RunOnce**
-   **HKEY \_ CURRENT USER Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ RunOnce**

Standardmäßig wird der Wert eines RunOnce-Schlüssels gelöscht, bevor die Befehlszeile ausgeführt wird. Sie können einem RunOnce-Wertnamen ein Ausrufezeichen (!) voran stellen, um das Löschen des Werts bis nach der Ausführung des Befehls zurückgestellt zu haben. Ohne das Ausrufezeichenpräfix wird das zugeordnete Programm nicht aufgefordert, beim nächsten Starten des Computers ausgeführt zu werden, wenn der RunOnce-Vorgang fehlschlägt.

Standardmäßig werden diese Schlüssel ignoriert, wenn der Computer im modus Tresor wird. Dem Wertnamen von RunOnce-Schlüsseln kann ein Sternchen ( ) vorangestellt werden, um die Ausführung des Programms auch im Tresor \* zu erzwingen.

Ein Programm, das von einem dieser Schlüssel ausgeführt wird, sollte während seiner Ausführung nicht in den Schlüssel schreiben, da dies die Ausführung anderer Programme beeinträchtigt, die unter dem Schlüssel registriert sind. Anwendungen sollten den RunOnce-Schlüssel nur für vorübergehende Bedingungen verwenden, z. B. zum Abschließen der Anwendungseinrichtung. Eine Anwendung darf Einträge unter RunOnce nicht kontinuierlich neu erstellen, da dies das Setup Windows beeinträchtigt.
