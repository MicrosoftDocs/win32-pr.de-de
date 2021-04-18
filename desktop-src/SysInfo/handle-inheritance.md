---
description: Ein untergeordneter Prozess kann Handles von seinem übergeordneten Prozess erben. Ein geerbtes Handle ist nur im Kontext des untergeordneten Prozesses gültig. Führen Sie die folgenden Schritte aus, um zu ermöglichen, dass ein untergeordneter Prozess geöffnete Handles von seinem übergeordneten Prozess erbt.
ms.assetid: 957cd369-bebf-4e04-9f7e-a936e2e97887
title: Behandlung von Vererbung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd684308503a8747f6730e9d0daf4aa3de760186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351053"
---
# <a name="handle-inheritance"></a>Behandlung von Vererbung

Ein untergeordneter Prozess kann Handles von seinem übergeordneten Prozess erben. Ein geerbtes Handle ist nur im Kontext des untergeordneten Prozesses gültig. Führen Sie die folgenden Schritte aus, um zu ermöglichen, dass ein untergeordneter Prozess geöffnete Handles von seinem übergeordneten Prozess erbt.

1.  Erstellen Sie das Handle mit dem **binherithandle** -Member der Struktur der [**Sicherheits \_ Attribute**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) , die auf **true** festgelegt ist.
2.  Erstellen Sie den untergeordneten Prozess mithilfe der Funktion " [**deateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) ", wobei der *binherithandles* -Parameter auf " **true**" festgelegt ist.

Die [**duplialisierandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) -Funktion dupliziert ein Handle, das im aktuellen Prozess oder in einem anderen Prozess verwendet werden soll. Wenn eine Anwendung eine ihrer Handles für einen anderen Prozess dupliziert, ist das doppelte Handle nur im Kontext des anderen Prozesses gültig.

Ein dupliziertes oder geerbtes Handle ist ein eindeutiger Wert, verweist jedoch auf dasselbe Objekt wie das ursprüngliche handle. Prozesse können Handles für die folgenden Objekttypen erben oder duplizieren:

-   Access Token
-   Kommunikationsgerät
-   Konsolen Eingabe
-   Bildschirm Puffer der Konsole
-   Desktop
-   Verzeichnis
-   Ereignis
-   File
-   Datei Zuordnung
-   Auftrag
-   Mailslot
-   Mutex
-   Pipe
-   Prozess
-   Registrierungsschlüssel
-   Semaphore
-   Steckdose
-   Thread
-   Timer
-   Fenster Station

Alle anderen Objekte sind für den Prozess, der Sie erstellt hat, privat. Ihre Objekt Handles können nicht dupliziert oder geerbt werden.

Weitere Informationen finden Sie unter [Vererbung](/windows/desktop/ProcThread/inheritance).

 

 
