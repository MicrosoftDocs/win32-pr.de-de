---
title: Installieren eines Diensts auf einem Hostcomputer
description: Das folgende Codebeispiel zeigt die grundlegenden Schritte zum Installieren eines verzeichnisfähigen Diensts auf einem Hostcomputer.
ms.assetid: 35a3b261-d499-4154-a022-1e33a9ef7ba8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0d22098b0a6b823aa5b7db50c20b5a5e2c80c7e540ffdb95e4e2f73c2550fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187388"
---
# <a name="installing-a-service-on-a-host-computer"></a>Installieren eines Diensts auf einem Hostcomputer

Das folgende Codebeispiel zeigt die grundlegenden Schritte zum Installieren eines verzeichnisfähigen Diensts auf einem Hostcomputer. Er führt die folgenden Vorgänge aus:

1.  Ruft die [**OpenSCManager-Funktion**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) auf, um ein Handle für den Dienststeuerungs-Manager (Service Control Manager, SCM) auf dem lokalen Computer zu öffnen.
2.  Ruft die [**CreateService-Funktion**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) auf, um den Dienst in der SCM-Datenbank zu installieren. Dieser Aufruf gibt das Anmeldekonto und das Kennwort des Diensts sowie die ausführbare Datei des Diensts und andere Informationen zum Dienst an. **CreateService** schlägt fehl, wenn das angegebene Anmeldekonto ungültig ist. CreateService **überprüft** jedoch nicht die Gültigkeit des Kennworts. Außerdem wird nicht überprüft, ob das Konto über die Anmeldung als Dienst auf dem lokalen Computer verfügt. Weitere Informationen finden Sie unter [Granting Logon as Service Right on the Host Computer](granting-logon-as-service-right-on-the-host-computer.md).
3.  Ruft die **ScpCreate-Unterroutine** des Diensts auf, die ein Dienstverbindungspunktobjekt (Service Connection Point Object, SCP) im Verzeichnis erstellt, um den Speicherort dieser Instanz des Diensts zu veröffentlichen. Weitere Informationen finden Sie unter Suchen und Verwenden [eines Dienstverbindungspunkts durch Clients.](how-clients-find-and-use-a-service-connection-point.md) Diese Routine speichert auch die Bindungsinformationen des Diensts im SCP, legt einen ACE auf dem SCP fest, damit der Dienst zur Laufzeit darauf zugreifen kann, speichert den Distinguished Name des SCP in der lokalen Registrierung zwischen und gibt den Distinguished Name des neuen SCP zurück.
4.  Ruft die **SpnCompose-Unterroutine** des Diensts auf, die die Klassenzeichenfolge des Diensts und den Distinguished Name des SCP verwendet, um einen Dienstprinzipalnamen (Service Principal Name, SPN) zu erstellen. Weitere Informationen finden Sie unter [Zusammenstellen der SPNs für einen Dienst mit einem SCP.](composing-the-spns-for-a-service-with-an-scp.md) Der SPN identifiziert diese Instanz des Diensts eindeutig.
5.  Ruft die **SpnRegister-Unterroutine** des Diensts auf, die den SPN für das Kontoobjekt registriert, das dem Anmeldekonto des Diensts zugeordnet ist. Weitere Informationen finden Sie unter [Registrieren der SPNs für einen Dienst.](registering-the-spns-for-a-service.md) Durch die Registrierung des SPN können Clientanwendungen den Dienst authentifizieren.

Dieses Codebeispiel funktioniert ordnungsgemäß, unabhängig davon, ob es sich bei dem Anmeldekonto um ein lokales Benutzerkonto oder ein Domänenbenutzerkonto oder um das LocalSystem-Konto handelt. Für ein Domänenbenutzerkonto enthält der *szServiceAccountSAM-Parameter* den Domain* UserName-Namen des Kontos, und ***\\**  *der szServiceAccountDN-Parameter* enthält den Distinguished Name des Benutzerkontoobjekts im Verzeichnis. Für das LocalSystem-Konto sind *szServiceAccountSAM* und *szPassword* **NULL,** *und szServiceAccountSN* ist der Distinguished Name des Kontoobjekts des lokalen Computers im Verzeichnis. Wenn *szServiceAccountSAM ein* lokales Benutzerkonto angibt \\ (das Namensformat ist ".* UserName*"), wird im Codebeispiel die SPN-Registrierung übersprungen, da die gegenseitige Authentifizierung für lokale Benutzerkonten nicht unterstützt wird.

Beachten Sie, dass die Standardsicherheitskonfiguration nur Domänenadministratoren die Ausführung dieses Codes erlaubt.

Beachten Sie außerdem, dass dieses Codebeispiel wie geschrieben auf dem Computer ausgeführt werden muss, auf dem der Dienst installiert wird. Folglich befindet sie sich in der Regel in einer separaten ausführbaren Installationsdatei von Ihrem Dienstinstallationscode, die das Schema erweitert, die Benutzeroberfläche erweitert oder Gruppenrichtlinien ein richtet. Diese Vorgänge installieren Dienstkomponenten für eine gesamte Gesamtstruktur, während dieser Code den Dienst auf einem einzelnen Computer installiert.


