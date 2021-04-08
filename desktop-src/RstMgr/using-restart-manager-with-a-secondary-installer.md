---
title: Verwenden des Neustart-Managers mit einem sekundären Installer
description: Im folgenden Verfahren wird die Verwendung des Neustart-Managers mit primären und sekundären Installationsprogrammen beschrieben.
ms.assetid: aa55ab09-206b-49ed-8cb4-e311c1ed2d9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb44105d9f3d391bb2ed793aca8a6da2c330b30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855731"
---
# <a name="using-restart-manager-with-a-secondary-installer"></a><span data-ttu-id="c9410-103">Verwenden des Neustart-Managers mit einem sekundären Installer</span><span class="sxs-lookup"><span data-stu-id="c9410-103">Using Restart Manager with a Secondary Installer</span></span>

<span data-ttu-id="c9410-104">Im folgenden Verfahren wird die Verwendung des Neustart-Managers mit primären und sekundären Installationsprogrammen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c9410-104">The following procedure describes the use of the Restart Manager with primary and secondary installers.</span></span>

<span data-ttu-id="c9410-105">Bei der Verwendung von primären und sekundären Installationsprogrammen steuert das primäre Installationsprogramm die Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="c9410-105">When using primary and secondary installers, the primary installer controls the user interface.</span></span>

<span data-ttu-id="c9410-106">**So verwenden Sie den Neustart-Manager mit primären und sekundären Installationsprogrammen**</span><span class="sxs-lookup"><span data-stu-id="c9410-106">**To use Restart Manager with primary and secondary installers**</span></span>

