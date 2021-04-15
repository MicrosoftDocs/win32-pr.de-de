---
title: Registrierungs Einrichtung der RAS-Verwaltungs-dll
description: Das Setup Programm für eine Drittanbieter-RAS-Verwaltungs-dll muss die dll bei RAS registrieren, indem Sie Informationen unter dem folgenden Schlüssel in der Registrierung bereitstellt.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0aed28fc41334c161a11ce5575b6395c4bb5da5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516023"
---
# <a name="ras-administration-dll-registry-setup"></a><span data-ttu-id="29d3d-103">Registrierungs Einrichtung der RAS-Verwaltungs-dll</span><span class="sxs-lookup"><span data-stu-id="29d3d-103">RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="29d3d-104">Das Setup Programm für eine Drittanbieter-RAS-Verwaltungs-dll muss die dll bei RAS registrieren, indem Sie Informationen unter dem folgenden Schlüssel in der Registrierung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="29d3d-104">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="29d3d-105">Um die dll zu registrieren, legen Sie die folgenden Werte unter diesem Schlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="29d3d-105">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="29d3d-106">Wertname</span><span class="sxs-lookup"><span data-stu-id="29d3d-106">Value name</span></span>    | <span data-ttu-id="29d3d-107">Wertdaten</span><span class="sxs-lookup"><span data-stu-id="29d3d-107">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="29d3d-108">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="29d3d-108">*DisplayName*</span></span> | <span data-ttu-id="29d3d-109">Eine **reg \_ SZ** -Zeichenfolge, die den benutzerfreundlichen anzeigen amen der dll enthält.</span><span class="sxs-lookup"><span data-stu-id="29d3d-109">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="29d3d-110">*Dll*</span><span class="sxs-lookup"><span data-stu-id="29d3d-110">*DLLPath*</span></span>     | <span data-ttu-id="29d3d-111">Eine **reg- \_ SZ** -Zeichenfolge, die den vollständigen Pfad der dll enthält.</span><span class="sxs-lookup"><span data-stu-id="29d3d-111">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="29d3d-112">Beispielsweise könnte der Registrierungs Eintrag für eine RAS-Verwaltungs-dll von einem fiktiven Unternehmen mit dem Namen ProElectron, Inc. wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="29d3d-112">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="29d3d-113">*Display Name* : **reg \_ SZ** : ProElectron RAS admin dll</span><span class="sxs-lookup"><span data-stu-id="29d3d-113">*DisplayName* : **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="29d3d-114">*DllPath* : **reg \_ SZ** : C: \\ NT \\ system32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="29d3d-114">*DLLPath* : **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="29d3d-115">Das Setup Programm für eine RAS-Verwaltungs-dll sollte auch Funktionen zum Entfernen/Deinstallieren bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="29d3d-115">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="29d3d-116">Wenn ein Benutzer die dll entfernt, sollte das Setup Programm die Registrierungseinträge der dll löschen.</span><span class="sxs-lookup"><span data-stu-id="29d3d-116">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 




