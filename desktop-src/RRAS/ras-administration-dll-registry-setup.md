---
title: Informationen zum Setup der RAS-Verwaltungs-DLL-Registrierung
description: Machen Sie sich mit den Anforderungen für die Registrierung einer RAS-Verwaltungs-DLL (Remote Access Service) eines Drittanbieters bei RAS bewusst. RAS unterstützt mehrere RAS-Verwaltungs-DLLs.
ms.assetid: e83a5e37-a39d-4465-abc9-653cdd56893b
keywords:
- RAS-Administration RRAS , SETUP DER DLL-Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b9a7b7c48422264a890a74b1bab36e61672f11d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406663"
---
# <a name="about-ras-administration-dll-registry-setup"></a><span data-ttu-id="d37f7-105">Informationen zum Setup der RAS-Verwaltungs-DLL-Registrierung</span><span class="sxs-lookup"><span data-stu-id="d37f7-105">About RAS Administration DLL Registry Setup</span></span>

<span data-ttu-id="d37f7-106">Das Setupprogramm für eine RAS-Verwaltungs-DLL eines Drittanbieters muss die DLL bei RAS registrieren, indem Informationen unter dem folgenden Schlüssel in der Registrierung zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d37f7-106">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="d37f7-107">Legen Sie zum Registrieren der DLL die folgenden Werte unter diesem Schlüssel fest.</span><span class="sxs-lookup"><span data-stu-id="d37f7-107">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="d37f7-108">Wertname</span><span class="sxs-lookup"><span data-stu-id="d37f7-108">Value name</span></span>    | <span data-ttu-id="d37f7-109">Wertdaten</span><span class="sxs-lookup"><span data-stu-id="d37f7-109">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="d37f7-110">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="d37f7-110">*DisplayName*</span></span> | <span data-ttu-id="d37f7-111">Eine **REG \_ SZ-Zeichenfolge,** die den benutzerfreundlichen Anzeigenamen der DLL enthält.</span><span class="sxs-lookup"><span data-stu-id="d37f7-111">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="d37f7-112">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="d37f7-112">*DLLPath*</span></span>     | <span data-ttu-id="d37f7-113">Eine **REG \_ SZ-Zeichenfolge,** die den vollständigen Pfad der DLL enthält.</span><span class="sxs-lookup"><span data-stu-id="d37f7-113">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="d37f7-114">Da RAS mehrere RAS-Verwaltungs-DLLs unterstützt, kann der Registrierungswert **DLLPath** eine durch Semikolons getrennte Liste von Pfaden enthalten.</span><span class="sxs-lookup"><span data-stu-id="d37f7-114">Because RAS supports multiple RAS Administration DLLs, the registry value **DLLPath** can contain a semi-colon delimited list of paths.</span></span> <span data-ttu-id="d37f7-115">Der Registrierungseintrag für eine RAS-Verwaltungs-DLL eines fiktiven Unternehmens namens ProElecaku, Inc. kann beispielsweise wie folgt sein:</span><span class="sxs-lookup"><span data-stu-id="d37f7-115">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc., might be the following:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="d37f7-116">*DisplayName*: **REG \_ SZ** : ProElecron RAS Admin DLL</span><span class="sxs-lookup"><span data-stu-id="d37f7-116">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL</span></span>

<span data-ttu-id="d37f7-117">*DLLPath*: **REG \_ SZ** : C: \\ nt \\ system32 \\ntwkadm.dll; C: \\ nt \\ system32 \\ntwkadm2.dll</span><span class="sxs-lookup"><span data-stu-id="d37f7-117">*DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll; C:\\nt\\system32\\ntwkadm2.dll</span></span>

<span data-ttu-id="d37f7-118">RAS ruft die DLLs in der Reihenfolge auf, in der sie in diesem Registrierungswert aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="d37f7-118">RAS calls the DLLs in the order in which they are listed in this registry value.</span></span> <span data-ttu-id="d37f7-119">Der Registrierungswert *DisplayName* enthält immer noch nur einen einzigen Anzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="d37f7-119">The registry value *DisplayName* still contains only a single display name.</span></span>

<span data-ttu-id="d37f7-120">Das Setupprogramm für eine RAS-Verwaltungs-DLL muss auch Funktionen zum Entfernen und Deinstallieren bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d37f7-120">The setup program for a RAS administration DLL must also provide remove and uninstall functionality.</span></span> <span data-ttu-id="d37f7-121">Wenn ein Benutzer die DLL entfernt, muss das Setupprogramm die Registrierungseinträge für die DLL löschen.</span><span class="sxs-lookup"><span data-stu-id="d37f7-121">If a user removes the DLL, the setup program must delete the registry entries for the DLL.</span></span>

<span data-ttu-id="d37f7-122">**Windows 2000/NT:** RAS unterstützt nur eine RAS-Verwaltungs-DLL, sodass der Registrierungswert **DLLPath** keine durch Semikolons getrennte Liste von Pfaden enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="d37f7-122">**Windows 2000/NT:** RAS supports only one RAS Administration DLL, so the registry value **DLLPath** cannot contain a semi-colon delimited list of paths.</span></span>

 

 




