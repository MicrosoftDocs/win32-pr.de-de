---
title: Verwenden des Neustart-Managers
description: In den folgenden Abschnitten wird die Verwendung der Restart Manager-API beschrieben.
ms.assetid: 78448d5e-20f6-45b6-b833-7d7791e5e4c6
keywords:
- 'Neustart-Manager: Neustarten von Mgr mit'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90826091aa4a3cdf39e0a1f063a211255ec4ef9cf84b06214eb172150ac3b8dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009998"
---
# <a name="using-restart-manager"></a>Verwenden des Neustart-Managers

In den folgenden Abschnitten wird die Verwendung der Restart Manager-API beschrieben. Ihre Anwendungen und Dienste sollten auch die [Richtlinien für Anwendungen und Dienste befolgen.](guidelines-for-applications-and-services.md)

## <a name="using-the-microsoft-windows-installer"></a>Verwenden des Microsoft Windows Installers

Microsoft [Windows Installer](/windows/desktop/Msi/windows-installer-portal) Version 4.0 ist der Anwendungsinstallationsdienst von Windows Vista oder Windows Server 2008. Anwendungen, die den Windows Installer Version 4.0 für die Installation und Wartung verwenden, verwenden automatisch den Neustart-Manager, um Systemneustarts zu reduzieren. Benutzerdefinierte Installationsprogramme können auch so entworfen werden, dass sie die Restart Manager-API aufrufen, um Anwendungen und Dienste direkt herunterzufahren und neu zu starten, um einen Systemneustart zu vermeiden. In Fällen, in denen ein Systemneustart unvermeidbar ist, können Installationsprogramme die [**Funktion InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) oder [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) verwenden, um sie so zu planen, dass die Unterbrechung für den Benutzer minimiert wird. Interaktive Windows Installer-Pakete sollten eine Benutzeroberfläche implementieren, die ein Dialogfeld [MsiRMFilesInUse](/windows/desktop/Msi/msirmfilesinuse-dialog) enthält. Weitere Informationen finden Sie unter [Using Windows Installer with Restart Manager (Verwenden von Windows Installer mit Restart Manager)](/windows/desktop/Msi/using-windows-installer-with-restart-manager) in der Windows Installer SDK-Dokumentation.

## <a name="using-the-restart-manager-api-with-custom-installers"></a>Verwenden der Neustart-Manager-API mit benutzerdefinierten Installationsprogrammen

Benutzerdefinierte Installationsprogramme oder ein Windows Installer-Paket, das benutzerdefinierte Aktionen enthält, die einen Systemneustart verursachen, können die Restart Manager-API verwenden, um Anwendungen und Dienste herunterzufahren und neu zu starten.

-   Alle Vorgänge, die mit der Restart Manager-API ausgeführt werden, müssen einer Sitzung zugeordnet werden. Auf dem System können maximal 64 Neustart-Manager-Sitzungen pro Benutzersitzung gleichzeitig geöffnet sein. Das primäre Installationsprogramm startet und beendet die Neustart-Manager-Sitzung. Weitere Informationen zur Verwendung von Restart Manager mit einem einzelnen Installationsprogramm finden Sie unter [Verwenden von Restart Manager mit einem primären Installationsprogramm.](using-restart-manager-with-a-primary-installer.md)
-   Wenn dies für die Installation erforderlich ist, kann mindestens ein sekundäres Installationsprogramm mit der Neustart-Manager-Sitzung verknüpft werden und entweder in-process oder out-of-process des primären Installationsprogramms ausgeführt werden. Sekundäre Installationsprogramme erfordern, dass der Sitzungsschlüssel vom primären Installationsprogramm bereitgestellt wird, um einer Sitzung beizutreten. Weitere Informationen und ein Beispiel für die Verwendung sekundärer Installationsprogramme finden Sie unter [Verwenden des Neustart-Managers mit einem sekundären Installationsprogramm.](using-restart-manager-with-a-secondary-installer.md)
-   Interaktive Installationsprogramme sollten eine Benutzeroberfläche implementieren, die ein [MsiRMFilesInUse-Dialogfeld](/windows/desktop/Msi/msirmfilesinuse-dialog) enthält, in dem Benutzer aufgefordert werden können, Anwendungen und Dienste zu schließen. Weitere Informationen finden Sie unter [Using Windows Installer with Restart Manager (Verwenden von Windows Installer mit Restart Manager)](/windows/desktop/Msi/using-windows-installer-with-restart-manager) in der Windows Installer SDK-Dokumentation.
-   Installationsprogramme können die Restart Manager-API aufrufen, um den Aktuellen Neustart-Manager-Vorgang zu ändern, abzubrechen und den Status abzurufen. Weitere Informationen finden Sie in den folgenden Themen: [Abrufen des Status eines Neustart-Manager-Vorgangs](getting-the-status-of-a-restart-manager-operation.md) und Abbrechen des [aktuellen Neustart-Manager-Vorgangs.](canceling-the-current-restart-manager-operation.md)
-   Installationsprogramme sollten die Dateisystemumleitung nicht deaktivieren, bevor sie die Restart Manager-API aufrufen. Einige 32-Bit-Installationsprogramme werden auf 64-Bit-Windows kann möglicherweise keine Datei im Verzeichnis %windir% \\ system32 registrieren.

 

 