```C++
void InstallServiceOnLocalComputer(
            LPTSTR szServiceAccountDN,  // Distinguished name of logon account.
            LPTSTR szServiceAccountSAM, // SAM name of logon account.
            LPTSTR szPassword)          // Password of logon account.
{
SC_HANDLE   schService = NULL;
SC_HANDLE   schSCManager = NULL;
TCHAR szPath[512];
LPTSTR lpFilePart;
TCHAR szDNofSCP[MAX_PATH];
TCHAR szServiceClass[]=TEXT("ADSockAuth");
 
DWORD dwStatus;
TCHAR **pspn=NULL;
ULONG ulSpn=1;
 
// Get the full path of the service's executable.
// The code example assumes that the executable is in the current directory.
dwStatus = GetFullPathName(TEXT("service.exe"), 512, szPath, &lpFilePart);
if (dwStatus == 0) {
    _tprintf(TEXT("Unable to install %s - %s\n"), 
            TEXT(SZSERVICEDISPLAYNAME), GetLastErrorText(szErr, 256));
    return;
}
_tprintf(TEXT("path of service.exe: %s\n"), szPath);
 
// Open the Service Control Manager on the local computer.
schSCManager = OpenSCManager(
                NULL,                   // Computer (NULL == local)
                NULL,                   // Database (NULL == default)
                SC_MANAGER_ALL_ACCESS   // Access required
                );
if (! schSCManager) {
    _tprintf(TEXT("OpenSCManager failed - %s\n"), 
                   GetLastErrorText(szErr,256));
    goto cleanup;
}
        
// Install the service in the SCM database.
schService = CreateService(
            schSCManager,               // SCManager database
            TEXT(SZSERVICENAME),        // Name of service
            TEXT(SZSERVICEDISPLAYNAME), // Name to display
            SERVICE_ALL_ACCESS,         // Desired access
            SERVICE_WIN32_OWN_PROCESS,  // Service type
            SERVICE_DEMAND_START,       // Start type
            SERVICE_ERROR_NORMAL,       // Error control type
            szPath,                     // Service binary
            NULL,                       // No load ordering group
            NULL,                       // No tag identifier
            TEXT(SZDEPENDENCIES),       // Dependencies
            szServiceAccountSAM,        // Service account
            szPassword);                // Account password
if (! schService) {
    _tprintf(TEXT("CreateService failed - %s\n"), 
                   GetLastErrorText(szErr,256));
    goto cleanup;
}
 
_tprintf(TEXT("%s installed.\n"), TEXT(SZSERVICEDISPLAYNAME) );
 
// Create the service's Service Connection Point (SCP).
dwStatus = ScpCreate(
        2000,                 // Service default port number
        szServiceClass,       // Specifies the service class string
        szServiceAccountSAM,  // SAM name of logon account for ACE
        szDNofSCP             // Buffer returns the DN of the SCP
        );
if (dwStatus != 0) {
    _tprintf(TEXT("ScpCreate failed: %d\n"), dwStatus );
    DeleteService(schService);
    goto cleanup;
}
 
// Compose and register a service principal name for this service.
// This is performed on the install path because this requires elevated
// privileges for updating the directory.
// If a local account of the format ".\user name", skip the SPN.
if ( szServiceAccountSAM[0] == '.' ) 
{
    _tprintf(TEXT("Do not register SPN for a local account.\n"));
    goto cleanup;
}
 
dwStatus = SpnCompose(
        &pspn,            // Receives pointer to the SPN array.
        &ulSpn,           // Receives number of SPNs returned.
        szDNofSCP,        // Input: DN of the SCP.
        szServiceClass);  // Input: the service's class string.
 
if (dwStatus == NO_ERROR) 
    dwStatus = SpnRegister(
        szServiceAccountDN,  // Account on which SPNs are registered.
        pspn,                // Array of SPNs to register.
        ulSpn,               // Number of SPNs in array.
        DS_SPN_ADD_SPN_OP);  // Operation code: Add SPNs.
 
if (dwStatus != NO_ERROR) 
{
    _tprintf(TEXT("Failed to compose SPN: Error was %X\n"), 
                  dwStatus);
    DeleteService(schService);
    ScpDelete(szDNofSCP, szServiceClass, szServiceAccountDN);
    goto cleanup;
}
 
cleanup:
if (schSCManager)
    CloseServiceHandle(schSCManager);
if (schService)
    CloseServiceHandle(schService);
DsFreeSpnArray(ulSpn, pspn);
return;
}
```



Weitere Informationen zum vorherigen Codebeispiel finden Sie unter Zusammenstellen der [SPNs](composing-the-spns-for-a-service-with-an-scp.md) für einen Dienst mit einem SCP und Registrieren der [SPNs für einen Dienst.](registering-the-spns-for-a-service.md)

 

 