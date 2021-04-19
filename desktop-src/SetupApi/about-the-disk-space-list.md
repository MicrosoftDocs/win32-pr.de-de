---
description: Mithilfe der Speicherplatz Liste können Sie den Speicherplatz berechnen, der zum Abschluss der Installations Vorgänge erforderlich ist.
ms.assetid: 6514cbdd-2f23-4ab8-9e34-86d3837503dc
title: Informationen zur Disk-Space Liste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b092d73c00f426fe5c0ab298e4b6a53c19131c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348375"
---
# <a name="about-the-disk-space-list"></a>Informationen zur Disk-Space Liste

Mithilfe der Speicherplatz Liste können Sie den Speicherplatz berechnen, der zum Abschluss der Installations Vorgänge erforderlich ist. Nachdem Sie eine Speicherplatz Liste erstellt und Ihr Dateien hinzugefügt haben, können Sie die Liste Abfragen, um die Ziel Laufwerke zu ermitteln, die von den Datei Vorgängen angegeben werden, und den Speicherplatz, der auf jedem Laufwerk erforderlich ist.

Wenn Sie den erforderlichen Speicherplatz mit dem auf den Ziel Datenträgern verfügbaren Speicherplatz vergleichen, können Sie Programm gesteuert ermitteln, ob genügend Speicherplatz für die aktuelle Installation verfügbar ist.

Sie können der Speicherplatz Liste Datei Vorgänge hinzufügen oder aus ihr entfernen und den erforderlichen Speicherplatz neu berechnen. Diese Funktion ermöglicht es Ihnen beispielsweise, ein Programm zu schreiben, das mit dem Benutzer interagiert, sodass Sie die zu installierenden Komponenten basierend auf dem benötigten Speicherplatz auswählen können.

Die Speicherplatz Listen-Funktionen suchen automatisch nach bereits vorhandenen Kopien von Dateien auf dem Ziel Datenträger. Wenn eine frühere Version der Datei gefunden wird, berechnen die Speicherplatz Listen Funktionen den zusätzlichen Speicherplatz, der zum Durchführen der Datei Vorgänge erforderlich ist.

Wenn ein Kopiervorgang z. b. angibt, dass eine 6000-Byte-Datei auf Laufwerk c kopiert werden soll und eine 2000-Byte-Version dieser Datei bereits auf dem Laufwerk c vorhanden ist, geben die Speicherplatz Funktionen einen erforderlichen Speicherplatz von 4000 Bytes zurück. Der zusätzliche Speicherplatz wird verwendet, um die ältere Version der Datei durch die neuere Version zu ersetzen.

Die Datenträger-Speicherplatz Liste dient zum Runden der Dateigrößen auf die Datenträger Cluster Grenzen.

 

 



