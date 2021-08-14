---
description: Anwendungen, die Windows Installer 4.0 für die Installation und Wartung auf Windows Vista verwenden, verwenden automatisch den Neustart-Manager, um Systemneustarts zu reduzieren.
ms.assetid: 821739ff-f7a7-4192-ad34-254aa7d74d13
title: Verwenden Windows Installers mit dem Neustart-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf361cf20d6f56dc25bd43c9077c65a25eeebdae1c6b512dfcde3e756448a7b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141150"
---
# <a name="using-windows-installer-with-restart-manager"></a>Verwenden Windows Installers mit dem Neustart-Manager

Anwendungen, die Windows Installer 4.0 für die Installation und Wartung unter Windows Vista verwenden, verwenden automatisch den [Neustart-Manager,](../rstmgr/restart-manager-portal.md) um Systemneustarts zu reduzieren. Das Standardverhalten auf Windows Vista ist das Herunterfahren von Anwendungen, anstatt das Betriebssystem nach Möglichkeit herunter- und neu zu starten. In Fällen, in denen ein Systemneustart nicht möglich ist, können Installationsprogramme die [Restart Manager-API](../rstmgr/restart-manager-portal.md) verwenden, um Neustarts so zu planen, dass die Unterbrechung des Benutzerarbeitsablaufs minimiert wird.

Windows Installerentwickler können die folgenden Aktionen ausführen, um ihr Paket für die Arbeit mit dem [Neustart-Manager vorzubereiten.](../rstmgr/restart-manager-portal.md)

-   Fügen Sie ihrem [Paket das Dialogfeld MsiRMFilesInUse](msirmfilesinuse-dialog.md) hinzu. Wenn das Dialogfeld MsiRMFilesInUse im Paket vorhanden ist, erhält der Windows Vista-Benutzer, der eine Installation auf der Benutzeroberflächenebene "Vollständige Benutzeroberfläche" ausgeführt, die Möglichkeit, Anwendungen automatisch zu schließen und neu zu starten. [](user-interface-levels.md) Ein Installationspaket kann Informationen sowohl für das Dialogfeld MsiRMFilesInUse als auch für das [Dialogfeld FilesInUse](filesinuse-dialog.md) enthalten. Das Dialogfeld MsiRMFilesInUse wird nur angezeigt, wenn das Paket mit mindestens Windows Installer 4.0 unter Windows Vista installiert ist und andernfalls ignoriert wird. Vorhandene Pakete, die nicht über das Dialogfeld MsiRMFilesInUse verfügen, funktionieren weiterhin über das Dialogfeld FilesInUse. Eine Anpassungstransformation kann verwendet werden, um vorhandenen Paketen ein Dialogfeld MsiRMFilesInUse hinzuzufügen.

    Endbenutzer führen Installationen in der Regel auf der Benutzeroberflächenebene ["Vollständige Benutzeroberfläche" aus.](user-interface-levels.md) Installationen der einfachen Benutzeroberfläche oder der reduzierten Benutzeroberflächenebene bieten dem Benutzer die Möglichkeit, den [Neustart-Manager](../rstmgr/restart-manager-portal.md) zu verwenden, um Systemneustarts zu reduzieren, auch wenn das [Dialogfeld MsiRMFilesInUse](msirmfilesinuse-dialog.md) nicht vorhanden ist. Automatische Installationen auf Benutzeroberflächenebene fahren Anwendungen und Dienste immer herunter, und verwenden Sie Windows Vista immer den Neustart-Manager.

-   Registrieren Sie Anwendungen für einen Neustart mithilfe der [**RegisterApplicationRestart-Funktion.**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart) Restart Manager kann nur Anwendungen neu starten, die für den Neustart registriert wurden. Der Neustart-Manager startet registrierte Anwendungen nach der Installation neu. Wenn die Installation einen Systemneustart erfordert, startet restart Manager die registrierte Anwendung nach dem Systemneustart neu.
-   Geben Sie INSTALLLOGMODE RMFILESINUSE an, wenn Sie einen externen Benutzeroberflächenhandler mit den \_ [**Funktionen MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) und [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord) aktivieren. Windows Das Installationsprogramm sendet eine INSTALLMESSAGE \_ RMFILESINUSE-Nachricht für externe Benutzeroberflächenhandler, die den [Neustart-Manager unterstützen.](../rstmgr/restart-manager-portal.md) Wenn keine registrierte oder interne Benutzeroberfläche die INSTALLMESSAGE RMFILESINUSE-Nachricht verarbeitet, sendet das Installationsprogramm eine INSTALLMESSAGE FILESINUSE-Nachricht für Benutzeroberflächenhandler, die das \_ \_ Dialogfeld [FilesInUse](filesinuse-dialog.md) unterstützen. Weitere Informationen finden Sie unter [Verwenden des Neustart-Managers mit einer externen Benutzeroberfläche.](using-restart-manager-with-an-external-ui-.md)
-   Benutzerdefinierte Aktionen können Ressourcen hinzufügen, die zu einer [Neustart-Manager-Sitzung](../rstmgr/restart-manager-portal.md) gehören. Die benutzerdefinierte Aktion sollte vor der [InstallValidate-Aktion sequenziert](installvalidate-action.md) werden. Benutzerdefinierte Aktionen können die [**MsiRestartManagerSessionKey-Eigenschaft**](msirestartmanagersessionkey.md) verwenden, um den Sitzungsschlüssel abzurufen, und sollten die [**RmJoinSession-**](/windows/win32/api/restartmanager/nf-restartmanager-rmjoinsession) und [**RmEndSession-Funktionen**](/windows/win32/api/restartmanager/nf-restartmanager-rmendsession) der Restart Manager-API aufrufen. Benutzerdefinierte Aktionen können keine Ressourcen entfernen, die zu einer Neustart-Manager-Sitzung gehören. Benutzerdefinierte Aktionen sollten nicht versuchen, Anwendungen mithilfe der [**Funktionen RmShutdown,**](/windows/win32/api/restartmanager/nf-restartmanager-rmshutdown) [**RmGetList**](/windows/win32/api/restartmanager/nf-restartmanager-rmgetlist) und [**RmRestart**](/windows/win32/api/restartmanager/nf-restartmanager-rmrestart) herunter- oder neu zu starten.
-   Paketautoren können eine Bedingung in der [LaunchCondition-Tabelle](launchcondition-table.md) auf der [**MsiSystemRebootPending-Eigenschaft**](msisystemrebootpending.md) erstellen, um die Installation ihres Pakets zu verhindern, wenn ein Systemneustart aussteht.
-   Paketautoren und -administratoren können die Interaktion von Windows Installer und Restart Manager mithilfe der Eigenschaften [**MSIRESTARTMANAGERCONTROL,**](msirestartmanagercontrol.md) [**MSIDISABLERMRESTART,**](msidisablermrestart.md) [**MSIRMSHUTDOWN**](msirmshutdown.md) und [DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md) steuern.
-   Anwendungen und Dienste sollten die Richtlinien befolgen, die im Abschnitt Verwenden des [Neustart-Managers](../rstmgr/using-restart-manager.md) der [Restart Manager-Dokumentation beschrieben](../rstmgr/restart-manager-portal.md) sind.

 

 
