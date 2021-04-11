---
title: Puffer der Netzwerk Verwaltungsfunktion
description: Die RPC-Lauf Zeit Bibliothek verarbeitet die Puffer, die für die Netzwerk Verwaltungsfunktionen des 32-Bit-Datenabruf erforderlich sind, wie folgt.
ms.assetid: f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385382d12aa5b5c8c7c93b9a833f684d913c5783
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206901"
---
# <a name="network-management-function-buffers"></a>Puffer der Netzwerk Verwaltungsfunktion

Die RPC-Lauf Zeit Bibliothek verarbeitet die Puffer, die für die Netzwerk Verwaltungsfunktionen des 32-Bit-Datenabruf erforderlich sind, wie folgt:

-   **Senden von Daten an den Server** (durch in-Parameter angegebene Daten \[ \] ).

    Der Aufrufer muss den Puffer für die relevante Informationsstruktur (oder Strukturen) zuordnen und seine Freigabe zuweisen und eine Zeiger Variable an die Funktion übergeben. Der Aufrufer muss die Pufferlänge nicht angeben.

    Beispiel: [ **NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)

-   **Abrufen von Daten vom Server** (durch out-Parameter angegebene Daten \[ \] ).

    Das System ordnet den Puffer für die zurückgegebenen Informationen zu. Der Aufrufer muss bei der Eingabe eine Zeiger Variable an die Funktion übergeben. Bei erfolgreicher Rückgabe erhält der Zeiger die Adresse des vom System zugewiesenen Puffers, der die zurückgegebenen Informationen enthält. Dadurch wird der aufrufende Code vereinfacht, da der Aufrufer die Größe des Puffers nicht einschätzen muss oder die Größe des Puffers ändern und die Funktion erneut ausgeben muss.

    Wenn der Aufrufer die Verarbeitung der zurückgegebenen Informationen abgeschlossen hat, muss der vom System zugewiesene Speicher durch Aufrufen der Funktion " [**nettapibufferfree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) " freigegeben werden. Weitere Informationen zum Angeben von Puffergrößen finden Sie unter [Puffer Längen der Netzwerk Verwaltungsfunktion](network-management-function-buffer-lengths.md).

    Beispiel: [ **netgroupum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)

 

 




