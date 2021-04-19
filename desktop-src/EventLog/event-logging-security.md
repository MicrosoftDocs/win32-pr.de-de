---
description: Das Sicherheitsprotokoll ist für die Verwendung durch das System vorgesehen. Allerdings können Benutzer das Sicherheitsprotokoll lesen und löschen, wenn Ihnen die Berechtigung "SE \_ Security Name" erteilt wurde \_ (das &\# 0034; Verwalten von Überwachungs-und Sicherheitsprotokollen&\# 0034; Benutzerrecht). Weitere Informationen finden Sie unter Berechtigungen.
ms.assetid: 861be39a-012e-473b-a2d3-2a8c7ba3adaa
title: Sicherheit der Ereignisprotokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4e2dce7318efeb6f26917bca1d6812eb32a343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348330"
---
# <a name="event-logging-security"></a>Sicherheit der Ereignisprotokollierung

Das **Sicherheits** Protokoll ist für die Verwendung durch das System vorgesehen. Allerdings können Benutzer das **Sicherheits** Protokoll lesen und löschen, wenn Ihnen die \_ Berechtigung zum Verwalten von Sicherheits Namen erteilt wurde \_ (das Benutzerrecht "Überwachungs-und Sicherheitsprotokoll verwalten"). Weitere Informationen finden Sie unter [Berechtigungen](/windows/desktop/SecAuthZ/privileges).

Nur die lokale Sicherheits Autorität (Lsass.exe) verfügt über Schreibberechtigungen für das **Sicherheits** Protokoll. Dieses Privileg kann von keinem anderen Konto angefordert werden. Verwenden Sie die [**authzreportsecurityevent**](/windows/desktop/api/authz/nf-authz-authzreportsecurityevent) -Funktion, um ein Ereignis in das **Sicherheits** Protokoll zu schreiben.

Der Zugriff auf das **Anwendungs** Protokoll, das **System** Protokoll und die benutzerdefinierten Protokolle ist eingeschränkt. Das System gewährt den Zugriff auf der Grundlage der Zugriffsrechte, die dem Konto erteilt werden, unter dem der Thread ausgeführt wird. In der folgenden Tabelle wird gezeigt, welche Zugriffs Typen für die Ereignis Protokollierungsfunktionen erforderlich sind.



| Zugriffsrecht                 | BESCHREIBUNG                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| ELF \_ Protokolldatei \_ Clear (0x0004) | Wird von [**cleareventlog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)benötigt.                                                    |
| ELF \_ Protokolldatei \_ Lesevorgang (0x0001)  | Erforderlich für [**openbackupeer ventlog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga) und [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga). |
| ELF \_ Protokolldatei \_ schreiben (0x0002) | Für " [**registereventsource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)" erforderlich.                                        |



 

Verwenden Sie den Registrierungs Wert **CustomSD** , um die Sicherheit des **Anwendungs** Protokolls, des **System** Protokolls und der benutzerdefinierten Protokolle zu konfigurieren. Weitere Informationen finden Sie unter [EventLog Key](eventlog-key.md).

**Windows XP/2000:** In der folgenden Tabelle werden die Zugriffsrechte beschrieben, die für jedes Konto in jedem Protokoll gewährt werden.

| Log             | Konto                 | Lesen | Schreiben | Clear |
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



 

Um dem Gast Konto Zugriff zu gewähren, ändern Sie den folgenden Registrierungs Wert:

**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **EventLog** \\ *Log* \\ **RestrictGuestAccess**

 

 
