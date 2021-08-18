---
description: Windows Resource Protection (WRP) verhindert den Austausch wichtiger Systemdateien, Ordner und Registrierungsschlüssel, die als Teil des Betriebssystems installiert werden.
ms.assetid: 39069f57-d9f6-4890-ba87-37175184d7a2
title: Informationen zu Windows Resource Protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d06110c668e48a401cc329d79982e7c1b2746408ce45da9b7b3dffaca40b85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134197"
---
# <a name="about-windows-resource-protection"></a>Informationen zu Windows Resource Protection

Windows Resource Protection (WRP) verhindert den Austausch wichtiger Systemdateien, Ordner und Registrierungsschlüssel, die als Teil des Betriebssystems installiert werden. Es wurde ab Windows Server 2008 und Windows Vista verfügbar. Die Berechtigung für vollzugriff zum Ändern von WRP-geschützten Ressourcen ist auf TrustedInstaller beschränkt. WRP-geschützte Ressourcen können nur mithilfe der [unterstützten Ressourcenersetzungsmechanismen](supported-file-replacement-mechanisms.md) mit dem Installerdienst für Windows Module geändert werden. Der Schutz dieser Ressourcen verhindert Anwendungs- und Betriebssystemfehler.

Anwendungen sollten nicht versuchen, WRP-geschützte Ressourcen zu ändern, da diese von Windows und anderen Anwendungen verwendet werden. Wenn eine Anwendung versucht, eine WRP-geschützte Ressource zu ändern, kann sie die folgenden Ergebnisse haben.

-   Anwendungsinstallationsprogramme, die versuchen, wichtige Windows Dateien oder Registrierungsschlüssel zu ersetzen, zu ändern oder zu löschen, können die Anwendung möglicherweise nicht installieren und erhalten eine Fehlermeldung mit dem Hinweis, dass der Zugriff auf die Ressource verweigert wurde.
-   Anwendungen, die versuchen, Unterschlüssel hinzuzufügen oder zu entfernen oder die Werte von geschützten Registrierungsschlüsseln zu ändern, können fehlschlagen und erhalten eine Fehlermeldung mit dem Hinweis, dass der Zugriff auf die Ressource verweigert wurde.
-   Anwendungen, die informationen in geschützte Registrierungsschlüssel, Ordner oder Dateien schreiben, können fehlschlagen.

WRP ist der neue Name für Windows File Protection (WFP). WRP schützt Registrierungsschlüssel und -ordner sowie wichtige Systemdateien. WFP war in Microsoft Windows Server 2003 und Windows XP verfügbar. WRP ersetzt WFP in Windows Server 2008 und Windows Vista.

In den folgenden Themen wird WRP beschrieben:

-   [Liste der geschützten Ressourcen](protected-file-list.md)
-   [Erkennen des Ressourcenaustauschs](detecting-file-replacement.md)
-   [Unterstützte Ressourcenersetzungsmechanismen](supported-file-replacement-mechanisms.md)
-   [System File Checker](system-file-checker.md)
-   [Überlegungen zur Remoteverwaltung](remote-administration-considerations.md)

 

 



