---
description: Das Einreihen von Datei Vorgängen in der Warteschlange ist nützlich, da es Ihnen ermöglicht, die Installation als Ganzes anstelle des INF-Abschnitts zu verarbeiten.
ms.assetid: 6519c2fb-142d-4071-865f-c00a98c2fe35
title: Erstellen von Warteschlangen-und Warteschlangen Datei Vorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f344e9d1c36ecac2d3cd3293196e1d08ff81a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347437"
---
# <a name="creating-a-queue-and-queuing-file-operations"></a>Erstellen von Warteschlangen-und Warteschlangen Datei Vorgängen

Das Einreihen von Datei Vorgängen in der Warteschlange ist nützlich, da es Ihnen ermöglicht, die Installation als Ganzes anstelle des INF-Abschnitts zu verarbeiten.

Zum Erstellen einer Datei Warteschlange deklarieren Sie eine Variable zum Speichern des Warteschlangen Handles, und rufen Sie dann die [**setupopenfilequeue**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenfilequeue) -Funktion auf. Nachdem die Warteschlange erstellt wurde, können Sie Kopier-, Umbenennungs-und Löschvorgänge in die Warteschlange stellen und die Datei Warteschlange überprüfen, um in die Warteschlange eingereihte Vorgänge

Verwenden Sie die Funktionen [**setupqueuecopy**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopya), [**setupqueuerename**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamea)und [**setupqueuedelete**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletea) , um der Warteschlange einzelne Datei Vorgänge hinzuzufügen.

Alle Datei Vorgänge, die im Abschnitt **Kopieren von Dateien**, **Löschen von Dateien** oder **Umbenennen** von Dateien aufgelistet sind, können der Warteschlange mithilfe von [**setupqueuecopysection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona), [**setupqueuedeletesection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuedeletesectiona)bzw. [**setupqueuerenamesection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuerenamesectiona)hinzugefügt werden.

Eine weitere Möglichkeit, alle Dateien in den in einem **Installations** Abschnitt von inf aufgelisteten Dateien in der **Kopier Datei** in eine Warteschlange zu stellen, ist die Verwendung der Funktion [**setupinstallfilesfrominfsection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona).

Im folgenden Beispiel wird die [**setupqueuecopysection**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueuecopysectiona) -Funktion verwendet, um Kopiervorgänge für alle Dateien in die Warteschlange zu stellen, die im Abschnitt **Kopieren von Dateien** einer INF-Datei aufgelistet sind.

``` syntax
test = SetupQueueCopySection(
     MyQueue,                  \\Handle to the open queue
     "A:\",                    \\Source root path
     MyInf,                    \\Inf containing the source info
     NULL,                     \\specifies that MyInf contains 
                               \\  the section to copy as well
     MySection,                \\the name of the section to queue
  
                               \\flags specifying the copy style
     SP_COPY_NOSKIP | SP_COPY_NOBROWSE,
);
```

In dem Beispiel ist myQueue die Warteschlange zum Hinzufügen von Kopier Vorgängen, "A: \\ " gibt den Pfad zur Quelle an, und myinf ist das Handle der geöffneten INF-Datei. Der Parameter *listinfhandle* ist auf **null** festgelegt und gibt an, dass der Abschnitt zum Kopieren in myinf ist. MySection ist der Abschnitt in myinf, der die zu kopierenden Dateien enthält.

Die Flags SP \_ Copy \_ noSkip und SP \_ Copy \_ nobrowse wurden mit einem or-Operator kombiniert, um anzugeben, dass dem Benutzer keine Optionen angeboten werden sollten, um Dateien zu überspringen oder zu durchsuchen, wenn Fehler auftreten.

 

 



