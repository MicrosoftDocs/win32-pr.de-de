---
description: Das Ersetzen geschützter Ressourcen wird durch die folgenden Mechanismen unterstützt.
ms.assetid: a757e6cf-59df-4894-a0dc-40174b0aa147
title: Unterstützte Mechanismen zum Ersetzen von Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8f839e65ddd07bbde6bb4e089c3235ee6930dec910c07c1c318e666b034afb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999250"
---
# <a name="supported-resource-replacement-mechanisms"></a>Unterstützte Mechanismen zum Ersetzen von Ressourcen

Das Ersetzen geschützter Ressourcen wird durch die folgenden Mechanismen unterstützt.

Die Berechtigung zum Ändern von WRP-geschützten Ressourcen unter Windows Vista und Windows Server 2008 ist mithilfe der folgenden Mechanismen auf TrustedInstaller mit dem Windows Modules Installer-Dienst beschränkt:

-   Windows Von TrustedInstaller installierte Service Packs.
-   Von TrustedInstaller installierte Hotfixes.
-   Von TrustedInstaller installierte Betriebssystemupgrades.
-   Windows Von TrustedInstaller installiertes Update.

Anwendungen und Installationsprogrammen, die versuchen, eine durch WRP geschützte Ressource durch andere Als diese angegebenen Methoden zu ersetzen, wird der Zugriff verweigert, um die Ressource zu ändern und eine Fehlermeldung "Zugriff verweigert" zu generieren.

Bei bekannten Installationsprogrammen, die versuchen, WRP-geschützte Ressourcen zu ersetzen, werden der Fehler und die Fehlermeldung "Zugriff verweigert" möglicherweise unterdrückt. In diesem Fall wird der Vorgang erfolgreich zurückgegeben, der Fehler und die Fehlermeldung werden unterdrückt, es werden jedoch keine Änderungen auf die WRP-geschützte Ressource angewendet. Der Fehler kann für ein bekanntes Installationsprogramm nur unterdrückt werden, wenn alle der folgenden Kriterien erfüllt sind:

-   Dies ist eine Legacyanwendung. Die Anwendung enthält kein Manifest mit einem requestedExecutionlevel, das die Anwendung identifiziert, die für Windows Vista oder Windows Server 2008 entworfen wurde.
-   Der Fehler "Zugriff verweigert" wird nur durch den Versuch verursacht, eine WRP-geschützte Ressource zu ändern.
-   Ein Administrator installiert die Anwendung.

Informationen zur Verwendung des Windows Installers mit WRP finden Sie unter [Using Windows Installer and Windows Resource Protection](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) im Windows [Installer](/windows/desktop/Msi/windows-installer-portal) SDK.

**Windows Server 2003 und Windows XP:** Das Ersetzen WFP-geschützter Systemdateien wird nur über die folgenden Mechanismen unterstützt:

-   Windows Service Pack-Installation mit Update.exe
-   Hotfixes, die mithilfe von Hotfix.exe
-   Betriebssystemupgrades mit Winnt32.exe
-   Windows-Update

Das Ersetzen geschützter Dateien durch andere Als diese angegebenen Methoden führt dazu, dass die ursprünglichen Dateien von WFP wiederhergestellt werden.

 

 
