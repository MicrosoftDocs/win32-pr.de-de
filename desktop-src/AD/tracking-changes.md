---
title: Nachverfolgen von Änderungen
description: Einige Anwendungen müssen die Konsistenz zwischen bestimmten Daten, die im Active Directory Directory-Dienst gespeichert sind, und anderen Daten beibehalten.
ms.assetid: f4539482-1170-4c0c-b817-b39e58049d39
ms.tgt_platform: multiple
keywords:
- Active Directory, verwenden, Nachverfolgen von Änderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dc772f883b97eb4e7305b39f0a582448a8bc021
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948540"
---
# <a name="tracking-changes"></a>Nachverfolgen von Änderungen

Einige Anwendungen müssen die Konsistenz zwischen bestimmten Daten, die im Active Directory Directory-Dienst gespeichert sind, und anderen Daten beibehalten. Die anderen Daten können im Verzeichnis, in einer SQL Server Tabelle, in einer Datei oder in der Registrierung gespeichert werden. Wenn sich im Verzeichnis gespeicherte Daten ändern, müssen die anderen Daten möglicherweise geändert werden, damit Sie konsistent bleiben. Anwendungen, die diese Anforderung erfüllen, umfassen Folgendes:

In diesem Abschnitt werden die von der Überwachung von Anwendungen verwendeten Mechanismen nicht behandelt. Dabei handelt es sich um Anwendungen, die Verzeichnisänderungen überwachen, nicht um konsistente Daten zwischen separaten speichern zu verwalten, sondern als System Verwaltungs Tool. Wenngleich Überwachungsanwendungen die gleichen Mechanismen verwenden können, die Anwendungen für die Änderungs Nachverfolgung unterstützen, sind die folgenden Mechanismen speziell für die Überwachung von Anwendungen konzipiert:

-   Sicherheitsüberwachung. Durch Ändern des Teils der System Zugriffs Steuerungs Liste (SACL) einer Objekt Sicherheits Beschreibung können Sie Zugriffe auf das-Objekt auf einem bestimmten Domänen Controller veranlassen, dass Überwachungsdaten Sätze im Sicherheits Ereignisprotokoll auf diesem Domänen Controller generiert werden. Sie können Lese-und Schreibvorgänge oder beides überwachen. Sie können das gesamte Objekt oder bestimmte Attribute überwachen. Weitere Informationen finden Sie unter [Abrufen der SACL](retrieving-an-objectampaposs-sacl.md) -und Überwachungs [Generierung](/windows/desktop/SecAuthZ/audit-generation)eines Objekts.
-   Ereignisprotokollierung Durch Ändern der Registrierungs Einstellungen auf einem bestimmten Domänen Controller können Sie die Arten von Ereignissen ändern, die in das Verzeichnisdienst-Ereignisprotokoll protokolliert werden. Um alle Änderungen zu protokollieren, legen Sie den **8-Verzeichniszugriffs** Wert unter dem folgenden Registrierungsschlüssel auf 4 fest.

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                NTDS
                   Diagnostics
    ```

    Weitere Informationen finden Sie unter [Ereignisprotokollierung](/windows/desktop/EventLog/event-logging).

-   Ereignisablaufverfolgung In Windows 2000 wurde eine Ereignis Ablauf Verfolgungs-API für die Ablauf Verfolgung und Protokollierung interessanter Ereignisse in Software oder Hardware eingeführt. Das Windows-Betriebssystem und Active Directory Domain Services insbesondere die Verwendung der Ereignis Ablauf Verfolgung für die Kapazitätsplanung und detaillierte Leistungsanalyse unterstützen. Weitere Informationen finden Sie unter [Ereignis Ablauf Verfolgung](/windows/desktop/ETW/event-tracing-portal) und [Ereignis Ablauf Verfolgung in ADSI](/windows/desktop/ADSI/adsi-and-etw).

Dieser Abschnitt schließt folgende Themen ein:

-   [Übersicht über Änderungsnachverfolgung Techniken](overview-of-change-tracking-techniques.md)
-   [Ändern von Benachrichtigungen in Active Directory Domain Services](change-notifications-in-active-directory-domain-services.md)
-   [Abrufen von Änderungen mithilfe des Dirsync-Steuer Elements](polling-for-changes-using-the-dirsync-control.md)
-   [Abrufen von Änderungen mithilfe von ""](polling-for-changes-using-usnchanged.md)

 

 