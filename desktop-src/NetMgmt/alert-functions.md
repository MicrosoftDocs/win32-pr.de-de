---
title: Benachrichtigungsfunktionen
description: Die Netzwerk Verwaltungs Benachrichtigungsfunktionen Benachrichtigen Netzwerkdienst Programme und Anwendungen von Netzwerk Ereignissen.
ms.assetid: e131191b-7413-45ff-84cd-b3a873d33ca1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80fde863b27bebc8bf815c939f7edf96cd998442
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473557"
---
# <a name="alert-functions"></a>Benachrichtigungsfunktionen

\[Die Warnungs Funktionen werden ab Windows Vista nicht unterstützt, da die Dienste "Warn" und "Messenger" nicht unterstützt werden.\]

Die Netzwerk Verwaltungs Benachrichtigungsfunktionen Benachrichtigen Netzwerkdienst Programme und Anwendungen von Netzwerk Ereignissen. Ein *Ereignis* ist eine bestimmte Instanz eines Prozesses, eines Vorkommens oder eines Hardware Zustands, wie in einer Anwendung definiert. Die Warnungs Funktionen ermöglichen es Anwendungen, anzugeben, wann vordefinierte Ereignisse auftreten.

**Windows Server 2003:** Die Dienste "Warn" und "Messenger" sind unter Windows Server 2003 standardmäßig deaktiviert. Sie müssen die Dienste erneut aktivieren, bevor Sie die Benachrichtigungsfunktionen der Netzwerkverwaltung oder die [Funktionen](message-functions.md)der Netzwerk Verwaltungs Nachricht aufrufen.

Die Warnungs Funktionen sind nachfolgend aufgeführt.



| Funktion                                   | BESCHREIBUNG                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Netzwerkertraise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | Benachrichtigt alle registrierten Clients, dass ein bestimmtes Ereignis aufgetreten ist.                                                                                                                                  |
| [**"Ntalertraiseex"**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | Vereinfacht das Benachrichtigen registrierter Clients, dass ein bestimmtes Ereignis aufgetreten ist, da " **nettalertraiseex** " im Gegensatz zu " **nettalertraise**" keine [**Std- \_**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) Warnungs Struktur erfordert. |



 

Der alteste-Dienst muss auf dem Client Computer ausgeführt werden, wenn Sie die Funktion " **nettalertraise** " oder die Funktion " **nettalertraiseex** " aufrufen. Wenn der Dienst nicht ausgeführt wird, schlagen die Funktionen fehl, und die **Fehler \_ Datei wurde \_ nicht \_ gefunden**. Der alattedienst auf dem Client ruft die [**netmessagebuffersend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend) -Funktion auf, um Informationen an Empfänger zu senden.

Anwendungen, Netzwerkdienste und interne Netzwerkkomponenten verwenden die Benachrichtigungsfunktionen der Netzwerkverwaltung, um eine Warnung zu generieren und verschiedene Anwendungen oder Benutzer zu benachrichtigen, wenn ein bestimmter Ereignistyp auftritt. Die Warnungs Kategorieinformationen, Datentypen, Strukturen und Konstanten werden in den lmcons definiert. H, lmerr. H und lmalert. H-Header Dateien. Um auf diese Definitionen zuzugreifen, definieren Sie die Konstanten einschließlich " \_ netterrors" und "inklusive" \_ , und schließen Sie die Header Datei "LM. H" ein.

Der lmalert. Die H-Datei definiert die folgenden Warn Klassen (Typen von Netzwerk Ereignissen) für das Senden von Warnungen:

-   Netzwerkereignisse, die administrative Unterstützung erfordern
-   Hinzufügen eines Eintrags zu einer Fehlerprotokoll Datei
-   Empfang einer Broadcast Nachricht durch einen Benutzer oder eine Anwendung
-   Abschluss eines Druckauftrags
-   Verwendung bestimmter Anwendungen oder Ressourcen durch Benutzer

Sie können bei Bedarf andere Klassen von Warnungen für Netzwerkanwendungen definieren. Wenn z. b. eine Anwendung auf einem Server regelmäßig große Datenmengen auf ein Laufwerk schreibt, führt die Anwendung das Risiko aus, den Datenträger zu füllen. In diesem Fall möchten Sie möglicherweise das Ereignis "kein freier Speicherplatz" hinzufügen, um eine Warnung zu generieren, mit der die Anwendung benachrichtigt wird, den Prozess zu beenden oder zu beenden, der den Datenträger füllt. Der Ereignis Name für eine Warnung kann eine beliebige Text Zeichenfolge sein.

Wenn Sie eine Warnung mit einem aufzurufenden Befehl an die Funktion " [**nettalertraise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise) " ausgeben, sollten die Nachrichten Daten aus einer Std-Warnungs Header Struktur bestehen, gefolgt von zusätzlichen Daten fester Länge, die in einem [**anderen Administrator ( \_ Weitere \_**](/windows/desktop/api/Lmalert/ns-lmalert-admin_other_info)Informationen, andere Info-Informationen, [**Andere Info \_ \_**](/windows/desktop/api/Lmalert/ns-lmalert-errlog_other_info) [**\_**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) -Informationen oder andere Informationen für andere [**Benutzer \_ \_**](/windows/desktop/api/Lmalert/ns-lmalert-user_other_info) ) Warnungs spezifisch sind. [**\_ \_**](/windows/desktop/api/Lmalert/ns-lmalert-print_other_info) Zusätzliche Daten variabler Länge können der Warnungs spezifischen Struktur folgen. (Aufrufe der Funktion " [**nettalertraiseex**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) " erfordern keine Std-Warnungs Struktur.) **\_** Die aufrufende Anwendung muss den Speicher für alle Strukturen und Daten variabler Länge zuweisen und den Speicher freigeben, nachdem der Aufruf zurückgegeben wurde.

Die folgenden Makros sind zur Verwendung mit Warnungs Daten Puffern verfügbar.



| Makro                                          | Beschreibung                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**\_Weitere \_ Informationen Benachrichtigen**](/windows/desktop/api/Lmalert/nf-lmalert-alert_other_info) | Gibt einen Zeiger auf die Daten fester Länge zurück, die der **Std \_** -Warnungs Struktur in einer Warnmeldung folgen. |
| [**Warnung \_ zu \_ Daten in var**](/windows/desktop/api/Lmalert/nf-lmalert-alert_var_data)     | Gibt einen Zeiger auf die Daten variabler Länge zurück, die den Warnungs spezifischen Daten in einer Warnmeldung folgen.   |



 

Anstatt die Funktionen der Netzwerk Verwaltungs Warnung zu verwenden, können Sie möglicherweise das-Windows-Verwaltungsinstrumentation (WMI)-SDK für die Ereignis Benachrichtigung verwenden. Weitere Informationen zu den Plattformen, die das WMI-Ereignis Modell unterstützen, finden Sie unter [WMI-Infrastruktur](/windows/desktop/WmiSdk/wmi-infrastructure) und [Überwachungs Ereignisse](/windows/desktop/WmiSdk/monitoring-events) in der WMI-Dokumentation.

 

 