---
description: Das Sicherheitsprotokoll ist für die Verwendung durch das System konzipiert. Benutzer können das Sicherheitsprotokoll jedoch lesen und löschen, wenn ihnen die berechtigung SE SECURITY NAME erteilt wurde \_ \_ (&\# 0034;Überwachung und Sicherheitsprotokoll verwalten&\# 0034; Benutzerrecht). Weitere Informationen finden Sie unter Berechtigungen.
ms.assetid: 861be39a-012e-473b-a2d3-2a8c7ba3adaa
title: Sicherheit der Ereignisprotokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52f6c801b061290ebb4d6f47fe78efebc09e1b2d23dc4a598dc9f97c1b3a46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151550"
---
# <a name="event-logging-security"></a>Sicherheit der Ereignisprotokollierung

Das **Sicherheitsprotokoll** ist für die Verwendung durch das System konzipiert. Benutzer können das Sicherheitsprotokoll  jedoch lesen und löschen, wenn ihnen die berechtigung SE SECURITY NAME (das Benutzerrecht "Überwachung und Sicherheitsprotokoll \_ \_ verwalten") erteilt wurde. Weitere Informationen finden Sie unter [Berechtigungen.](/windows/desktop/SecAuthZ/privileges)

Nur die lokale Sicherheitsstelle (local security authority, Lsass.exe) verfügt über schreibberechtigung für das **Sicherheitsprotokoll.** Dieses Privileg kann von keinem anderen Konto anfordern werden. Um ein Ereignis in das **Sicherheitsprotokoll zu** schreiben, verwenden Sie die [**FunktionHzReportSecurityEvent.**](/windows/desktop/api/authz/nf-authz-authzreportsecurityevent)

Der Zugriff auf **das Anwendungsprotokoll,** das **Systemprotokoll** und benutzerdefinierte Protokolle ist eingeschränkt. Das System gewährt Zugriff basierend auf den Zugriffsrechten, die dem Konto gewährt werden, unter dem der Thread ausgeführt wird. Die folgende Tabelle zeigt, welche Zugriffstypen für die Ereignisprotokollierungsfunktionen erforderlich sind.



| Zugriffsrecht                 | Beschreibung                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| ELF \_ LOGFILE \_ CLEAR (0x0004) | Erforderlich für [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga).                                                    |
| ELF \_ LOGFILE \_ READ (0x0001)  | Erforderlich für [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga) und [**OpenEventLog.**](/windows/desktop/api/Winbase/nf-winbase-openeventloga) |
| ELF \_ LOGFILE \_ WRITE (0x0002) | Erforderlich für [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea).                                        |



 

Verwenden Sie **den Registrierungswert CustomSD,** um die Sicherheit des Anwendungsprotokolls, des **Systemprotokolls** und der benutzerdefinierten Protokolle zu konfigurieren.  Weitere Informationen finden Sie unter [Eventlog Key](eventlog-key.md).

**Windows XP/2000:** In der folgenden Tabelle werden die Zugriffsrechte beschrieben, die für jedes Konto in jedem Protokoll gewährt werden.

| Protokoll wird erstellt             | Konto                 | Lesen | Schreiben | Clear |
|-----------------|-------------------------|------|-------|-------|
| **Anwendung** | Administratoren (System) | X    | X     | X     |
|                 | Administratoren (Domäne) | X    | X     | X     |
|                 | LocalSystem             | X    | X     | X     |
|                 | Interaktiver Benutzer        | X    | X     |       |
| **System**      | Administratoren (System) | X    | X     | X     |
|                 | Administratoren (Domäne) | X    |       | X     |
|                 | LocalSystem             | X    | X     | X     |
|                 | Interaktiver Benutzer        | X    |       |       |
| *Benutzerdefiniert*        | Administratoren (System) | X    | X     | X     |
|                 | Administratoren (Domäne) | X    | X     | X     |
|                 | LocalSystem             | X    | X     | X     |
|                 | Interaktiver Benutzer        | X    | X     |       |



 

Um den Mitgliedern des Gastkontos Zugriff zu gewähren, ändern Sie den folgenden Registrierungswert:

**HKEY \_ LOCAL \_ MACHINE** \\ **SYSTEM** \\ **CurrentControlSet** \\ **Services** \\ **EventLog** \\ *Log* \\ **RestrictGuestAccess**

 

 
