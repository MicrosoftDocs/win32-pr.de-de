---
description: Der Installer führt standardmäßig benutzerdefinierte Aktionen mit Benutzerberechtigungen aus, um den Zugriff auf benutzerdefinierte Aktionen auf das System zu beschränken.
ms.assetid: 62a3d103-a786-4727-b757-3a8229c8a53f
title: Sicherheit für benutzerdefinierte Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7d36e0e5c6cecc61730144fb7efdeed63ba0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349759"
---
# <a name="custom-action-security"></a>Sicherheit für benutzerdefinierte Aktionen

Der Installer führt standardmäßig benutzerdefinierte Aktionen mit Benutzerberechtigungen aus, um den Zugriff auf benutzerdefinierte Aktionen auf das System zu beschränken. Der Installer kann benutzerdefinierte Aktionen mit erhöhten Rechten ausführen, wenn eine verwaltete Anwendung installiert wird oder wenn die System Richtlinie für erweiterte Berechtigungen angegeben wurde.

Verwenden Sie zum Verhindern der Protokollierung sensibler Informationen, die von der benutzerdefinierten Aktion verwendet werden, die [**msihiddenproperties**](msihiddenproperties.md) -Eigenschaft und **msidbcustomaction typehidetarget** . Weitere Informationen zu **msidbcustomaction typehidetarget** finden Sie unter ausgeblendete [Ziel Option für benutzerdefinierte Aktionen](custom-action-hidden-target-option.md).

Deaktivieren Sie die Eigenschaft customaktiondata, nachdem Sie Sie festgelegt haben, um sicherzustellen, dass sensible Daten nicht mehr verfügbar sind. Der folgende Beispielcode zeigt einen Code Ausschnitt, der von einer unmittelbaren benutzerdefinierten DLL-Aktion verwendet wird, die Daten für die Verwendung durch eine verzögerte benutzerdefinierte Aktion mit dem Namen "mydeferredca" festlegt:


```C++
#include <windows.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall MyImmediateCA(MSIHANDLE hInstall)
{
    // set up information for deferred custom action called MyDeferredCA
    const TCHAR szValue[] = TEXT("data");
    UINT uiStat = ERROR_INSTALL_FAILURE;
    if (ERROR_SUCCESS == MsiSetProperty(hInstall, TEXT("MyDeferredCA"), szValue))
    {
        uiStat = MsiDoAction(hInstall, TEXT("MyDeferredCA"));

        // clear CustomActionData property
        if (ERROR_SUCCESS != MsiSetProperty(hInstall, TEXT("MyDeferredCA"), TEXT("")))
            return ERROR_INSTALL_FAILURE;
    }

    return (uiStat == ERROR_SUCCESS) ? uiStat : ERROR_INSTALL_FAILURE;    
}
```



Beachten Sie, dass [benutzerdefinierte Aktionen für die verzögerte Ausführung](deferred-execution-custom-actions.md) nur das **msidbcustomaktiontypoidentitäts Ate** -Attribut verwenden können. Weitere Informationen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).

Wenn das **msidbcustomaction typoidentitäts** -Bit nicht für eine benutzerdefinierte Aktion festgelegt ist, führt das Installationsprogramm die benutzerdefinierte Aktion mit Berechtigungen auf Benutzerebene aus. Weitere Informationen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).

Wenn das **msidbcustomaction typoidentitäts Ate** -Bit festgelegt ist und eine verwaltete Anwendung mit der Administrator Berechtigung installiert wird, kann das Installationsprogramm die benutzerdefinierte Aktion mit erhöhten Rechten ausführen. Wenn ein Benutzer jedoch versucht, die verwaltete Anwendung ohne Administrator Berechtigung zu installieren, führt das Installationsprogramm die Anwendung mit Berechtigungen auf Benutzerebene aus, und zwar unabhängig davon, ob **msidbcustomaktiontycuoidentitäts Ate** festgelegt ist.

Beachten Sie, dass eine benutzerdefinierte Aktion auch dann mit System Privilegien ausgeführt werden kann, wenn das **msidbcustomaction typoidentitäts Ate** -Bit nicht festgelegt ist. Dies tritt auf, wenn ein Administrator die Anwendung für alle Benutzer auf einem Server installiert, auf dem der Terminal Server-Rollen Dienst mit Windows 2000 ausgeführt wird, und die Aktion nicht mit " **msidbcustomaction typetsaware**" gekennzeichnet ist. Eine benutzerdefinierte Aktion kann auch mit System Privilegien ausgeführt werden, wenn die Installation aufgerufen wird, wenn kein Benutzer Kontext vorhanden ist. Dies ist beispielsweise der Fall, wenn während einer von der Windows 2000-Anwendungs Bereitstellung aufgerufenen Installation kein aktuell angemeldeter Benutzer vorhanden ist.

Wenn Sie eigene benutzerdefinierte Aktionen erstellen, sollten Sie die benutzerdefinierte Aktion immer mit sicheren Methoden erstellen. Weitere Informationen finden Sie unter [Richtlinien zum Sichern von benutzerdefinierten Aktionen](guidelines-for-securing-custom-actions.md).

 

 



