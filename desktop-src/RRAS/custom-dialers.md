---
title: Benutzerdefinierte-diker
description: Windows 2000 und spätere Betriebssysteme ermöglichen es Entwicklern, eigene benutzerdefinierte dbugatoren bereitzustellen, die mit dem Remote Zugriffs Dienst (RAS) funktionieren.
ms.assetid: ad94f38d-812f-4329-8055-6274a21a3242
keywords:
- Benutzerdefinierte-diker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35293de408a2a0faa146b93f9b5d5ebccf447acc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209302"
---
# <a name="custom-dialers"></a><span data-ttu-id="c5490-104">Benutzerdefinierte-diker</span><span class="sxs-lookup"><span data-stu-id="c5490-104">Custom Dialers</span></span>

<span data-ttu-id="c5490-105">Windows 2000 und spätere Betriebssysteme ermöglichen es Entwicklern, eigene benutzerdefinierte dbugatoren bereitzustellen, die mit dem Remote Zugriffs Dienst (RAS) funktionieren.</span><span class="sxs-lookup"><span data-stu-id="c5490-105">Windows 2000 and later operating systems enable developers to provide their own custom dialers that work with the Remote Access Service (RAS).</span></span> <span data-ttu-id="c5490-106">Die benutzerdefinierte Einwählprogramm ist als einzelne Dynamic Link Library (dll) implementiert, die die folgenden Einstiegspunkte exportiert:</span><span class="sxs-lookup"><span data-stu-id="c5490-106">The custom dialer is implemented as a single dynamic-link library (DLL) that exports the following entry points:</span></span>

