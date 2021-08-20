---
description: Das Installationsprogramm führt standardmäßig benutzerdefinierte Aktionen mit Benutzerberechtigungen aus, um den Zugriff benutzerdefinierter Aktionen auf das System zu beschränken.
ms.assetid: 62a3d103-a786-4727-b757-3a8229c8a53f
title: Sicherheit für benutzerdefinierte Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0a8011640bea177ec253f555b6ff83302541b640a050ccf861eb345c58ca13f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143310"
---
# <a name="custom-action-security"></a>Sicherheit für benutzerdefinierte Aktionen

Das Installationsprogramm führt standardmäßig benutzerdefinierte Aktionen mit Benutzerberechtigungen aus, um den Zugriff benutzerdefinierter Aktionen auf das System zu beschränken. Das Installationsprogramm kann benutzerdefinierte Aktionen mit erhöhten Rechten ausführen, wenn eine verwaltete Anwendung installiert wird oder die Systemrichtlinie für erhöhte Rechte angegeben wurde.

Sie sollten die [**MsiHiddenProperties-Eigenschaft**](msihiddenproperties.md) und **msidbCustomActionTypeHideTarget** verwenden, um die Protokollierung vertraulicher Informationen zu verhindern, die von der benutzerdefinierten Aktion verwendet werden. Weitere Informationen zu **msidbCustomActionTypeHideTarget finden** Sie unter [Option "Benutzerdefinierte Aktion ausgeblendetes Ziel".](custom-action-hidden-target-option.md)

Löschen Sie die CustomActionData-Eigenschaft nach dem Festlegen, um sicherzustellen, dass vertrauliche Daten nicht mehr verfügbar sind. Der folgende Beispielcode ist ein Codeausschnitt, der von einer unmittelbaren benutzerdefinierten DLL-Aktion verwendet wird, die Daten für die Verwendung durch eine zurückgestellte benutzerdefinierte Aktion namens "MyDeferredCA" einsetzt:


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



Beachten Sie, dass nur benutzerdefinierte Aktionen [mit verzögerter](deferred-execution-custom-actions.md) Ausführung das **Attribut msidbCustomActionTypeNoImpersonate verwenden** können. Weitere Informationen finden Sie unter [Benutzerdefinierte Aktion In-Script Ausführungsoptionen](custom-action-in-script-execution-options.md).

Wenn das **bit msidbCustomActionTypeNoImpersonate** nicht für eine benutzerdefinierte Aktion festgelegt ist, führt das Installationsprogramm die benutzerdefinierte Aktion mit Berechtigungen auf Benutzerebene aus. Weitere Informationen finden Sie unter [Benutzerdefinierte Aktion In-Script Ausführungsoptionen.](custom-action-in-script-execution-options.md)

Wenn **das msidbCustomActionTypeNoImpersonate-Bit** festgelegt ist und eine verwaltete Anwendung mit Administratorberechtigung installiert wird, kann das Installationsprogramm die benutzerdefinierte Aktion mit erhöhten Rechten ausführen. Wenn ein Benutzer jedoch versucht, die verwaltete Anwendung ohne Administratorberechtigung zu installieren, führt das Installationsprogramm die Anwendung mit Berechtigungen auf Benutzerebene aus, unabhängig davon, ob **msidbCustomActionTypeNoImpersonate** festgelegt ist.

Beachten Sie, dass eine benutzerdefinierte Aktion mit Systemberechtigungen ausgeführt werden kann, auch wenn das **msidbCustomActionTypeNoImpersonate-Bit** nicht festgelegt ist. Dies tritt auf, wenn ein Administrator die Anwendung für alle Benutzer auf einem Server installiert, auf dem der Terminalserver-Rollendienst mithilfe von Windows 2000 ausgeführt wird, und die Aktion nicht mit **msidbCustomActionTypeTSAware** gekennzeichnet ist. Eine benutzerdefinierte Aktion kann auch mit Systemberechtigungen ausgeführt werden, wenn die Installation aufgerufen wird, wenn kein Benutzerkontext vorgefertigt ist. Wenn beispielsweise während einer Installation, die von der 2000-Anwendungsbereitstellung aufgerufen wird, kein Windows benutzer angemeldet ist.

Beim Erstellen eigener benutzerdefinierter Aktionen sollten Sie die benutzerdefinierte Aktion immer mit sicheren Methoden erstellen. Weitere Informationen finden Sie unter [Richtlinien zum Schützen benutzerdefinierter Aktionen.](guidelines-for-securing-custom-actions.md)

 

 



