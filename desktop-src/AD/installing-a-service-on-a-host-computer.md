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
# <a name="installing-a-service-on-a-host-computer"></a><span data-ttu-id="d8e56-103">Installieren eines Diensts auf einem Host Computer</span><span class="sxs-lookup"><span data-stu-id="d8e56-103">Installing a Service on a Host Computer</span></span>

<span data-ttu-id="d8e56-104">Im folgenden Codebeispiel werden die grundlegenden Schritte zum Installieren eines Verzeichnis fähigen Diensts auf einem Host Computer veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d8e56-104">The following code example shows the basic steps of installing a directory-enabled service on a host computer.</span></span> <span data-ttu-id="d8e56-105">Sie führt die folgenden Vorgänge aus:</span><span class="sxs-lookup"><span data-stu-id="d8e56-105">It performs the following operations:</span></span>

1.  <span data-ttu-id="d8e56-106">Ruft die [**OpenSCManager**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) -Funktion auf, um ein Handle für den Dienststeuerungs-Manager (Service Control Manager, SCM) auf dem lokalen Computer zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d8e56-106">Calls the [**OpenSCManager**](/windows/desktop/api/winsvc/nf-winsvc-openscmanagera) function to open a handle to the service control manager (SCM) on the local computer.</span></span>
2.  <span data-ttu-id="d8e56-107">Ruft die [**Funktion "**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) " in der SCM-Datenbank auf, um den Dienst zu installieren.</span><span class="sxs-lookup"><span data-stu-id="d8e56-107">Calls the [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) function to install the service in the SCM database.</span></span> <span data-ttu-id="d8e56-108">Dieser Befehl gibt das Anmelde Konto und das Kennwort des Diensts sowie die ausführbare Datei des Diensts sowie andere Informationen über den Dienst an.</span><span class="sxs-lookup"><span data-stu-id="d8e56-108">This call specifies the service's logon account and password, as well as the service's executable and other information about the service.</span></span> <span data-ttu-id="d8e56-109">Bei "up **Service Service** " tritt ein Fehler auf, wenn das angegebene Anmelde Konto ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="d8e56-109">**CreateService** fails if the specified logon account is invalid.</span></span> <span data-ttu-id="d8e56-110">Allerdings überprüft die Gültigkeit des Kennworts **nicht.**</span><span class="sxs-lookup"><span data-stu-id="d8e56-110">However, **CreateService** does not check the validity of the password.</span></span> <span data-ttu-id="d8e56-111">Außerdem wird nicht überprüft, ob das Konto über das Recht "Anmelden als Dienst" auf dem lokalen Computer verfügt.</span><span class="sxs-lookup"><span data-stu-id="d8e56-111">It also does not verify that the account has the logon as a service right on the local computer.</span></span> <span data-ttu-id="d8e56-112">Weitere Informationen finden Sie unter [erteilen der Berechtigung "Anmelden als Dienst" auf dem Host Computer](granting-logon-as-service-right-on-the-host-computer.md).</span><span class="sxs-lookup"><span data-stu-id="d8e56-112">For more information, see [Granting Logon as Service Right on the Host Computer](granting-logon-as-service-right-on-the-host-computer.md).</span></span>
3.  <span data-ttu-id="d8e56-113">Ruft die **scpcreate** -Unterroutine des dienstanders auf, die ein Dienst Verbindungspunkt-Objekt (SCP) im Verzeichnis erstellt, um den Speicherort dieser Instanz des Dienstanbieter zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="d8e56-113">Calls the service's **ScpCreate** subroutine that creates a service connection point object (SCP) in the directory to publish the location of this instance of the service.</span></span> <span data-ttu-id="d8e56-114">Weitere Informationen finden Sie unter Gewusst wie: Suchen [und Verwenden eines Dienst Verbindungs Punkts durch Clients](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="d8e56-114">For more information, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span> <span data-ttu-id="d8e56-115">Diese Routine speichert außerdem die Bindungs Informationen des Dienstanbieter im SCP, legt einen ACE auf dem SCP fest, sodass der Dienst zur Laufzeit darauf zugreifen kann, den Distinguished Name des SCP in der lokalen Registrierung zwischenspeichert und den Distinguished Name des neuen Dienst Verbindungs Punkts zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d8e56-115">This routine also stores the service's binding information in the SCP, sets an ACE on the SCP so the service can access it at run time, caches the distinguished name of the SCP in the local registry, and returns the distinguished name of the new SCP.</span></span>
4.  <span data-ttu-id="d8e56-116">Ruft die **spncompose** -Unterroutine des Dieners auf, die die Klassen Zeichenfolge des dienstanders und den Distinguished Name des SCP verwendet, um einen Dienst Prinzipal Namen (SPN) zu verfassen.</span><span class="sxs-lookup"><span data-stu-id="d8e56-116">Calls the service's **SpnCompose** subroutine that uses the service's class string and the distinguished name of the SCP to compose a service principal name (SPN).</span></span> <span data-ttu-id="d8e56-117">Weitere Informationen finden Sie unter Erstellen [der SPNs für einen Dienst mit einem SCP](composing-the-spns-for-a-service-with-an-scp.md).</span><span class="sxs-lookup"><span data-stu-id="d8e56-117">For more information, see [Composing the SPNs for a Service with an SCP](composing-the-spns-for-a-service-with-an-scp.md).</span></span> <span data-ttu-id="d8e56-118">Der SPN identifiziert diese Instanz des Dienstanbieter eindeutig.</span><span class="sxs-lookup"><span data-stu-id="d8e56-118">The SPN uniquely identifies this instance of the service.</span></span>
5.  <span data-ttu-id="d8e56-119">Ruft die **spnregister** -Unterroutine des Diensts auf, die den SPN für das Konto Objekt registriert, das dem Anmelde Konto des Diensts zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d8e56-119">Calls the service's **SpnRegister** subroutine that registers the SPN on the account object associated with service's logon account.</span></span> <span data-ttu-id="d8e56-120">Weitere Informationen finden Sie unter [Registrieren der SPNs für einen Dienst](registering-the-spns-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="d8e56-120">For more information, see [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span> <span data-ttu-id="d8e56-121">Durch die Registrierung des SPN können Client Anwendungen den Dienst authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="d8e56-121">Registration of the SPN enables client applications to authenticate the service.</span></span>

<span data-ttu-id="d8e56-122">Dieses Codebeispiel funktioniert unabhängig davon, ob es sich bei dem Anmelde Konto um ein lokales oder ein Domänen Benutzerkonto oder um das LocalSystem-Konto handelt.</span><span class="sxs-lookup"><span data-stu-id="d8e56-122">This code example works correctly regardless of whether the logon account is a local or domain user account or the LocalSystem account.</span></span> <span data-ttu-id="d8e56-123">Bei einem Domänen Benutzerkonto enthält der Parameter " *szserviceaccountsam* " den Namen des *Domänen ***\\*** Benutzer* namens des Kontos, und der Parameter " *szserviceaccountdn* " enthält den Distinguished Name des Benutzerkonto Objekts im Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="d8e56-123">For a domain user account, the *szServiceAccountSAM* parameter contains the *Domain ***\\*** UserName* name of the account, and the *szServiceAccountDN* parameter contains the distinguished name of the user account object in the directory.</span></span> <span data-ttu-id="d8e56-124">Für das Konto "LocalSystem" sind " *szserviceaccountsam* " und " *szPassword* " **null**, und " *szserviceaccountn* " ist der Distinguished Name des Konto Objekts des lokalen Computers im Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="d8e56-124">For the LocalSystem account, *szServiceAccountSAM* and *szPassword* are **NULL**, and *szServiceAccountSN* is the distinguished name of the local computer's account object in the directory.</span></span> <span data-ttu-id="d8e56-125">Wenn *szserviceaccountsam* ein lokales Benutzerkonto angibt (Namensformat). \\ *Benutzername*"), das Codebeispiel überspringt die SPN-Registrierung, weil die gegenseitige Authentifizierung für lokale Benutzerkonten nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d8e56-125">If *szServiceAccountSAM* specifies a local user account (name format is ".\\*UserName*"), the code example skips the SPN registration because mutual authentication is not supported for local user accounts.</span></span>

<span data-ttu-id="d8e56-126">Beachten Sie, dass die Standard Sicherheitskonfiguration nur Domänen Administratoren das Ausführen dieses Codes ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="d8e56-126">Be aware that the default security configuration allows only domain administrators to execute this code.</span></span>

<span data-ttu-id="d8e56-127">Beachten Sie außerdem, dass dieses Codebeispiel wie geschrieben auf dem Computer ausgeführt werden muss, auf dem der Dienst installiert wird.</span><span class="sxs-lookup"><span data-stu-id="d8e56-127">Also, be aware that this code example, as written, must be executed on the computer where the service is being installed.</span></span> <span data-ttu-id="d8e56-128">Folglich befindet er sich in der Regel in einer separaten ausführbaren Installationsdatei des Dienst Installationscodes, der das Schema erweitert, die Benutzeroberfläche erweitert oder die Gruppenrichtlinie festlegt.</span><span class="sxs-lookup"><span data-stu-id="d8e56-128">Consequently, it is typically in a separate installation executable from your service installation code, if any, that extends the schema, extends the UI, or sets up group policy.</span></span> <span data-ttu-id="d8e56-129">Mit diesen Vorgängen werden Dienst Komponenten für eine gesamte Gesamtstruktur installiert, während dieser Code den Dienst auf einem einzelnen Computer installiert.</span><span class="sxs-lookup"><span data-stu-id="d8e56-129">Those operations install service components for an entire a forest, whereas this code installs the service on a single computer.</span></span>


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



<span data-ttu-id="d8e56-130">Weitere Informationen zum vorherigen Codebeispiel finden Sie unter Erstellen [der SPNs für einen Dienst mit einem SCP](composing-the-spns-for-a-service-with-an-scp.md) und [Registrieren der SPNs für einen Dienst](registering-the-spns-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="d8e56-130">For more information about the previous code example, see [Composing the SPNs for a Service with an SCP](composing-the-spns-for-a-service-with-an-scp.md) and [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span>

 

 