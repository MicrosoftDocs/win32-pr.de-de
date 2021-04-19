---
description: Die Ersetzung geschützter Ressourcen wird durch die folgenden Mechanismen unterstützt.
ms.assetid: a757e6cf-59df-4894-a0dc-40174b0aa147
title: Unterstützte Mechanismen für die Ressourcen Ersetzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2aaaa1d9cc8d24d8cd172be71ee40790bf8161a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368992"
---
# <a name="supported-resource-replacement-mechanisms"></a>Unterstützte Mechanismen für die Ressourcen Ersetzung

Die Ersetzung geschützter Ressourcen wird durch die folgenden Mechanismen unterstützt.

Die Berechtigung für den vollständigen Zugriff zum Ändern von durch WRP geschützten Ressourcen unter Windows Vista und Windows Server 2008 ist auf die Treuhänder mit dem Windows modules Installer-Dienst beschränkt, indem die folgenden Mechanismen verwendet werden:

-   Windows Service Packs, die von Treuhänder installiert werden.
-   Von Treuhänder installierte Hotfixes.
-   Betriebssystem Upgrades, die von Treuhänder installiert werden.
-   Windows Update von Treuhänder installiert.

Anwendungen und Installationsprogramme, die versuchen, eine durch WRP geschützte Ressource durch andere Methoden als die angegebenen Methoden zu ersetzen, wird der Zugriff zum Ändern der Ressource und Generieren einer Fehlermeldung "Zugriff verweigert" verweigert.

Für bekannte Installationsprogramme, die versuchen, durch WRP geschützte Ressourcen zu ersetzen, wird möglicherweise der Fehler "Zugriff verweigert" und die Fehlermeldung unterdrückt. In diesem Fall wird der Vorgang erfolgreich zurückgegeben, und die Fehlermeldung und die Fehlermeldung werden unterdrückt, aber auf die durch WRP geschützte Ressource werden keine Änderungen angewendet. Der Fehler wird möglicherweise nur für einen bekannten Installer unterdrückt, wenn alle der folgenden Kriterien erfüllt sind:

-   Dies ist eine Legacy Anwendung. Die Anwendung enthält kein Manifest mit einem requestedExecutionLevel, das die Anwendung identifiziert, die für Windows Vista oder Windows Server 2008 entworfen wurde.
-   Der Fehler "Zugriff verweigert" wird nur durch den Versuch verursacht, eine durch WRP geschützte Ressource zu ändern.
-   Ein Administrator installiert die Anwendung.

Weitere Informationen zum Verwenden der Windows Installer mit WRP finden Sie unter [Verwenden von Windows Installer und Windows-Ressourcenschutz](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) im [Windows Installer](/windows/desktop/Msi/windows-installer-portal) SDK.

**Windows Server 2003 und Windows XP:** Die Ersetzung von WFP-geschützten Systemdateien wird nur durch die folgenden Mechanismen unterstützt:

-   Windows Service Pack-Installation mit Update.exe
-   Mit Hotfix.exe installierte Hotfixes
-   Betriebssystem Upgrades mithilfe von Winnt32.exe
-   Windows-Update

Das Ersetzen geschützter Dateien durch andere Methoden als die angegebenen Methoden führt dazu, dass die ursprünglichen Dateien von WFP wieder hergestellt werden.

 

 
