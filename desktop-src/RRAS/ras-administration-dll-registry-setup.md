---
title: Informationen zur Registrierungs Einrichtung der RAS-Verwaltung
description: Das Setup Programm für eine Drittanbieter-RAS-Verwaltungs-dll muss die dll bei RAS registrieren, indem Sie Informationen unter dem folgenden Schlüssel in der Registrierung bereitstellt.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- RAS-Administration-RRAS, Einrichten der DLL-Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cf487f792a4add9ebf61e8f866b9f0577fb468d
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "103857827"
---
# <a name="about-ras-administration-dll-registry-setup"></a><span data-ttu-id="e9bd6-104">Informationen zur Registrierungs Einrichtung der RAS-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="e9bd6-104">About RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="e9bd6-105">Das Setup Programm für eine Drittanbieter-RAS-Verwaltungs-dll muss die dll bei RAS registrieren, indem Sie Informationen unter dem folgenden Schlüssel in der Registrierung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e9bd6-105">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="e9bd6-106">Um die dll zu registrieren, legen Sie die folgenden Werte unter diesem Schlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="e9bd6-106">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="e9bd6-107">Wertname</span><span class="sxs-lookup"><span data-stu-id="e9bd6-107">Value name</span></span>    | <span data-ttu-id="e9bd6-108">Wertdaten</span><span class="sxs-lookup"><span data-stu-id="e9bd6-108">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="e9bd6-109">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="e9bd6-109">*DisplayName*</span></span> | <span data-ttu-id="e9bd6-110">Eine **reg \_ SZ** -Zeichenfolge, die den benutzerfreundlichen anzeigen amen der dll enthält.</span><span class="sxs-lookup"><span data-stu-id="e9bd6-110">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="e9bd6-111">*Dll*</span><span class="sxs-lookup"><span data-stu-id="e9bd6-111">*DLLPath*</span></span>     | <span data-ttu-id="e9bd6-112">Eine **reg- \_ SZ** -Zeichenfolge, die den vollständigen Pfad der dll enthält.</span><span class="sxs-lookup"><span data-stu-id="e9bd6-112">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="e9bd6-113">Da RAS mehrere RAS-Verwaltungs-DLLs unterstützt, kann der Registrierungs Wert **DllPath** eine durch Semikolons getrennte Liste von Pfaden enthalten.</span><span class="sxs-lookup"><span data-stu-id="e9bd6-113">Because RAS supports multiple RAS Administration DLLs, the registry value **DLLPath** can contain a semi-colon delimited list of paths.</span></span> <span data-ttu-id="e9bd6-114">Beispielsweise könnte der Registrierungs Eintrag für eine RAS-Verwaltungs-dll von einem fiktiven Unternehmen mit dem Namen ProElectron, Inc. wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="e9bd6-114">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc., might be the following:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="e9bd6-115">*Display Name*: **reg \_ SZ** : ProElectron RAS admin dll</span><span class="sxs-lookup"><span data-stu-id="e9bd6-115">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="e9bd6-116">*DllPath*: **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll; C: \\ NT \\ system32 \\ntwkadm2.dll</span><span class="sxs-lookup"><span data-stu-id="e9bd6-116">*DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll; C:\\nt\\system32\\ntwkadm2.dll</span></span>

<span data-ttu-id="e9bd6-117">RAS Ruft die DLLs in der Reihenfolge auf, in der Sie in diesem Registrierungs Wert aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="e9bd6-117">RAS calls the DLLs in the order in which they are listed in this registry value.</span></span> <span data-ttu-id="e9bd6-118">Der Registrierungs Wert *Display Name* enthält immer noch nur einen einzigen anzeigen Amen.</span><span class="sxs-lookup"><span data-stu-id="e9bd6-118">The registry value *DisplayName* still contains only a single display name.</span></span>

<span data-ttu-id="e9bd6-119">Das Setup Programm für eine RAS-Verwaltungs-dll muss ebenfalls die Funktionen zum Entfernen und deinstallieren bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e9bd6-119">The setup program for a RAS administration DLL must also provide remove and uninstall functionality.</span></span> <span data-ttu-id="e9bd6-120">Wenn ein Benutzer die dll entfernt, muss das Setup Programm die Registrierungseinträge für die dll löschen.</span><span class="sxs-lookup"><span data-stu-id="e9bd6-120">If a user removes the DLL, the setup program must delete the registry entries for the DLL.</span></span>

<span data-ttu-id="e9bd6-121">**Windows 2000/NT:** RAS unterstützt nur eine RAS-Verwaltungs-dll, sodass der Registrierungs Wert ' **DllPath** ' keine durch Semikolons getrennte Liste von Pfaden enthalten darf.</span><span class="sxs-lookup"><span data-stu-id="e9bd6-121">**Windows 2000/NT:** RAS supports only one RAS Administration DLL, so the registry value **DLLPath** cannot contain a semi-colon delimited list of paths.</span></span>

 

 




