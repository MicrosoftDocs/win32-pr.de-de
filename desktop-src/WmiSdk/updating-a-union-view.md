---
description: Sie können die Werte der nicht Schlüsseleigenschaften von Union-Ansichts Klassen Instanzen aktualisieren. Die Änderungen, die Sie an der Instanz der Ansichts Klasse vornehmen, werden zurück an die Quell Klassen Instanzen weitergegeben, die die Union-Ansichts Klasse bilden.
ms.assetid: 375c9bc8-9f7b-42b4-a841-cf6af88887de
ms.tgt_platform: multiple
title: Aktualisieren einer Union-Ansicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b051147ab40aacbf9032c5a0998d5894148985c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130960"
---
# <a name="updating-a-union-view"></a>Aktualisieren einer Union-Ansicht

Sie können die Werte der nicht Schlüsseleigenschaften von Union-Ansichts Klassen Instanzen aktualisieren. Die Änderungen, die Sie an der Instanz der Ansichts Klasse vornehmen, werden zurück an die Quell Klassen Instanzen weitergegeben, die die Union-Ansichts Klasse bilden.

Die folgenden Einschränkungen gelten für Änderungen von Ansichts Klassen Instanzen:

-   Es können keine neuen Instanzen von Ansichts Klassen erstellt werden.
-   Updates werden nur von Union-Klassen unterstützt. Verknüpfungs-und Zuordnungs Sichten erstellen schreibgeschützte Ansichts Instanzen.
-   Der Erfolg eines Updates hängt davon ab, ob eine Quell Instanz aktualisierbar ist. Wenn eine Ansichts Instanzeigenschaft einer schreibgeschützten Eigenschaft einer Quell Instanz zugeordnet ist, tritt beim Versuch, die Ansichts Eigenschaft zu ändern, ein Fehler auf.

 

 



