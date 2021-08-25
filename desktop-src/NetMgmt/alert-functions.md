---
title: Warnungsfunktionen
description: Die Warnungsfunktionen der Netzwerkverwaltung benachrichtigen Netzwerkdienstprogramme und Anwendungen über Netzwerkereignisse.
ms.assetid: e131191b-7413-45ff-84cd-b3a873d33ca1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411a9bab5f8b74b5dc6e83d9a3c09cdcaeebf66d34c265ad27639e7aab8d7c00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912460"
---
# <a name="alert-functions"></a>Warnungsfunktionen

\[Die Warnungsfunktionen werden ab Windows Vista nicht unterstützt, da die Warnungs- und Messenger-Dienste nicht unterstützt werden.\]

Die Warnungsfunktionen der Netzwerkverwaltung benachrichtigen Netzwerkdienstprogramme und Anwendungen über Netzwerkereignisse. Ein *Ereignis* ist eine bestimmte Instanz eines Prozesses, eines Vorkommens oder eines Hardwarezustands, wie von einer Anwendung definiert. Mit den Warnungsfunktionen können Anwendungen angeben, wann vordefinierte Ereignisse auftreten.

**Windows Server 2003:** Die Warnungs- und Messenger-Dienste sind auf Windows Server 2003 standardmäßig deaktiviert. Sie müssen die Dienste erneut aktivieren, bevor Sie die Warnungsfunktionen der Netzwerkverwaltung oder die Nachrichtenfunktionen der [Netzwerkverwaltung aufrufen.](message-functions.md)

Die Warnungsfunktionen sind im Folgenden aufgeführt.



| Funktion                                   | BESCHREIBUNG                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAlertR period**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | Benachrichtigt alle registrierten Clients, dass ein bestimmtes Ereignis aufgetreten ist.                                                                                                                                  |
| [**NetAlertRerklärex**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | Vereinfacht die Benachrichtigung registrierter Clients, dass ein bestimmtes Ereignis aufgetreten ist, da **NetAlertRerklär** im Gegensatz zu **NetAlertRandroEx** keine [**STD \_ ALERT-Struktur**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) erfordert. |



 

Der Warnungsdienst muss auf dem Clientcomputer ausgeführt werden, wenn Sie die **NetAlertR function** oder **die NetAlertRandroEx-Funktion** aufrufen. Wenn der Dienst nicht ausgeführt wird, tritt bei den Funktionen ein Fehler mit **\_ FEHLERDATEI \_ NICHT GEFUNDEN \_ auf.** Der Warnungsdienst auf dem Client ruft die [**NetMessageBufferSend-Funktion**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend) auf, um Informationen an Empfänger zu senden.

Anwendungen, Netzwerkdienste und interne Netzwerkkomponenten verwenden die Warnungsfunktionen der Netzwerkverwaltung, um eine Warnung zu erstellen und verschiedene Anwendungen oder Benutzer zu benachrichtigen, wenn eine bestimmte Art von Ereignis auftritt. Die Warnungskategoriefunktionen, Datentypen, Strukturen und Konstanten werden in LMCONS definiert. H, LMERR. H und LMALERT. H-Headerdateien. Um auf diese Definitionen zu zugreifen, definieren Sie die Konstanten INCL \_ NETERRORS und INCL NETALERT, und schließen \_ Sie die Headerdatei LM.H ein.

The LMALERT. Die H-Datei definiert die folgenden Warnungsklassen (Arten von Netzwerkereignissen) zum Senden von Warnungen:

-   Netzwerkereignisse, die Administrative Unterstützung erfordern
-   Addition eines Eintrags zu einer Fehlerprotokolldatei
-   Empfang einer Broadcastnachricht durch einen Benutzer oder eine Anwendung
-   Abschluss eines Druckauftrags
-   Verwendung bestimmter Anwendungen oder Ressourcen durch Benutzer

Sie können bei Bedarf andere Warnungsklassen für Netzwerkanwendungen definieren. Wenn beispielsweise eine Anwendung auf einem Server routinemäßig große Datenmengen auf ein Laufwerk schreibt, besteht das Risiko, dass die Anwendung den Datenträger füllt. In diesem Fall können Sie das Ereignis "Kein freier Speicherplatz" hinzufügen, um eine Warnung auszulösen, die die Anwendung darüber informiert, dass sie angehalten oder den Prozess beendet, der den Datenträger füllt. Der Ereignisname für eine Warnung kann eine beliebige Textzeichenfolge sein.

Wenn Sie eine Warnung mit einem Aufruf der [**NetAlertRadmin-Funktion**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise) ausgelöst haben, sollten die Nachrichtendaten aus einer [**STD \_ ALERT-Headerstruktur**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) gefolgt von zusätzlichen Daten fester Länge bestehen, die warnungsspezifisch in einer ADMIN [**OTHER \_ \_ INFO-,**](/windows/desktop/api/Lmalert/ns-lmalert-admin_other_info) [**ERRLOG \_ OTHER \_ INFO-,**](/windows/desktop/api/Lmalert/ns-lmalert-errlog_other_info) [**PRINT OTHER \_ \_ INFO-**](/windows/desktop/api/Lmalert/ns-lmalert-print_other_info)oder [**USER OTHER \_ \_ INFO-Struktur**](/windows/desktop/api/Lmalert/ns-lmalert-user_other_info) sind. Zusätzliche Daten variabler Länge können der warnungsspezifischen Struktur folgen. (Aufrufe der [**NetAlertRerklärEx-Funktion**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) erfordern keine **STD \_ ALERT-Struktur.)** Die aufrufende Anwendung muss den Arbeitsspeicher für alle Strukturen und Daten variabler Länge zuordnen und den Arbeitsspeicher nach der Rückgabe des Aufrufs frei geben.

Die folgenden Makros sind für die Verwendung mit Warnungsdatenpuffern verfügbar.



| Makro                                          | Beschreibung                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**WARNUNG \_ ANDERE \_ INFORMATIONEN**](/windows/desktop/api/Lmalert/nf-lmalert-alert_other_info) | Gibt einen Zeiger auf die Daten fester Länge zurück, die der **STD \_ ALERT-Struktur** in einer Warnmeldung folgen. |
| [**\_ \_ WARNUNGS-VAR-DATEN**](/windows/desktop/api/Lmalert/nf-lmalert-alert_var_data)     | Gibt einen Zeiger auf die Daten variabler Länge zurück, die auf die warnungsspezifischen Daten in einer Warnmeldung folgen.   |



 

Anstatt die Warnungsfunktionen der Netzwerkverwaltung zu verwenden, können Sie möglicherweise das Windows Management Instrumentation (WMI) SDK für Ereignisbenachrichtigungen verwenden. Weitere Informationen zu den Plattformen, die das WMI-Ereignismodell unterstützen, finden Sie [in](/windows/desktop/WmiSdk/monitoring-events) der WMI-Dokumentation unter [WMI-Infrastruktur](/windows/desktop/WmiSdk/wmi-infrastructure) und Überwachungsereignisse.

 

 