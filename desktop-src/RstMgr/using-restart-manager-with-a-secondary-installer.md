---
title: Verwenden des Neustart-Managers mit einem sekundären Installationsprogramm
description: Das folgende Verfahren beschreibt die Verwendung des Neustart-Managers mit primären und sekundären Installationsprogrammen.
ms.assetid: aa55ab09-206b-49ed-8cb4-e311c1ed2d9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aefb1f9658752677e7850e939fcb6a3c4c6047c5efc2dc0ceb06ec0f51900ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009988"
---
# <a name="using-restart-manager-with-a-secondary-installer"></a>Verwenden des Neustart-Managers mit einem sekundären Installationsprogramm

Das folgende Verfahren beschreibt die Verwendung des Neustart-Managers mit primären und sekundären Installationsprogrammen.

Bei Verwendung von primären und sekundären Installationsprogrammen steuert das primäre Installationsprogramm die Benutzeroberfläche.

**So verwenden Sie den Neustart-Manager mit primären und sekundären Installationsprogrammen**

1.  Das primäre Installationsprogramm ruft die [**RmStartSession-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmstartsession) auf, um die Neustart-Manager-Sitzung zu starten und ein Sitzungshandle und einen Schlüssel abzurufen.
2.  Das primäre Installationsprogramm startet oder kontaktiert das sekundäre Installationsprogramm und stellt den Sitzungsschlüssel bereit, den Sie im vorherigen Schritt abgerufen haben.
3.  Das sekundäre Installationsprogramm ruft die [**RmJoinSession-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmjoinsession) mit dem Sitzungsschlüssel auf, um der Neustart-Manager-Sitzung beizutreten. Ein sekundäres Installationsprogramm kann nur dann einer Sitzung beitreten, die vom primären Installationsprogramm gestartet wird, wenn beide Installationsprogramme im selben Benutzerkontext ausgeführt werden.
4.  Die primären und sekundären Installationsprogramme rufen die [**RmRegisterResources-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmregisterresources) auf, um Ressourcen zu registrieren. Der Neustart-Manager kann nur registrierte Ressourcen verwenden, um zu bestimmen, welche Anwendungen und Dienste heruntergefahren und neu gestartet werden müssen. Alle Ressourcen, die von der Installation betroffen sein können, sollten bei der Sitzung registriert werden. Ressourcen können anhand des Dateinamens, des Kurznamens des Diensts oder einer [**RM \_ UNIQUE \_ PROCESS-Struktur**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_unique_process) identifiziert werden.
5.  Das primäre Installationsprogramm ruft die [**RmGetList-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) auf, um ein Array von [**RM PROCESS \_ \_ INFO-Strukturen**](/windows/desktop/api/RestartManager/ns-restartmanager-rm_process_info) abzurufen, das alle Anwendungen und Dienste auflistet, die heruntergefahren und neu gestartet werden müssen.

    Wenn der Wert des *lpdwRebootReason-Parameters,* der von der [**RmGetList-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) zurückgegeben wird, ungleich 0 (null) ist, kann der Neustart-Manager eine registrierte Ressource nicht freigeben, indem eine Anwendung oder ein Dienst heruntergefahren wird. In diesem Fall ist ein Herunterfahren und Neustarten des Systems erforderlich, um die Installation fortzusetzen. Das primäre Installationsprogramm sollte den Benutzer zur Eingabe einer Aktion auffordern, Programme oder Dienste beenden oder ein Herunterfahren und Neustarten des Systems planen.

    Wenn der Wert des *lpdwRebootReason-Parameters,* der von der [**RmGetList-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmgetlist) zurückgegeben wird, 0 (null) ist, sollte das Installationsprogramm die [**RmShutdown-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) aufrufen. Dadurch werden die Dienste und Anwendungen heruntergefahren, die registrierte Ressourcen verwenden. Die primären und sekundären Installationsprogramme sollten dann Systemänderungen vornehmen, die zum Abschließen der Installation erforderlich sind. Schließlich sollte das primäre Installationsprogramm die [**RmRestart-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) aufrufen, damit der Neustart-Manager die heruntergefahrenen Anwendungen neu starten kann, die für einen Neustart registriert wurden.

6.  Das primäre und sekundäre Installationsprogramm ruft die [**RmEndSession-Funktion**](/windows/desktop/api/RestartManager/nf-restartmanager-rmendsession) auf, um die Neustart-Manager-Sitzung zu schließen.

Der folgende Codeausschnitt zeigt ein Beispiel für ein primäres Installationsprogramm, das eine Restart Manager-Sitzung startet und verwendet. Für das Beispiel ist Windows 7 oder Windows Server 2008 R2 erforderlich. Auf Windows Vista oder Windows Server 2008 wird die Rechneranwendung heruntergefahren, aber nicht neu gestartet. Dieses Beispiel zeigt, wie ein primäres Installationsprogramm den Neustart-Manager verwenden kann, um einen Prozess herunterzufahren und neu zu starten. Im Beispiel wird davon ausgegangen, dass calculator bereits ausgeführt wird, bevor die Neustart-Manager-Sitzung gestartet wird.


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



Der folgende Codeausschnitt zeigt ein Beispiel für das Verknüpfen eines sekundären Installationsprogramms mit der vorhandenen Restart Manager-Sitzung. Für das Beispiel ist Windows Vista oder Windows Server 2008 erforderlich. Das sekundäre Installationsprogramm ruft den Sitzungsschlüssel vom primären Installationsprogramm ab und verwendet diesen, um der Sitzung beizutreten.


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



 

 