-   [<span data-ttu-id="c5490-107">**Rascustomdial**</span><span class="sxs-lookup"><span data-stu-id="c5490-107">**RasCustomDial**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [<span data-ttu-id="c5490-108">**Rascustomdialdlg**</span><span class="sxs-lookup"><span data-stu-id="c5490-108">**RasCustomDialDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [<span data-ttu-id="c5490-109">**Rascustomhangup**</span><span class="sxs-lookup"><span data-stu-id="c5490-109">**RasCustomHangup**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [<span data-ttu-id="c5490-110">**Rascustomentrydlg**</span><span class="sxs-lookup"><span data-stu-id="c5490-110">**RasCustomEntryDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [<span data-ttu-id="c5490-111">**Rascustomdeleteentrynotify**</span><span class="sxs-lookup"><span data-stu-id="c5490-111">**RasCustomDeleteEntryNotify**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

<span data-ttu-id="c5490-112">Die benutzerdefinierte DFÜ-dll muss alle diese Einstiegspunkte exportieren und die Einstiegspunkte als Unicode-Funktionen implementieren.</span><span class="sxs-lookup"><span data-stu-id="c5490-112">The custom-dial DLL must export all of these entry points, and it must implement the entry points as Unicode functions.</span></span> <span data-ttu-id="c5490-113">Weitere Informationen zu diesen Funktionen finden Sie auf der Referenzseite für jede Funktion in der Windows SDK RAS-Dienst Referenz.</span><span class="sxs-lookup"><span data-stu-id="c5490-113">For more information about these functions, see the reference page for each function in the Windows SDK Remote Access Service Reference.</span></span>

<span data-ttu-id="c5490-114">Damit eine RAS-Verbindung die benutzerdefinierte Dialer verwendet, muss der Telefonbucheintrag für die Verbindung den Pfad zur benutzerdefinierten dll enthalten.</span><span class="sxs-lookup"><span data-stu-id="c5490-114">In order for a RAS connection to use the custom dialer, the phone-book entry for the connection must contain the path to the custom-dial DLL.</span></span> <span data-ttu-id="c5490-115">Verwenden Sie die RAS-API-Funktionen " [**rasgetentryproperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) " und " [**rassetentryproperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) ", um diesen Pfad im **szcustomdialdll** -Member der " [**rasentry**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) "-Struktur für den Telefonbucheintrag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c5490-115">Use the RAS API functions [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) and [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) to set this path in the **szCustomDialDll** member of the [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) structure for the phone-book entry.</span></span>

## <a name="updating-the-registry-for-custom-dialers"></a><span data-ttu-id="c5490-116">Aktualisieren der Registrierung für benutzerdefinierte Dialekte</span><span class="sxs-lookup"><span data-stu-id="c5490-116">Updating the Registry for Custom Dialers</span></span>

<span data-ttu-id="c5490-117">Damit das System eine Verbindung wählen kann, die eine benutzerdefinierte Dialer verwendet, muss der Pfad zur benutzerdefinierten DFÜ-dll im folgenden Registrierungs Wert vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="c5490-117">In order for the system to dial a connection that uses a custom dialer, the path to the custom-dial DLL must exist in the following registry value.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
                  CustomDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_MULTI_SZ</dd>
</dl>
```

<span data-ttu-id="c5490-118">Da **CustomDLL** den Typ **reg \_ \_ MultiSZ** hat, kann es Pfade zu mehreren benutzerdefinierten DLLs enthalten.</span><span class="sxs-lookup"><span data-stu-id="c5490-118">Because **CustomDLL** is of type **REG\_MULTI\_SZ**, it can hold paths to multiple custom-dial DLLs.</span></span> <span data-ttu-id="c5490-119">Sie müssen den Pfad zu der benutzerdefinierten DFÜ-dll in diesem Registrierungs Wert zusätzlich zum Telefonbucheintrag für die Verbindung festlegen.</span><span class="sxs-lookup"><span data-stu-id="c5490-119">You need to set the path to the custom-dial DLL in this registry value, in addition to the phone-book entry for the connection.</span></span>

<span data-ttu-id="c5490-120">Standardmäßig kann dieser Registrierungs Wert nur von einem Benutzer mit Administrator-oder System Berechtigungen geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c5490-120">By default, this registry value is writeable only by a user with Administrator or System privileges.</span></span> <span data-ttu-id="c5490-121">Ändern Sie die Berechtigungen für diesen Registrierungsschlüssel aus Sicherheitsgründen nicht.</span><span class="sxs-lookup"><span data-stu-id="c5490-121">For security reasons, do not change the permissions on this registry key.</span></span>

## <a name="using-custom-dialers-at-system-logon"></a><span data-ttu-id="c5490-122">Verwenden von benutzerdefinierten dialtoren bei der System Anmeldung</span><span class="sxs-lookup"><span data-stu-id="c5490-122">Using Custom Dialers at System Logon</span></span>

<span data-ttu-id="c5490-123">Windows 2000 und spätere Betriebssysteme ermöglichen es einem Benutzer, zum Zeitpunkt der Anmeldung eine RAS-Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="c5490-123">Windows 2000 and later operating systems allow a user to establish a RAS connection at the time of logon.</span></span> <span data-ttu-id="c5490-124">Zu diesem Zweck überprüft der Benutzer die **Anmeldung mithilfe des Einwählnetzwerks** im Dialogfeld **Anmelde Informationen** .</span><span class="sxs-lookup"><span data-stu-id="c5490-124">To do so, the user checks **Logon using Dial-up Networking** in the **Logon Information** dialog box.</span></span> <span data-ttu-id="c5490-125">Nachdem der Benutzer auf die Schaltfläche "OK" geklickt hat, zeigt das System die verfügbaren Verbindungen an.</span><span class="sxs-lookup"><span data-stu-id="c5490-125">After the user clicks the Okay button, the system displays the available connections.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="c5490-126">Überlegungen zur Sicherheit</span><span class="sxs-lookup"><span data-stu-id="c5490-126">Security Considerations</span></span>

<span data-ttu-id="c5490-127">In den meisten Fällen arbeitet eine benutzerdefinierte Einwählprogramm mit den Sicherheits Privilegien des Benutzers, der ihn aufruft.</span><span class="sxs-lookup"><span data-stu-id="c5490-127">In most cases, a custom dialer operates with the security privileges of the user that invokes it.</span></span> <span data-ttu-id="c5490-128">Wenn jedoch die benutzerdefinierte Einwählprogramm bei der Anmeldung aufgerufen wird, wird Sie mit System Privilegien betrieben.</span><span class="sxs-lookup"><span data-stu-id="c5490-128">However, if the custom dialer is invoked at logon, it operates with system privileges.</span></span> <span data-ttu-id="c5490-129">Daher sollten Sie die benutzerdefinierte Einwählprogramm so entwerfen, dass Sie nicht zur Verletzung der Systemsicherheit verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c5490-129">Therefore, design the custom dialer so that it cannot be used to violate system security.</span></span> <span data-ttu-id="c5490-130">Beispielsweise sollte die Einwählprogramm keine Benutzeroberfläche präsentieren, die dem Benutzer den Schreibzugriff auf das Dateisystem des Computers ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="c5490-130">For example, the dialer should not present a user interface that allows the user write access to the computer's file system.</span></span> <span data-ttu-id="c5490-131">Zu den Benutzeroberflächen, die diesen Zugriff bereitstellen, gehören das Dialogfeld " **Find-File** ", das Dialogfeld " **Datei öffnen** " und die Windows- **Hilfe**</span><span class="sxs-lookup"><span data-stu-id="c5490-131">User interfaces that provide such access include the **Find-File** dialog, the **File-Open** common dialog, and Windows **Help**.</span></span>

## <a name="custom-dialer-user-interface-must-support-idcancel"></a><span data-ttu-id="c5490-132">Benutzerdefinierte Dialer-Benutzeroberfläche muss IDCANCEL unterstützen</span><span class="sxs-lookup"><span data-stu-id="c5490-132">Custom Dialer User Interface Must Support IDCANCEL</span></span>

<span data-ttu-id="c5490-133">Wenn die benutzerdefinierte Einwählprogramm eine Benutzeroberfläche anzeigt, muss die Benutzeroberfläche die WM-befehlsnachrichten unterstützen, \_ wobei LoWord (*wParam*) gleich IDCANCEL ist.</span><span class="sxs-lookup"><span data-stu-id="c5490-133">If the custom dialer displays a user interface, the user interface must support WM\_COMMAND messages where LOWORD(*wParam*) equals IDCANCEL.</span></span>

 

 