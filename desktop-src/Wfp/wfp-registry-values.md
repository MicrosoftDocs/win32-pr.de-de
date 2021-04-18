---
description: 'Die WFP-Registrierungs Werte befinden sich im folgenden Registrierungsschlüssel: HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon.'
ms.assetid: d4da7f24-1e5d-4ea2-98e8-049e7eaefae1
title: WFP-Registrierungs Werte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb8db23800ebbead68f34eaf0fa9fffd772f01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352527"
---
# <a name="wfp-registry-values"></a><span data-ttu-id="fe898-103">WFP-Registrierungs Werte</span><span class="sxs-lookup"><span data-stu-id="fe898-103">WFP Registry Values</span></span>

<span data-ttu-id="fe898-104">\[WFP-Registrierungs Werte werden ab Windows Vista nicht unterstützt.\]</span><span class="sxs-lookup"><span data-stu-id="fe898-104">\[WFP registry values are not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="fe898-105">WFP verwendet mehrere Registrierungs Werte für Anpassungs Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="fe898-105">WFP uses several registry values for customization settings.</span></span> <span data-ttu-id="fe898-106">Die WFP-Registrierungs Werte befinden sich im folgenden Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="fe898-106">The WFP registry values are located in the following registry key:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               Winlogon
```

<span data-ttu-id="fe898-107">Im folgenden werden die WFP-Registrierungs Werte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fe898-107">The following are the WFP registry values.</span></span>

<dl> <dt>

<span data-ttu-id="fe898-108"><span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**</span><span class="sxs-lookup"><span data-stu-id="fe898-108"><span id="SFCDllCacheDir"></span><span id="sfcdllcachedir"></span><span id="SFCDLLCACHEDIR"></span>**SFCDllCacheDir**</span></span>
</dt> <dd>

<span data-ttu-id="fe898-109">Speicherort des Caches.</span><span class="sxs-lookup"><span data-stu-id="fe898-109">Location of the cache.</span></span> <span data-ttu-id="fe898-110">Dies muss ein lokaler Pfad sein.</span><span class="sxs-lookup"><span data-stu-id="fe898-110">This must be a local path.</span></span> <span data-ttu-id="fe898-111">Der Standardwert ist% SystemRoot% \\ system32 \\ Dllcache.</span><span class="sxs-lookup"><span data-stu-id="fe898-111">The default value is %systemroot%\\system32\\dllcache.</span></span>

</dd> <dt>

<span data-ttu-id="fe898-112"><span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**</span><span class="sxs-lookup"><span data-stu-id="fe898-112"><span id="SFCQuota"></span><span id="sfcquota"></span><span id="SFCQUOTA"></span>**SFCQuota**</span></span>
</dt> <dd>

<span data-ttu-id="fe898-113">Kontingent Optionen.</span><span class="sxs-lookup"><span data-stu-id="fe898-113">Quota options.</span></span> <span data-ttu-id="fe898-114">Bei diesem Registrierungs Wert kann es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="fe898-114">This registry value can be one of the following values.</span></span>



| <span data-ttu-id="fe898-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fe898-115">Value</span></span>                  | <span data-ttu-id="fe898-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fe898-116">Meaning</span></span>                                                  |
|------------------------|----------------------------------------------------------|
| <span data-ttu-id="fe898-117">SFC- \_ Kontingent für \_ alle \_ Dateien</span><span class="sxs-lookup"><span data-stu-id="fe898-117">SFC\_QUOTA\_ALL\_FILES</span></span> | <span data-ttu-id="fe898-118">Die Größe des dll-Caches ist unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="fe898-118">Size of the DLL cache is unlimited.</span></span> <span data-ttu-id="fe898-119">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="fe898-119">This is the default.</span></span> |
| <span data-ttu-id="fe898-120">Andere Werte</span><span class="sxs-lookup"><span data-stu-id="fe898-120">Other values</span></span>           | <span data-ttu-id="fe898-121">Größe des dll-Caches in Dateien.</span><span class="sxs-lookup"><span data-stu-id="fe898-121">Size of the DLL cache, in files.</span></span>                         |



 

</dd> <dt>

<span data-ttu-id="fe898-122"><span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SfcScan**</span><span class="sxs-lookup"><span data-stu-id="fe898-122"><span id="SFCScan"></span><span id="sfcscan"></span><span id="SFCSCAN"></span>**SFCScan**</span></span>
</dt> <dd>

<span data-ttu-id="fe898-123">Überprüfungs Optionen.</span><span class="sxs-lookup"><span data-stu-id="fe898-123">Scan options.</span></span> <span data-ttu-id="fe898-124">Bei diesem Registrierungs Wert kann es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="fe898-124">This registry value can be one of the following values.</span></span>



| <span data-ttu-id="fe898-125">Wert</span><span class="sxs-lookup"><span data-stu-id="fe898-125">Value</span></span>             | <span data-ttu-id="fe898-126">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fe898-126">Meaning</span></span>                                                   |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="fe898-127">SFC- \_ Scan \_ Normal</span><span class="sxs-lookup"><span data-stu-id="fe898-127">SFC\_SCAN\_NORMAL</span></span> | <span data-ttu-id="fe898-128">Überprüfen Sie keine geschützten Dateien beim Start.</span><span class="sxs-lookup"><span data-stu-id="fe898-128">Do not scan protected files at boot.</span></span> <span data-ttu-id="fe898-129">Dies ist die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="fe898-129">This is the default.</span></span> |
| <span data-ttu-id="fe898-130">SFC- \_ Scan \_ immer</span><span class="sxs-lookup"><span data-stu-id="fe898-130">SFC\_SCAN\_ALWAYS</span></span> | <span data-ttu-id="fe898-131">Überprüfen geschützter Dateien bei jedem Start.</span><span class="sxs-lookup"><span data-stu-id="fe898-131">Scan protected files at every boot.</span></span>                       |
| <span data-ttu-id="fe898-132">SFC- \_ Scan einmalig \_</span><span class="sxs-lookup"><span data-stu-id="fe898-132">SFC\_SCAN\_ONCE</span></span>   | <span data-ttu-id="fe898-133">Überprüfen geschützter Dateien beim nächsten Start.</span><span class="sxs-lookup"><span data-stu-id="fe898-133">Scan protected files at the next boot.</span></span>                    |



 

</dd> </dl>

 

 



