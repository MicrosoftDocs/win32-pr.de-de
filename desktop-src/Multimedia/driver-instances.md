---
title: Treiber Instanzen
description: Treiber Instanzen
ms.assetid: 93dba9e8-bfb3-4714-9466-cf5c78babcf2
keywords:
- installierbare Treiber, Instanzen
- installierbare Treiber, mehrere Instanzen
- mehrere Treiber Instanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37148dcb12fbfa2984d4e55424102b5985165d9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709588"
---
# <a name="driver-instances"></a>Treiber Instanzen

Windows ermöglicht mehrfaches Instanzen eines installierbaren Treibers. Das System erstellt jedes Mal, wenn der Treiber geöffnet wird, eine Instanz des Treibers und zerstört die Instanz, wenn der Treiber geschlossen wird. Treiber Instanzen sind besonders nützlich für installierbare Treiber, die mehrere Geräte unterstützen oder die von mehreren Anwendungen oder von der gleichen Anwendung mehrmals geöffnet werden.

Um dem Treiber beim Nachverfolgen der Instanzen zu helfen, sendet das System einen treiberinstanzhandle mit jeder Treiber Nachricht, nachdem die Instanz erstellt wurde. Da dieses Handle die Instanz eindeutig identifiziert, ordnen installierbare Treiber das Handle häufig dem Arbeitsspeicher und anderen Ressourcen zu, die Sie speziell für die Instanz zugeordnet haben.

Wenn die erste Instanz geöffnet wird, sendet das System die Nachrichten [**drv \_ Load**](drv-load.md), [**drv \_ enable**](drv-enable.md)und [**drv \_ Open**](drv-open.md) an den Treiber in dieser Reihenfolge. Der drv \_ -Lade-und drv- \_ Aktivierungs Nachrichten benachrichtigen den Treiber, dass er sich nun im Arbeitsspeicher befindet und für den Betrieb aktiviert ist. Die "drv \_ Open"-Meldung identifiziert das Instanzhandle und kann Konfigurationsinformationen für die Instanz enthalten. Bei jedem nachfolgenden Öffnen einer Instanz desselben Treibers sendet das System nur eine vom drv \_ geöffnete Nachricht.

Bei der Verarbeitung einer drv \_ -Lade Nachricht liest ein Treiber in der Regel Konfigurationseinstellungen aus der Registrierung, konfiguriert den Treiber und alle zugeordneten Hardware und ordnet Speicher für die Verwendung durch alle Instanzen des Treibers zu. Wenn ein Treiber die Konfiguration nicht ausführen kann oder Arbeitsspeicher belegt, wird NULL zurückgegeben, damit das System den Treiber sofort aus dem Arbeitsspeicher entfernt und verhindert, dass nachfolgende Nachrichten gesendet werden. Beim Verarbeiten der drv- \_ Aktivierungs Nachricht bereitet der Treiber die Hardware für das empfangen und Verarbeiten von Eingabe-und Ausgabeanforderungen (e/a) vor. Die Vorbereitung kann die Installation von Interrupt-Handlern einschließen.

Bei der Verarbeitung der \_ vom drv geöffneten Nachricht weist der Treiber Speicher oder Ressourcen zu, die für die angegebene Instanz des Treibers erforderlich sind, und gibt dann einen Wert ungleich 0 (null) zurück. Das System verwendet diesen Wert ungleich 0 (null) als *Treiber Bezeichner* in nachfolgenden Treiber Meldungen für die Instanz. Dieser Bezeichner kann vom Treiber für beliebige Zwecke verwendet werden. Einige Treiber verwenden z. b. ein Speicher Handle für den Bezeichner, um schnellen Zugriff auf den Arbeitsspeicher zu erhalten, der Informationen über die angegebene Instanz enthält.

Viele installierbare Treiber verarbeiten den zweiten Parameter der drv-Nachricht vom Typ "drv" \_ , sodass das System und die Anwendungen beim Öffnen einer Instanz die Möglichkeit haben, zusätzliche Informationen an den Treiber zu senden. Der-Parameter kann ein einzelner Wert oder eine Adresse einer Struktur sein, die einen Satz von Werten enthält. Bei der Verarbeitung von drv wird der- \_ Parameter vom Treiber überprüft, um zu bestimmen, ob es sich um einen Wert handelt, und verwendet die angegebenen Werte (sofern vorhanden), um die Erstellung der Instanz abzuschließen.

Das System sendet immer dann eine [**drv- \_ Close**](drv-close.md) -Nachricht, wenn eine Instanz geschlossen wird. Das mit der Meldung gesendete Instanzhandle identifiziert, welche Instanz geschlossen werden soll. Wenn die letzte verbleibende Instanz geschlossen ist, sendet das System die \_ [**\_ freien**](drv-free.md) drv-Nachrichten vom Typ drv Close, [**drv \_ Deaktivieren**](drv-disable.md)und drv in dieser Reihenfolge. Die drv- \_ Schließen-Nachricht weist den Treiber an, die Instanz zu schließen, und die \_ kostenlosen drv-und drv- \_ Nachrichten benachrichtigen den Treiber, dass er nun deaktiviert ist und sofort aus dem Speicher freigegeben wird.

Beim Verarbeiten der drv- \_ Schließen-Nachricht gibt der Treiber in der Regel den Arbeitsspeicher oder die Ressourcen frei, die der Instanz zugeordnet sind. Wenn die drv-Deaktivierungs \_ Nachricht verarbeitet wird, versetzt der Treiber alle Hardware in einen inaktiven Zustand. Dies kann das Entfernen von Interrupt-Handlern einschließen. Bei der Verarbeitung der \_ freien drv-Nachricht gibt der Treiber Speicher oder Ressourcen frei, die noch zugeordnet sind.

Installierbare Treiber sind nicht erforderlich, um mehrere Instanzen zu unterstützen. Ein Treiber kann verhindern, dass eine Instanz erstellt wird, indem er für die [**drv- \_ Open**](drv-open.md) -Nachricht 0 zurückgibt.

 

 




