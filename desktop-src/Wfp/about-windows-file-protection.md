---
description: Windows-Ressourcenschutz (WRP) verhindert, dass wichtige Systemdateien, Ordner und Registrierungsschlüssel ersetzt werden, die als Teil des Betriebssystems installiert werden.
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: Informationen zu Windows-Ressourcenschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c102225a547c4e454c3fb67ac94f715cd3adf8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366131"
---
# <a name="about-windows-resource-protection"></a>Informationen zu Windows-Ressourcenschutz

Windows-Ressourcenschutz (WRP) verhindert, dass wichtige Systemdateien, Ordner und Registrierungsschlüssel ersetzt werden, die als Teil des Betriebssystems installiert werden. Es wurde ab Windows Server 2008 und Windows Vista verfügbar. Die Berechtigung für den Vollzugriff zum Ändern von durch WRP geschützten Ressourcen ist auf Treuhänder beschränkt. Durch WRP geschützte Ressourcen können nur mithilfe der [unterstützten Ressourcenaustausch Mechanismen](supported-file-replacement-mechanisms.md) mit dem Windows-Modul Installations Dienst geändert werden. Der Schutz dieser Ressourcen verhindert Anwendungs-und Betriebssystem Fehler.

Anwendungen sollten nicht versuchen, durch WRP geschützte Ressourcen zu ändern, da diese von Windows und anderen Anwendungen verwendet werden. Wenn eine Anwendung versucht, eine durch WRP geschützte Ressource zu ändern, kann dies folgende Ergebnisse haben:

-   Anwendungsinstallations Programme, die versuchen, wichtige Windows-Dateien oder Registrierungsschlüssel zu ersetzen, zu ändern oder zu löschen, können die Anwendung möglicherweise nicht installieren und erhalten eine Fehlermeldung, dass der Zugriff auf die Ressource verweigert wurde.
-   Anwendungen, die versuchen, Unterschlüssel hinzuzufügen oder zu entfernen oder die Werte geschützter Registrierungsschlüssel zu ändern, schlagen möglicherweise fehl, und es wird eine Fehlermeldung angezeigt, die besagt, dass der Zugriff auf die Ressource verweigert wurde.
-   Anwendungen, die auf das Schreiben von Informationen in geschützte Registrierungsschlüssel, Ordner oder Dateien angewiesen sind, können fehlschlagen.

WRP ist der neue Name für den Windows-Datei Schutz (WFP). WRP schützt Registrierungsschlüssel und Ordner sowie wichtige Systemdateien. WFP war in Microsoft Windows Server 2003 und Windows XP verfügbar. WRP ersetzt WFP in Windows Server 2008 und Windows Vista.

In den folgenden Themen wird WRP beschrieben:

-   [Liste geschützter Ressourcen](protected-file-list.md)
-   [Erkennen von Ressourcenaustausch](detecting-file-replacement.md)
-   [Unterstützte Mechanismen für die Ressourcen Ersetzung](supported-file-replacement-mechanisms.md)
-   [System File Checker](system-file-checker.md)
-   [Überlegungen zur Remote Verwaltung](remote-administration-considerations.md)

 

 



