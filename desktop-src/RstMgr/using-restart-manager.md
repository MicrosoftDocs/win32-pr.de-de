---
title: Verwenden des Neustart-Managers
description: In den folgenden Abschnitten wird die Verwendung der Neustart-Manager-API beschrieben.
ms.assetid: 78448d5e-20f6-45b6-b833-7d7791e5e4c6
keywords:
- Neustart-Manager neu starten, Verwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e4ac72edb9f2395bbd67236806c3ab3029372cc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858413"
---
# <a name="using-restart-manager"></a>Verwenden des Neustart-Managers

In den folgenden Abschnitten wird die Verwendung der Neustart-Manager-API beschrieben. Ihre Anwendungen und Dienste sollten auch die [Richtlinien für Anwendungen und Dienste](guidelines-for-applications-and-services.md)einhalten.

## <a name="using-the-microsoft-windows-installer"></a>Verwenden des Microsoft Windows Installer

Der [Microsoft Windows Installer](/windows/desktop/Msi/windows-installer-portal) Version 4,0 ist der Anwendungsinstallations Dienst von Windows Vista oder Windows Server 2008. Anwendungen, die die Windows Installer Version 4,0 für die Installation und Wartung verwenden, verwenden automatisch den Neustart-Manager, um die Systemneustarts zu verringern. Benutzerdefinierte Installationsprogramme können auch so entworfen werden, dass Sie die Neustart-Manager-API zum direkten Herunterfahren und Neustarten von Anwendungen und Diensten für den Systemneustart benötigen. In Fällen, in denen ein Systemneustart unvermeidlich ist, können Installer die [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) -oder [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) -Funktion verwenden, um Sie so zu planen, dass Sie die Unterbrechung des Benutzers minimiert. Interaktive Windows Installer Pakete sollten eine Benutzeroberfläche implementieren, die ein [msirmfilesinuse](/windows/desktop/Msi/msirmfilesinuse-dialog) -Dialogfeld enthält. Weitere Informationen finden Sie unter [Verwenden von Windows Installer mit dem Neustart-Manager](/windows/desktop/Msi/using-windows-installer-with-restart-manager) in der Windows Installer SDK-Dokumentation.

## <a name="using-the-restart-manager-api-with-custom-installers"></a>Verwenden der Neustart-Manager-API mit benutzerdefinierten Installationsprogrammen

Benutzerdefinierte Installationsprogramme oder ein Windows Installer Paket, das benutzerdefinierte Aktionen enthält, die einen Systemneustart verursachen, können die Neustart-Manager-API verwenden, um Anwendungen und Dienste herunterzufahren und neu zu starten.

-   Alle Vorgänge, die mit der Neustart-Manager-API ausgeführt werden, müssen einer-Sitzung zugeordnet werden. Maximal 64 Neustart-Manager-Sitzungen pro Benutzersitzung können gleichzeitig auf dem System geöffnet werden. Das primäre Installationsprogramm startet und beendet die Neustart-Manager-Sitzung. Weitere Informationen zum Verwenden des Neustart-Managers mit einem einzelnen Installationsprogramm finden Sie unter Verwenden des Neustart-Managers [mit einem primären Installations](using-restart-manager-with-a-primary-installer.md)Programm.
-   Wenn dies für die Installation erforderlich ist, kann mindestens ein sekundäres Installationsprogramm mit der Neustart-Manager-Sitzung verknüpft werden und kann entweder in-Process oder außerhalb des Prozesses des primären Installers ausgeführt werden. Sekundäre Installer erfordern, dass der Sitzungsschlüssel vom primären Installer bereitgestellt wird, um einer Sitzung beizutreten. Weitere Informationen und ein Beispiel für die Verwendung sekundärer Installer finden Sie unter [Verwenden des Neustart-Managers mit einem sekundären Installations](using-restart-manager-with-a-secondary-installer.md)Programm.
-   Interaktive Installationsprogramme sollten eine Benutzeroberfläche implementieren, die ein [msirmfilesinuse](/windows/desktop/Msi/msirmfilesinuse-dialog) -Dialogfeld enthält, in dem Benutzer aufgefordert werden, Anwendungen und Dienste zu schließen. Weitere Informationen finden Sie unter [Verwenden von Windows Installer mit dem Neustart-Manager](/windows/desktop/Msi/using-windows-installer-with-restart-manager) in der Windows Installer SDK-Dokumentation.
-   Installationsprogramme können die API für den Neustart-Manager zum ändern, Abbrechen und Abrufen des Status des aktuellen Vorgangs für den Neustart-Manager aufruft. Weitere Informationen finden Sie in den folgenden Themen: Abrufen [des Status eines Neustart-Manager-Vorgangs](getting-the-status-of-a-restart-manager-operation.md) und [Abbrechen des aktuellen Vorgangs für den Neustart-Manager](canceling-the-current-restart-manager-operation.md).
-   Installationsprogramme sollten die Dateisystem Umleitung nicht deaktivieren, bevor Sie die Neustart-Manager-API aufrufen. Einige 32-Bit-Installationsprogramme, die auf 64-Bit-Windows ausgeführt werden, können eine Datei im Verzeichnis "% windir% System32" möglicherweise nicht registrieren \\ .

 

 