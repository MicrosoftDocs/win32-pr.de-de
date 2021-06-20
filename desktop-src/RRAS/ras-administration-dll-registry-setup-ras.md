---
title: Setup der RAS-Verwaltungs-DLL-Registrierung
description: Machen Sie sich mit den Anforderungen für die Registrierung einer RAS-Verwaltungs-DLL (Remote Access Service) eines Drittanbieters bei RAS bewusst.
ms.assetid: 8108a0ac-8562-4251-99be-5f2b2f5c67c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed0af8e4b189de69f254429c18beb4756e01ad56
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406713"
---
# <a name="ras-administration-dll-registry-setup"></a><span data-ttu-id="01600-103">Setup der RAS-Verwaltungs-DLL-Registrierung</span><span class="sxs-lookup"><span data-stu-id="01600-103">RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="01600-104">Das Setupprogramm für eine RAS-Verwaltungs-DLL eines Drittanbieters muss die DLL bei RAS registrieren, indem Informationen unter dem folgenden Schlüssel in der Registrierung zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="01600-104">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="01600-105">Legen Sie zum Registrieren der DLL die folgenden Werte unter diesem Schlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="01600-105">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="01600-106">Wertname</span><span class="sxs-lookup"><span data-stu-id="01600-106">Value name</span></span>    | <span data-ttu-id="01600-107">Wertdaten</span><span class="sxs-lookup"><span data-stu-id="01600-107">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="01600-108">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="01600-108">*DisplayName*</span></span> | <span data-ttu-id="01600-109">Eine **REG \_ SZ-Zeichenfolge,** die den benutzerfreundlichen Anzeigenamen der DLL enthält.</span><span class="sxs-lookup"><span data-stu-id="01600-109">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="01600-110">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="01600-110">*DLLPath*</span></span>     | <span data-ttu-id="01600-111">Eine **REG \_ SZ-Zeichenfolge,** die den vollständigen Pfad der DLL enthält.</span><span class="sxs-lookup"><span data-stu-id="01600-111">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="01600-112">Der Registrierungseintrag für eine RAS-Verwaltungs-DLL eines fiktiven Unternehmens mit dem Namen ProElecron, Inc. kann beispielsweise wie im Folgenden beschrieben sein:</span><span class="sxs-lookup"><span data-stu-id="01600-112">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="01600-113">*DisplayName* : **REG \_ SZ** : ProElecron RAS Admin DLL</span><span class="sxs-lookup"><span data-stu-id="01600-113">*DisplayName* : **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="01600-114">*DLLPath* : **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="01600-114">*DLLPath* : **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="01600-115">Das Setupprogramm für eine RAS-Verwaltungs-DLL sollte auch Funktionen zum Entfernen/Deinstallieren bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="01600-115">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="01600-116">Wenn ein Benutzer die DLL entfernt, sollte das Setupprogramm die Registrierungseinträge der DLL löschen.</span><span class="sxs-lookup"><span data-stu-id="01600-116">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 




