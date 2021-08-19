---
title: Nachverfolgen von Änderungen
description: Einige Anwendungen müssen die Konsistenz zwischen bestimmten Daten, die im Active Directory-Verzeichnisdienst gespeichert sind, und anderen Daten gewährleisten.
ms.assetid: f4539482-1170-4c0c-b817-b39e58049d39
ms.tgt_platform: multiple
keywords:
- Active Directory,Verwenden,Nachverfolgen von Änderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3d8521fbd7b04d2c317246d81e0b9af7bce888bcc8e78b7bc9fcbbdd05b0c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024568"
---
# <a name="tracking-changes"></a>Nachverfolgen von Änderungen

Einige Anwendungen müssen die Konsistenz zwischen bestimmten Daten, die im Active Directory-Verzeichnisdienst gespeichert sind, und anderen Daten gewährleisten. Die anderen Daten können im Verzeichnis, in einer SQL Server Tabelle, in einer Datei oder in der Registrierung gespeichert werden. Wenn sich die im Verzeichnis gespeicherten Daten ändern, müssen sich die anderen Daten möglicherweise ändern, um konsistent zu bleiben. Zu den Anwendungen mit dieser Anforderung gehören:

In diesem Abschnitt werden die mechanismen, die von der Überwachung von Anwendungen verwendet werden, nicht behandelt. Dies sind Anwendungen, die Verzeichnisänderungen nicht überwachen, um konsistente Daten zwischen separaten Speichern zu verwalten, sondern als Systemverwaltungstool. Obwohl Überwachungsanwendungen die gleichen Mechanismen verwenden können, die Anwendungen zur Änderungsnachverfolgung unterstützen, sind die folgenden Mechanismen speziell für die Überwachung von Anwendungen konzipiert:

-   Sicherheitsüberwachung. Durch Ändern des SACL-Teils (System Access Control List) eines Objektsicherheitsdeskriptors können Sie bewirken, dass Zugriffe auf das Objekt auf einem bestimmten Domänencontroller Überwachungsdatensätze im Sicherheitsereignisprotokoll auf diesem Domänencontroller generieren. Sie können Lese-, Schreib- oder beides überwachen. Sie können das gesamte Objekt oder bestimmte Attribute überwachen. Weitere Informationen finden Sie unter [Abrufen der SACL eines Objekts](retrieving-an-objectampaposs-sacl.md) und Überwachen der [Generierung](/windows/desktop/SecAuthZ/audit-generation)von .
-   Ereignisprotokollierung Durch Ändern der Registrierungseinstellungen auf einem bestimmten Domänencontroller können Sie die Arten von Ereignissen ändern, die im Verzeichnisdienst-Ereignisprotokoll protokolliert werden. Um alle Änderungen zu protokollieren, legen Sie den Wert **8 Directory Access** unter dem folgenden Registrierungsschlüssel auf 4 fest.

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                NTDS
                   Diagnostics
    ```

    Weitere Informationen finden Sie unter [Ereignisprotokollierung.](/windows/desktop/EventLog/event-logging)

-   Ereignisablaufverfolgung Windows 2000 wurde eine Ereignisablaufverfolgungs-API zum Nachverfolgen und Protokollieren interessanter Ereignisse in Software oder Hardware eingeführt. Das Windows Betriebssystem und insbesondere Active Directory Domain Services unterstützen die Verwendung der Ereignisablaufverfolgung für die Kapazitätsplanung und detaillierte Leistungsanalyse. Weitere Informationen finden Sie unter [Ereignisablaufverfolgung](/windows/desktop/ETW/event-tracing-portal) und [Ereignisablaufverfolgung in ADSI.](/windows/desktop/ADSI/adsi-and-etw)

Dieser Abschnitt schließt folgende Themen ein:

-   [Übersicht über Änderungsnachverfolgung Techniken](overview-of-change-tracking-techniques.md)
-   [Änderungsbenachrichtigungen in Active Directory Domain Services](change-notifications-in-active-directory-domain-services.md)
-   [Abfragen von Änderungen mithilfe des DirSync-Steuerelements](polling-for-changes-using-the-dirsync-control.md)
-   [Abfragen von Änderungen mit USNChanged](polling-for-changes-using-usnchanged.md)

 

 