1.  <span data-ttu-id="c9410-107">Das primäre Installationsprogramm ruft die [**rmstartession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) -Funktion auf, um die Neustart-Manager-Sitzung zu starten und ein Sitzungs Handle und einen Schlüssel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c9410-107">The primary installer calls the [**RmStartSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) function to start the Restart Manager session and obtain a session handle and key.</span></span>
2.  <span data-ttu-id="c9410-108">Der primäre Installer startet oder kontaktiert den sekundären Installer und stellt ihm den Sitzungsschlüssel zur Verfügung, der im vorherigen Schritt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c9410-108">The primary installer starts or contacts the secondary installer and provides it with the session key obtained in the previous step.</span></span>
3.  <span data-ttu-id="c9410-109">Der sekundäre Installer Ruft die [**rmjoinsession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession) -Funktion mit dem Sitzungsschlüssel auf, um der Neustart-Manager-Sitzung beizutreten.</span><span class="sxs-lookup"><span data-stu-id="c9410-109">The secondary installer calls the [**RmJoinSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession) function with the session key to join the Restart Manager session.</span></span> <span data-ttu-id="c9410-110">Ein sekundäres Installationsprogramm kann einer Sitzung beitreten, die vom primären Installer gestartet wird, wenn beide Installationsprogramme im selben Benutzer Kontext ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c9410-110">A secondary installer can join a session that is started by the primary installer only when both installers run in the same user context.</span></span>
4.  <span data-ttu-id="c9410-111">Die primären und sekundären Installationsprogramme wenden die [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) -Funktion an, um Ressourcen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="c9410-111">The primary and secondary installers call the [**RmRegisterResources**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) function to register resources.</span></span> <span data-ttu-id="c9410-112">Mit dem Neustart-Manager können nur registrierte Ressourcen verwendet werden, um zu bestimmen, welche Anwendungen und Dienste heruntergefahren und neu gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c9410-112">The Restart Manager can use only registered resources to determine which applications and services must be shut down and restarted.</span></span> <span data-ttu-id="c9410-113">Alle Ressourcen, die von der Installation betroffen sein können, sollten bei der Sitzung registriert werden.</span><span class="sxs-lookup"><span data-stu-id="c9410-113">All resources that can be affected by the installation should be registered with the session.</span></span> <span data-ttu-id="c9410-114">Ressourcen können anhand des Datei namens, des Dienst Kurznamens oder einer [**eindeutigen RM- \_ \_ Prozess**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) Struktur identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c9410-114">Resources can be identified by filename, service short name, or an [**RM\_UNIQUE\_PROCESS**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) structure.</span></span>
5.  <span data-ttu-id="c9410-115">Das primäre Installationsprogramm ruft die [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) -Funktion auf, um ein Array von [**RM- \_ Prozess \_ Informations**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) Strukturen abzurufen, das alle Anwendungen und Dienste auflistet, die heruntergefahren und neu gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c9410-115">The primary installer calls the [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) function to obtain an array of [**RM\_PROCESS\_INFO**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) structures that lists all applications and services that must be shut down and restarted.</span></span>

    <span data-ttu-id="c9410-116">Wenn der Wert des *lpdwrebooverrat* -Parameters, der von der [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) -Funktion zurückgegeben wird, nicht NULL ist, kann der Neustart-Manager eine registrierte Ressource nicht durch das Herunterfahren einer Anwendung oder eines Dienstanbieter freigeben.</span><span class="sxs-lookup"><span data-stu-id="c9410-116">If the value of the *lpdwRebootReason* parameter that is returned by the [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) function is nonzero, the Restart Manager is unable to free a registered resource by the shutdown of an application or service.</span></span> <span data-ttu-id="c9410-117">In diesem Fall ist das Herunterfahren und Neustarten des Systems erforderlich, um die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="c9410-117">In this case, a system shutdown and restart is required to continue the installation.</span></span> <span data-ttu-id="c9410-118">Das primäre Installationsprogramm muss den Benutzer zur Eingabe einer Aktion auffordern, Programme oder Dienste beenden oder das Herunterfahren und Neustarten des Systems planen.</span><span class="sxs-lookup"><span data-stu-id="c9410-118">The primary installer should prompt the user for an action, stop programs or services, or schedule a system shutdown and restart.</span></span>

    <span data-ttu-id="c9410-119">Wenn der Wert des *lpdwrebooverrat* -Parameters, der von der [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) -Funktion zurückgegeben wird, 0 (null) ist, sollte das Installationsprogramm die [**rmshutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c9410-119">If the value of the *lpdwRebootReason* parameter that is returned by the [**RmGetList**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) function is zero, the installer should call the [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) function.</span></span> <span data-ttu-id="c9410-120">Dadurch werden die Dienste und Anwendungen heruntergefahren, die registrierte Ressourcen verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9410-120">This shuts down the services and applications that are using registered resources.</span></span> <span data-ttu-id="c9410-121">Die primären und sekundären Installationsprogramme sollten dann Systemänderungen ausführen, die zum Abschluss der Installation erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="c9410-121">The primary and secondary installers should then perform system modifications that are required to complete the installation.</span></span> <span data-ttu-id="c9410-122">Zum Schluss sollte das primäre Installationsprogramm die [**rmrestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) -Funktion anrufen, damit der Neustart-Manager die herunter gefahrenen Anwendungen neu starten kann, die für einen Neustart registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="c9410-122">Finally, the primary installer should call the [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) function so that the Restart Manager can restart the applications it has shut down and that have been registered for a restart.</span></span>

6.  <span data-ttu-id="c9410-123">Das primäre und sekundäre Installationsprogramm ruft die [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) -Funktion auf, um die Neustart-Manager-Sitzung zu schließen.</span><span class="sxs-lookup"><span data-stu-id="c9410-123">The primary and secondary installer call the [**RmEndSession**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) function to close the Restart Manager session.</span></span>

<span data-ttu-id="c9410-124">Der folgende Code Ausschnitt zeigt ein Beispiel für einen primären Installer, der gestartet wird und eine Neustart-Manager-Sitzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9410-124">The following code snippet shows an example of a primary installer starting and using a Restart Manager session.</span></span> <span data-ttu-id="c9410-125">Das Beispiel erfordert Windows 7 oder Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c9410-125">The example requires Windows 7 or Windows Server 2008 R2.</span></span> <span data-ttu-id="c9410-126">Unter Windows Vista oder Windows Server 2008 wird die Rechner Anwendung heruntergefahren, aber nicht neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="c9410-126">On Windows Vista or Windows Server 2008, the Calculator application shuts down but does not restart.</span></span> <span data-ttu-id="c9410-127">Dieses Beispiel zeigt, wie ein primäres Installationsprogramm den Neustart-Manager zum Herunterfahren und Neustarten eines Prozesses verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="c9410-127">This example shows how a primary installer can use Restart Manager to shutdown and restart a process.</span></span> <span data-ttu-id="c9410-128">Im Beispiel wird davon ausgegangen, dass der Rechner bereits ausgeführt wird, bevor die Restart Manager-Sitzung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c9410-128">The example assumes that Calculator is already running before starting the Restart Manager session.</span></span>


```C++
#include <windows.h>
#include <restartmanager.h>

#pragma comment(lib, "rstrtmgr.lib")

int _cdecl wmain()
{
    DWORD dwErrCode         = ERROR_SUCCESS;
    DWORD dwSessionHandle   = 0xFFFFFFFF; // Invalid handle value

    //
    // CCH_RM_SESSION_KEY: Character count of the  
    // Text-Encoded session key,defined in RestartManager.h
    //
    WCHAR sessKey[CCH_RM_SESSION_KEY+1];
    
    // Number of calc files to be registered.
    DWORD dwFiles           = 2;   

    //
    // NOTE:We register two calc executable files. 
    // The second one is for the redirection of 32 bit calc on 
    // 64 bit machines. Even if you are using a 32 bit machine,  
    // you don't need to comment out the second line. 
    //
    LPCWSTR rgsFiles[]      = 
     {L"C:\\Windows\\System32\\calc.exe",
      L"C:\\Windows\\SysWow64\\calc.exe"};

    UINT nRetry             = 0; 
    UINT nAffectedApps      = 0;
    UINT nProcInfoNeeded    = 0;
    RM_REBOOT_REASON dwRebootReasons    = RmRebootReasonNone;
    RM_PROCESS_INFO *rgAffectedApps     = NULL;
    
    //
    // Start a Restart Manager Session
    //
    dwErrCode = RmStartSession(&dwSessionHandle, 0, sessKey);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // Register items with Restart Manager
    //
    // NOTE: we only register two calc executable files 
    // in this sample. You can register files, processes 
    // (in the form of process ID), and services (in the   
    // form of service short names) with Restart Manager.
    //
    dwErrCode = RmRegisterResources(dwSessionHandle,
                                    dwFiles, 
                                    rgsFiles,       // Files
                                    0,  
                                    NULL,           // Processes
                                    0, 
                                    NULL);          // Services 
                                    
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // Obtain the list of affected applications/services.
    //
    // NOTE: Restart Manager returns the results into the  
    // buffer allocated by the caller. The first call to 
    // RmGetList() will return the size of the buffer  
    // (i.e. nProcInfoNeeded) the caller needs to allocate. 
    // The caller then needs to allocate the buffer  
    // (i.e. rgAffectedApps) and make another RmGetList() 
    // call to ask Restart Manager to write the results 
    // into the buffer. However, since Restart Manager 
    // refreshes the list every time RmGetList()is called, 
    // it is possible that the size returned by the first 
    // RmGetList()call is not sufficient to hold the results  
    // discovered by the second RmGetList() call. Therefore, 
    // it is recommended that the caller follows the 
    // following practice to handle this race condition:
    //   
    //    Use a loop to call RmGetList() in case the buffer 
    //    allocated according to the size returned in previous 
    //    call is not enough.      
    // 
    // In this example, we use a do-while loop trying to make 
    // 3 RmGetList() calls (including the first attempt to get 
    // buffer size) and if we still cannot succeed, we give up. 
    //
    do
    {
        dwErrCode = RmGetList(dwSessionHandle,
                              &nProcInfoNeeded,
                              &nAffectedApps, 
                              rgAffectedApps, 
                              (LPDWORD) &dwRebootReasons);
        if (ERROR_SUCCESS == dwErrCode)
        {
            //
            // RmGetList() succeeded
            //
            break;
        }

        if (ERROR_MORE_DATA != dwErrCode)
        {
            //
            // RmGetList() failed, with errors 
            // other than ERROR_MORE_DATA
            //
            goto RM_CLEANUP;
        }

        //
        // RmGetList() is asking for more data
        //
        nAffectedApps = nProcInfoNeeded;
        
        if (NULL != rgAffectedApps)
        {
            delete []rgAffectedApps;
            rgAffectedApps = NULL;
        }

        rgAffectedApps = new RM_PROCESS_INFO[nAffectedApps];
    } while ((ERROR_MORE_DATA == dwErrCode) && (nRetry ++ < 3));

    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    if (RmRebootReasonNone != dwRebootReasons)
    {
        //
        // Restart Manager cannot mitigate a reboot. 
        // We goes to the clean up. The caller may want   
        // to add additional code to handle this scenario.
        //
        goto RM_CLEANUP;
    }
    
    //
    // Now rgAffectedApps contains the affected applications 
    // and services. The number of applications and services
    // returned is nAffectedApps. The result of RmGetList can 
    // be interpreted by the user to determine subsequent  
    // action (e.g. ask user's permission to shutdown).
    //
    // CALLER CODE GOES HERE...
     
    //
    // Shut down all running instances of affected 
    // applications and services.
    //
    dwErrCode = RmShutdown(dwSessionHandle, 0, NULL);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // An installer can now replace or update
    // the calc executable file.
    //
    // CALLER CODE GOES HERE...


    //
    // Restart applications and services, after the 
    // files have been replaced or updated.
    //
    dwErrCode = RmRestart(dwSessionHandle, 0, NULL);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

  RM_CLEANUP:
    
    if (NULL != rgAffectedApps)
    {
        delete [] rgAffectedApps;
        rgAffectedApps = NULL;
    }

    if (0xFFFFFFFF != dwSessionHandle)
    {
        //
        // Clean up the Restart Manager session.
        //
        RmEndSession(dwSessionHandle);
        dwSessionHandle = 0xFFFFFFFF;
    }

    return 0;
}
```



<span data-ttu-id="c9410-129">Der folgende Code Ausschnitt zeigt ein Beispiel für das Hinzufügen eines sekundären Installationsprogramms zur vorhandenen Restart Manager-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="c9410-129">The following code snippet shows an example of joining a secondary installer to the existing Restart Manager session.</span></span> <span data-ttu-id="c9410-130">Das Beispiel erfordert Windows Vista oder Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c9410-130">The example requires Windows Vista or Windows Server 2008.</span></span> <span data-ttu-id="c9410-131">Das sekundäre Installationsprogramm ruft den Sitzungsschlüssel vom primären Installer ab und verwendet diesen, um der Sitzung beizutreten.</span><span class="sxs-lookup"><span data-stu-id="c9410-131">The secondary installer obtains the session key from the primary installer and uses this to join the session.</span></span>


```C++
#include <windows.h>
#include <restartmanager.h>

#pragma comment(lib, "rstrtmgr.lib")

int _cdecl wmain()
{
    DWORD dwErrCode         = ERROR_SUCCESS;
    DWORD dwSessionHandle   = 0xFFFFFFFF; // Invalid handle value

    //
    // CCH_RM_SESSION_KEY: Character count of the 
    // Text-Encoded session key, defined in RestartManager.h
    //
    WCHAR sessKey[CCH_RM_SESSION_KEY+1];
    
    // Number of files to be registered.
    DWORD dwFiles           = 1;   
    //
    // We register oleaut32.dll with Restart Manager.
    //
    LPCWSTR rgsFiles[]      = 
        {L"C:\\Windows\\System32\\oleaut32.dll"};

    //    
    // Secondary installer needs to obtain the session key from  
    // the primary installer and uses it to join the session.
    //
    // CALLER CODE GOES HERE ...
    //

    // We assume the session key obtained is stored in sessKey
    dwErrCode = RmJoinSession(&dwSessionHandle, sessKey);
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

    //
    // Register items with Restart Manager
    //
    // NOTE: In Vista, the subordinate is only allowed to 
    // register resources and cannot perform any other 
    // getlist, shutdown, restart or filter operations.
    //
    dwErrCode = RmRegisterResources(dwSessionHandle,
                                    dwFiles, 
                                    rgsFiles,     // Files
                                    0,  
                                    NULL,         // Processes
                                    0, 
                                    NULL);        // Services 
                                    
    if (ERROR_SUCCESS != dwErrCode)
    {
        goto RM_CLEANUP;
    }

  RM_CLEANUP:

    if (0xFFFFFFFF != dwSessionHandle)
    {
        //
        // The subordinate leaves the conductor's session 
        // by calling RmEndSession(). The session itself 
        // won't be destroyed until the primary installer 
        // calls RmEndSession()
        //          
        RmEndSession(dwSessionHandle);
        dwSessionHandle = 0xFFFFFFFF;
    }

    return 0;
}

```



 

 




