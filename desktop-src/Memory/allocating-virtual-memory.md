---
description: Die Funktionen des virtuellen Arbeitsspeichers bearbeiten Arbeitsspeicher Seiten. Die Funktionen verwenden die Größe einer Seite auf dem aktuellen Computer, um die angegebenen Größen und Adressen abzurunden.
ms.assetid: 509cd529-ff79-4b07-9e09-3c5ae65f6cba
title: Zuordnen des virtuellen Speichers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f42b4f7eb9d5de3c8c5e9339c9e5931a89e371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345369"
---
# <a name="allocating-virtual-memory"></a>Zuordnen des virtuellen Speichers

Die Funktionen des virtuellen Arbeitsspeichers bearbeiten Arbeitsspeicher Seiten. Die Funktionen verwenden die Größe einer Seite auf dem aktuellen Computer, um die angegebenen Größen und Adressen abzurunden.

Die [**virtualzuweisung**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) -Funktion führt einen der folgenden Vorgänge aus:

-   Reserviert eine oder mehrere freie Seiten.
-   Führt einen Commit für eine oder mehrere reservierte Seiten aus.
-   Reserviert und führt einen Commit für eine oder mehrere freie Seiten aus.

Sie können die Startadresse der Seiten angeben, für die reserviert oder ein Commit ausgeführt werden soll, oder Sie können zulassen, dass das System die Adresse bestimmt. Die-Funktion rundet die angegebene Adresse auf die entsprechende Seitenbegrenzung. Auf reservierte Seiten kann nicht zugegriffen werden, aber zugeordnete Seiten können mit Seiten Lese **Berechtigung \_ , Seiten** **\_ Schreib** Zugriff **oder \_ Seiten** Speicherzugriff zugeordnet werden. Wenn für Seiten ein Commit ausgeführt wird, werden Arbeitsspeicher Gebühren aus der Gesamtgröße des Arbeitsspeichers und der Auslagerungs Dateien auf dem Datenträger belegt, aber jede Seite wird initialisiert und in den physischen Speicher geladen, wenn Sie zum ersten Mal versucht, diese Seite zu lesen oder zu schreiben. Sie können normale Zeiger Verweise verwenden, um auf den Speicher zuzugreifen, der von der [**virtualbelegc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) -Funktion zugesichert wurde.

 

 
