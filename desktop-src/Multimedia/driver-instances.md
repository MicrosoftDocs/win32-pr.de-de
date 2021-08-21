---
title: Treiberinstanzen
description: Treiberinstanzen
ms.assetid: 93dba9e8-bfb3-4714-9466-cf5c78babcf2
keywords:
- Installierbare Treiber,Instanzen
- Installierbare Treiber,mehrere Instanzen
- mehrere Treiberinstanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deea546ffb7cd848993f8aac569d3624f87988b583ea47cab7bb16451cc6ed1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941197"
---
# <a name="driver-instances"></a>Treiberinstanzen

Windows ermöglicht mehrere Instanzen eines installierbaren Treibers. Das System erstellt bei jedem Öffnen des Treibers eine Instanz des Treibers und zerstört die Instanz, wenn der Treiber geschlossen wird. Treiberinstanzen sind besonders nützlich für installierbare Treiber, die mehrere Geräte unterstützen oder von mehreren Anwendungen oder von derselben Anwendung mehrmals geöffnet werden.

Damit der Treiber die Instanzen nachverfolgen kann, sendet das System nach dem Erstellen der Instanz ein Handle für die Treiberinstanz mit jeder Treibernachricht. Da dieses Handle die Instanz eindeutig identifiziert, ordnen installierbare Treiber das Handle häufig dem Arbeitsspeicher und anderen Ressourcen zu, die sie speziell für die Instanz zugeordnet haben.

Wenn die erste Instanz geöffnet wird, sendet das System die [**DRV \_ LOAD-,**](drv-load.md) [**DRV \_ ENABLE-**](drv-enable.md)und [**DRV \_ OPEN-Meldungen**](drv-open.md) in dieser Reihenfolge an den Treiber. Die DRV LOAD- und DRV ENABLE-Meldungen benachrichtigen den Treiber, dass er sich jetzt im Arbeitsspeicher befindet \_ und für den Betrieb aktiviert \_ ist. Die DRV \_ OPEN-Meldung identifiziert das Instanzhand handle und kann Konfigurationsinformationen für die Instanz enthalten. Bei jedem nachfolgenden Öffnen einer Instanz desselben Treibers sendet das System nur eine DRV \_ OPEN-Nachricht.

Bei der Verarbeitung einer DRV LOAD-Nachricht liest ein Treiber in der Regel Konfigurationseinstellungen aus der Registrierung, konfiguriert den Treiber und die zugehörige Hardware und weist Arbeitsspeicher für die Verwendung durch alle Instanzen des \_ Treibers zu. Wenn ein Treiber die Konfiguration nicht abschließen oder Arbeitsspeicher zuordnen kann, gibt er 0 zurück, um das System an die sofortige Entfernung des Treibers aus dem Arbeitsspeicher zu hindern und zu verhindern, dass nachfolgende Nachrichten gesendet werden. Bei der Verarbeitung der DRV ENABLE-Nachricht bereitet der Treiber die Hardware auf den Empfang und die Verarbeitung von \_ E/A-Anforderungen (Input and Output) vor. Die Vorbereitung kann die Installation von Interrupthandlern umfassen.

Bei der Verarbeitung der DRV OPEN-Nachricht weist der Treiber Arbeitsspeicher oder Ressourcen zu, die von der angegebenen Instanz des Treibers benötigt werden, und gibt dann einen Wert ungleich \_ 0 (null) zurück. Das System verwendet diesen Wert ungleich 0 (null) als *Treiberbezeichner* in nachfolgenden Treibermeldungen für die Instanz. Der Treiber kann diesen Bezeichner für jeden Zweck verwenden. Einige Treiber verwenden z. B. ein Speicherhand handle für den Bezeichner, um schnellen Zugriff auf den Arbeitsspeicher zu erhalten, der Informationen über die gegebene Instanz enthält.

Viele installierbare Treiber verarbeiten den zweiten Parameter der DRV OPEN-Nachricht, was dem System und den Anwendungen die Möglichkeit gibt, beim Öffnen einer Instanz zusätzliche Informationen an den \_ Treiber zu senden. Der -Parameter kann ein einzelner Wert oder eine Adresse einer -Struktur sein, die einen Satz von Werten enthält. Bei der Verarbeitung von DRV OPEN überprüft der Treiber den Parameter, um zu bestimmen, ob es sich um einen Wert handelt, und verwendet die angegebenen Werte (sofern dies der Fall ist), um die Erstellung \_ der Instanz fertig zu stellen.

Das System sendet jedes Mal [**eine DRV \_ CLOSE-Nachricht,**](drv-close.md) wenn eine Instanz geschlossen wird. Das instanzhand handle, das mit der Nachricht gesendet wird, gibt an, welche Instanz geschlossen werden soll. Wenn die letzte verbleibende Instanz geschlossen wird, sendet das System die DRV \_ CLOSE-, [**DRV \_ DISABLE-**](drv-disable.md)und [**DRV \_ FREE-Meldungen**](drv-free.md) in dieser Reihenfolge. Die DRV CLOSE-Meldung leitet den Treiber an, die Instanz zu schließen, und die \_ DRV DISABLE- und DRV FREE-Meldungen benachrichtigen den Treiber, dass er jetzt deaktiviert ist und sofort aus dem Arbeitsspeicher \_ \_ frei wird.

Bei der Verarbeitung der DRV CLOSE-Nachricht gibt der Treiber in der Regel jeglichen Arbeitsspeicher oder alle Ressourcen frei, die \_ für die Instanz zugeordnet sind. Bei der Verarbeitung der DRV DISABLE-Meldung platziert der Treiber jede Hardware in einen inaktiven Zustand, was das Entfernen von \_ Interrupthandlern umfassen kann. Bei der Verarbeitung der DRV FREE-Nachricht gibt der Treiber jeglichen Arbeitsspeicher oder alle Ressourcen \_ frei, die noch zugeordnet sind.

Installierbare Treiber sind nicht erforderlich, um mehrere Instanzen zu unterstützen. Ein Treiber kann verhindern, dass eine Instanz erstellt wird, indem er 0 (null) für die [**DRV \_ OPEN-Nachricht**](drv-open.md) zurücksendet.

 

 




