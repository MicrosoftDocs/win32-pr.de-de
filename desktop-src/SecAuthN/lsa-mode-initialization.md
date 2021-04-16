---
description: Wenn das Computersystem gestartet wird, werden von der lokalen Sicherheits Autorität (Local Security Authority, LSA) automatisch alle registrierten Security Support Provider-/Authentifizierungspaket-DLLs (SSP/AP) in den Prozessbereich geladen. Die folgenden Abbildungen zeigen den Initialisierungs Prozess.
ms.assetid: 2d52cbbf-9e28-4c6f-8b4c-448b73c6dbf8
title: LSA-ModusInitialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e4212a584d290e67c6465488c8398604db2c16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529741"
---
# <a name="lsa-mode-initialization"></a><span data-ttu-id="9d7f5-104">LSA-ModusInitialisierung</span><span class="sxs-lookup"><span data-stu-id="9d7f5-104">LSA Mode Initialization</span></span>

<span data-ttu-id="9d7f5-105">Wenn das Computersystem gestartet wird, lädt die [*Lokale Sicherheits Autorität (Local Security Authority*](../secgloss/l-gly.md) , LSA [](../secgloss/s-gly.md)) automatisch alle registrierten / SSP/AP-DLLs (Security Support Provider [*Authentication Package*](../secgloss/a-gly.md) ) in den Prozessbereich.</span><span class="sxs-lookup"><span data-stu-id="9d7f5-105">When the computer system is started, the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) automatically loads all registered [*security support provider*](../secgloss/s-gly.md)/[*authentication package*](../secgloss/a-gly.md) (SSP/AP) DLLs into its process space.</span></span> <span data-ttu-id="9d7f5-106">Die folgenden Abbildungen zeigen den Initialisierungs Prozess.</span><span class="sxs-lookup"><span data-stu-id="9d7f5-106">The following illustrations show the initialization process.</span></span>

> [!Note]  
> <span data-ttu-id="9d7f5-107">"Kerberos" stellt den Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP dar, und "My SSP/AP" stellt einen benutzerdefinierten SSP/AP dar, der zwei benutzerdefinierte Sicherheitspakete enthält.</span><span class="sxs-lookup"><span data-stu-id="9d7f5-107">"Kerberos" represents the Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/AP, and "My SSP/AP" represents a custom SSP/AP that contains two custom security packages.</span></span>

 

![LSA-ModusInitialisierung](images/lsamode1.png)

<span data-ttu-id="9d7f5-109">Beim Start Ruft die LSA die Funktion " [**splsamodeinitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) " in jedem SSP/AP auf, um Zeiger auf die Funktionen zu erhalten, die von den einzelnen [*Sicherheitspaketen*](../secgloss/s-gly.md) in der dll implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="9d7f5-109">At startup, the LSA calls the [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) function in each SSP/AP to obtain pointers to the functions implemented by each [*security package*](../secgloss/s-gly.md) in the DLL.</span></span> <span data-ttu-id="9d7f5-110">Die Funktionszeiger werden an die LSA in einem Array von Tabellenstrukturen der [**secpkg- \_ Funktion \_**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) übergeben.</span><span class="sxs-lookup"><span data-stu-id="9d7f5-110">The function pointers are passed to the LSA in an array of [**SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) structures.</span></span>

![der LSA ruft "splsamodeinitialize" auf, um Funktionszeiger zu erhalten.](images/lsamode2.png)

<span data-ttu-id="9d7f5-112">Nachdem der Satz von Tabellenstrukturen der [**secpkg- \_ Funktion \_**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) empfangen wurde, ruft die LSA die [**spinitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) -Funktion jedes Sicherheitspakets auf.</span><span class="sxs-lookup"><span data-stu-id="9d7f5-112">After receiving the set of [**SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) structures, the LSA calls each security package's [**SpInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) function.</span></span> <span data-ttu-id="9d7f5-113">Der LSA verwendet diesen Funktions aufrufsbefehl, um jedes Sicherheitspaket an eine [**LSA \_ secpkg- \_ Funktions \_ Tabellen**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) Struktur zu übergeben, die Zeiger auf die LSA-Unterstützungsfunktionen enthält, die für Sicherheitspakete verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="9d7f5-113">The LSA uses this function call to pass each security package an [**LSA\_SECPKG\_FUNCTION\_TABLE**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) structure, which contains pointers to the LSA support functions available to security packages.</span></span> <span data-ttu-id="9d7f5-114">Zusätzlich zum Speichern der Zeiger auf die LSA-Unterstützungsfunktionen sollten benutzerdefinierte Sicherheitspakete Ihre Implementierung der **spinitialize** -Funktion verwenden, um eine Initialisierungs bezogene Verarbeitung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9d7f5-114">In addition to storing the pointers to the LSA support functions, custom security packages should use their implementation of the **SpInitialize** function to perform any initialization-related processing.</span></span>

<span data-ttu-id="9d7f5-115">Eine Liste der LSA-Unterstützungsfunktionen, die für Sicherheitspakete im LSA-Modus verfügbar sind, finden Sie unter [LSA-Funktionen, die von SSP/APS aufgerufen](authentication-functions.md)werden.</span><span class="sxs-lookup"><span data-stu-id="9d7f5-115">For a list of the LSA support functions available to LSA-mode security packages, see [LSA Functions Called by SSP/APs](authentication-functions.md).</span></span>

<span data-ttu-id="9d7f5-116">Informationen zum Registrieren einer SSP/AP-dll finden Sie unter [Registrieren von SSP/AP-DLLs](registering-ssp-ap-dlls.md).</span><span class="sxs-lookup"><span data-stu-id="9d7f5-116">For information about registering an SSP/AP DLL, see [Registering SSP/AP DLLs](registering-ssp-ap-dlls.md).</span></span>

 

 
