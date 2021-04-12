---
title: Installieren eines Diensts auf einem Host Computer
description: Im folgenden Codebeispiel werden die grundlegenden Schritte zum Installieren eines Verzeichnis fähigen Diensts auf einem Host Computer veranschaulicht.
ms.assetid: 35a3b261-d499-4154-a022-1e33a9ef7ba8
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d687bbbfadb4d1ccb789e9d5f1051ebfbb4484d7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472525"
---
# <a name="installing-a-service-on-a-host-computer"></a>Installieren eines Diensts auf einem Host Computer

Im folgenden Codebeispiel werden die grundlegenden Schritte zum Installieren eines Verzeichnis fähigen Diensts auf einem Host Computer veranschaulicht. Sie führt die folgenden Vorgänge aus:

1.  Ruft die [**OpenSCManager**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) -Funktion auf, um ein Handle für den Dienststeuerungs-Manager (Service Control Manager, SCM) auf dem lokalen Computer zu öffnen.
2.  Ruft die [**Funktion "**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) " in der SCM-Datenbank auf, um den Dienst zu installieren. Dieser Befehl gibt das Anmelde Konto und das Kennwort des Diensts sowie die ausführbare Datei des Diensts sowie andere Informationen über den Dienst an. Bei "up **Service Service** " tritt ein Fehler auf, wenn das angegebene Anmelde Konto ungültig ist. Allerdings überprüft die Gültigkeit des Kennworts **nicht.** Außerdem wird nicht überprüft, ob das Konto über das Recht "Anmelden als Dienst" auf dem lokalen Computer verfügt. Weitere Informationen finden Sie unter [erteilen der Berechtigung "Anmelden als Dienst" auf dem Host Computer](granting-logon-as-service-right-on-the-host-computer.md).
3.  Ruft die **scpcreate** -Unterroutine des dienstanders auf, die ein Dienst Verbindungspunkt-Objekt (SCP) im Verzeichnis erstellt, um den Speicherort dieser Instanz des Dienstanbieter zu veröffentlichen. Weitere Informationen finden Sie unter Gewusst wie: Suchen [und Verwenden eines Dienst Verbindungs Punkts durch Clients](how-clients-find-and-use-a-service-connection-point.md). Diese Routine speichert außerdem die Bindungs Informationen des Dienstanbieter im SCP, legt einen ACE auf dem SCP fest, sodass der Dienst zur Laufzeit darauf zugreifen kann, den Distinguished Name des SCP in der lokalen Registrierung zwischenspeichert und den Distinguished Name des neuen Dienst Verbindungs Punkts zurückgibt.
4.  Ruft die **spncompose** -Unterroutine des Dieners auf, die die Klassen Zeichenfolge des dienstanders und den Distinguished Name des SCP verwendet, um einen Dienst Prinzipal Namen (SPN) zu verfassen. Weitere Informationen finden Sie unter Erstellen [der SPNs für einen Dienst mit einem SCP](composing-the-spns-for-a-service-with-an-scp.md). Der SPN identifiziert diese Instanz des Dienstanbieter eindeutig.
5.  Ruft die **spnregister** -Unterroutine des Diensts auf, die den SPN für das Konto Objekt registriert, das dem Anmelde Konto des Diensts zugeordnet ist. Weitere Informationen finden Sie unter [Registrieren der SPNs für einen Dienst](registering-the-spns-for-a-service.md). Durch die Registrierung des SPN können Client Anwendungen den Dienst authentifizieren.

Dieses Codebeispiel funktioniert unabhängig davon, ob es sich bei dem Anmelde Konto um ein lokales oder ein Domänen Benutzerkonto oder um das LocalSystem-Konto handelt. Bei einem Domänen Benutzerkonto enthält der Parameter " *szserviceaccountsam* " den Namen des *Domänen ***\\*** Benutzer* namens des Kontos, und der Parameter " *szserviceaccountdn* " enthält den Distinguished Name des Benutzerkonto Objekts im Verzeichnis. Für das Konto "LocalSystem" sind " *szserviceaccountsam* " und " *szPassword* " **null**, und " *szserviceaccountn* " ist der Distinguished Name des Konto Objekts des lokalen Computers im Verzeichnis. Wenn *szserviceaccountsam* ein lokales Benutzerkonto angibt (Namensformat). \\ *Benutzername*"), das Codebeispiel überspringt die SPN-Registrierung, weil die gegenseitige Authentifizierung für lokale Benutzerkonten nicht unterstützt wird.

Beachten Sie, dass die Standard Sicherheitskonfiguration nur Domänen Administratoren das Ausführen dieses Codes ermöglicht.

Beachten Sie außerdem, dass dieses Codebeispiel wie geschrieben auf dem Computer ausgeführt werden muss, auf dem der Dienst installiert wird. Folglich befindet er sich in der Regel in einer separaten ausführbaren Installationsdatei des Dienst Installationscodes, der das Schema erweitert, die Benutzeroberfläche erweitert oder die Gruppenrichtlinie festlegt. Mit diesen Vorgängen werden Dienst Komponenten für eine gesamte Gesamtstruktur installiert, während dieser Code den Dienst auf einem einzelnen Computer installiert.


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



Weitere Informationen zum vorherigen Codebeispiel finden Sie unter Erstellen [der SPNs für einen Dienst mit einem SCP](composing-the-spns-for-a-service-with-an-scp.md) und [Registrieren der SPNs für einen Dienst](registering-the-spns-for-a-service.md).

 

 