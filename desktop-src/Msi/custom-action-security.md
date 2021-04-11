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
# <a name="custom-action-security"></a><span data-ttu-id="b186e-103">Sicherheit für benutzerdefinierte Aktionen</span><span class="sxs-lookup"><span data-stu-id="b186e-103">Custom Action Security</span></span>

<span data-ttu-id="b186e-104">Der Installer führt standardmäßig benutzerdefinierte Aktionen mit Benutzerberechtigungen aus, um den Zugriff auf benutzerdefinierte Aktionen auf das System zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="b186e-104">The installer runs custom actions with user privileges by default in order to limit the access of custom actions to the system.</span></span> <span data-ttu-id="b186e-105">Der Installer kann benutzerdefinierte Aktionen mit erhöhten Rechten ausführen, wenn eine verwaltete Anwendung installiert wird oder wenn die System Richtlinie für erweiterte Berechtigungen angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="b186e-105">The installer may run custom actions with elevated privileges if a managed application is being installed or if the system policy has been specified for elevated privileges.</span></span>

<span data-ttu-id="b186e-106">Verwenden Sie zum Verhindern der Protokollierung sensibler Informationen, die von der benutzerdefinierten Aktion verwendet werden, die [**msihiddenproperties**](msihiddenproperties.md) -Eigenschaft und **msidbcustomaction typehidetarget** .</span><span class="sxs-lookup"><span data-stu-id="b186e-106">You should use the [**MsiHiddenProperties**](msihiddenproperties.md) property and **msidbCustomActionTypeHideTarget** to prevent logging of sensitive information used by the custom action.</span></span> <span data-ttu-id="b186e-107">Weitere Informationen zu **msidbcustomaction typehidetarget** finden Sie unter ausgeblendete [Ziel Option für benutzerdefinierte Aktionen](custom-action-hidden-target-option.md).</span><span class="sxs-lookup"><span data-stu-id="b186e-107">For more information about **msidbCustomActionTypeHideTarget** see [Custom Action Hidden Target Option](custom-action-hidden-target-option.md).</span></span>

<span data-ttu-id="b186e-108">Deaktivieren Sie die Eigenschaft customaktiondata, nachdem Sie Sie festgelegt haben, um sicherzustellen, dass sensible Daten nicht mehr verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b186e-108">Clear the CustomActionData property after setting it to ensure that sensitive data is no longer available.</span></span> <span data-ttu-id="b186e-109">Der folgende Beispielcode zeigt einen Code Ausschnitt, der von einer unmittelbaren benutzerdefinierten DLL-Aktion verwendet wird, die Daten für die Verwendung durch eine verzögerte benutzerdefinierte Aktion mit dem Namen "mydeferredca" festlegt:</span><span class="sxs-lookup"><span data-stu-id="b186e-109">Example code below is a snippet used by an immediate DLL custom action that is setting up data for use by a deferred custom action called "MyDeferredCA":</span></span>


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



<span data-ttu-id="b186e-110">Beachten Sie, dass [benutzerdefinierte Aktionen für die verzögerte Ausführung](deferred-execution-custom-actions.md) nur das **msidbcustomaktiontypoidentitäts Ate** -Attribut verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b186e-110">Note that only [deferred execution custom actions](deferred-execution-custom-actions.md) can use the **msidbCustomActionTypeNoImpersonate** attribute.</span></span> <span data-ttu-id="b186e-111">Weitere Informationen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="b186e-111">For more information see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="b186e-112">Wenn das **msidbcustomaction typoidentitäts** -Bit nicht für eine benutzerdefinierte Aktion festgelegt ist, führt das Installationsprogramm die benutzerdefinierte Aktion mit Berechtigungen auf Benutzerebene aus.</span><span class="sxs-lookup"><span data-stu-id="b186e-112">If the **msidbCustomActionTypeNoImpersonate** bit is not set for a custom action, the installer runs the custom action with user-level privileges.</span></span> <span data-ttu-id="b186e-113">Weitere Informationen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="b186e-113">For more information, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="b186e-114">Wenn das **msidbcustomaction typoidentitäts Ate** -Bit festgelegt ist und eine verwaltete Anwendung mit der Administrator Berechtigung installiert wird, kann das Installationsprogramm die benutzerdefinierte Aktion mit erhöhten Rechten ausführen.</span><span class="sxs-lookup"><span data-stu-id="b186e-114">If the **msidbCustomActionTypeNoImpersonate** bit is set and a managed application is being installed with administrator permission, the installer may run the custom action with elevated privileges.</span></span> <span data-ttu-id="b186e-115">Wenn ein Benutzer jedoch versucht, die verwaltete Anwendung ohne Administrator Berechtigung zu installieren, führt das Installationsprogramm die Anwendung mit Berechtigungen auf Benutzerebene aus, und zwar unabhängig davon, ob **msidbcustomaktiontycuoidentitäts Ate** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b186e-115">However, if a user attempts to install the managed application without administrator permission, the installer runs the application with user level privileges regardless of whether **msidbCustomActionTypeNoImpersonate** is set.</span></span>

<span data-ttu-id="b186e-116">Beachten Sie, dass eine benutzerdefinierte Aktion auch dann mit System Privilegien ausgeführt werden kann, wenn das **msidbcustomaction typoidentitäts Ate** -Bit nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b186e-116">Note that a custom action may run with system privileges even when the **msidbCustomActionTypeNoImpersonate** bit is not set.</span></span> <span data-ttu-id="b186e-117">Dies tritt auf, wenn ein Administrator die Anwendung für alle Benutzer auf einem Server installiert, auf dem der Terminal Server-Rollen Dienst mit Windows 2000 ausgeführt wird, und die Aktion nicht mit " **msidbcustomaction typetsaware**" gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="b186e-117">This occurs if an administrator installs the application for all users on a server running the Terminal Server role service using Windows 2000 and the action is not marked with **msidbCustomActionTypeTSAware**.</span></span> <span data-ttu-id="b186e-118">Eine benutzerdefinierte Aktion kann auch mit System Privilegien ausgeführt werden, wenn die Installation aufgerufen wird, wenn kein Benutzer Kontext vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b186e-118">A custom action may also run with system privileges if the installation is invoked when there is no user context.</span></span> <span data-ttu-id="b186e-119">Dies ist beispielsweise der Fall, wenn während einer von der Windows 2000-Anwendungs Bereitstellung aufgerufenen Installation kein aktuell angemeldeter Benutzer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b186e-119">For example, if there is no currently logged-on user during an installation invoked by Windows 2000 Application Deployment.</span></span>

<span data-ttu-id="b186e-120">Wenn Sie eigene benutzerdefinierte Aktionen erstellen, sollten Sie die benutzerdefinierte Aktion immer mit sicheren Methoden erstellen.</span><span class="sxs-lookup"><span data-stu-id="b186e-120">When creating your own custom actions, you should always author the custom action using secure methods.</span></span> <span data-ttu-id="b186e-121">Weitere Informationen finden Sie unter [Richtlinien zum Sichern von benutzerdefinierten Aktionen](guidelines-for-securing-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="b186e-121">For more information, see [Guidelines for Securing Custom Actions](guidelines-for-securing-custom-actions.md).</span></span>

 

 



