---
description: Die Struktur "expertconfig" enthält die Konfigurationsdaten des Experten. Der Experte überlagert den rawConfigData-Member mit einer expertenspezifischen Struktur.
ms.assetid: 6167e846-d58c-40a8-94f7-c6d6185ae724
title: Expertenconfig-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTCONFIG
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 293bdf4c792c10232564a7ba6386df430e81ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342822"
---
# <a name="expertconfig-structure"></a><span data-ttu-id="26e44-104">Expertenkonfigurations-Struktur</span><span class="sxs-lookup"><span data-stu-id="26e44-104">EXPERTCONFIG structure</span></span>

<span data-ttu-id="26e44-105">Die Struktur " **expertconfig** " enthält die Konfigurationsdaten des Experten.</span><span class="sxs-lookup"><span data-stu-id="26e44-105">The **EXPERTCONFIG** structure contains the configuration data of the expert.</span></span> <span data-ttu-id="26e44-106">Der Experte überlagert den **rawConfigData** -Member mit einer expertenspezifischen Struktur.</span><span class="sxs-lookup"><span data-stu-id="26e44-106">The expert overlays the **RawConfigData** member with an expert-specific structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="26e44-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="26e44-107">Syntax</span></span>


```C++
typedef struct {
  DWORD RawConfigLength;
  BYTE  RawConfigData[];
} EXPERTCONFIG, *PEXPERTCONFIG;
```



## <a name="members"></a><span data-ttu-id="26e44-108">Member</span><span class="sxs-lookup"><span data-stu-id="26e44-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="26e44-109">**Rawconfiglength**</span><span class="sxs-lookup"><span data-stu-id="26e44-109">**RawConfigLength**</span></span>
</dt> <dd>

<span data-ttu-id="26e44-110">Gesamtlänge der Struktur, einschließlich der vier Bytes, die für den Member verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26e44-110">Total length of the structure, including the four bytes used for the member.</span></span> <span data-ttu-id="26e44-111">Netzwerkmonitor verwendet den-Wert, wenn die Struktur in einem Laufwerk gespeichert und von diesem gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="26e44-111">Network Monitor uses the value when the structure is saved-to and read-from a disk drive.</span></span>

</dd> <dt>

<span data-ttu-id="26e44-112">**RawConfigData**</span><span class="sxs-lookup"><span data-stu-id="26e44-112">**RawConfigData**</span></span>
</dt> <dd>

<span data-ttu-id="26e44-113">Konfigurationsdaten.</span><span class="sxs-lookup"><span data-stu-id="26e44-113">Configuration data.</span></span> <span data-ttu-id="26e44-114">Der Experte muss die Konfigurationsdaten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="26e44-114">The expert must add the configuration data.</span></span> <span data-ttu-id="26e44-115">Angenommen, Sie verfügen über eine Datenstruktur, die wie folgt aussieht.</span><span class="sxs-lookup"><span data-stu-id="26e44-115">For example, suppose that you had a data structure that looked like this.</span></span>

``` syntax
typedef struct
{
    DWORD       RawConfigLength;   // Overlay of structure
    DWORD       PickNumEvents;
    DWORD       NumEventsSpecific;
    DWORD       PickSpeedThroughCapture;
    DWORD       PickStartup;
    DWORD       PickAttachProperties;
} TESTEXPERTCONFIG;
typedef TESTEXPERTCONFIG* LPTESTEXPERTCONFIG;
```

<span data-ttu-id="26e44-116">Beachten Sie, dass **rawconfiglength** sicherstellt, dass das Overlay ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="26e44-116">Note that **RawConfigLength** ensures that the overlay works correctly.</span></span> <span data-ttu-id="26e44-117">Wenn Sie die Daten verwenden, könnte Ihr Code wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="26e44-117">When you use the data, your code might look like this:</span></span>

``` syntax
BOOL WINAPI Configure( 
    HEXPERTKEY ExpertKey,
    PEXPERTCONFIG * ppConfig,
    PEXPERTSTARTUPINFO pStartupInfo,
    DWORD StartupFlags,
    HWND hWnd
)
{
    LPTESTEXPERTCONFIG  lpConfig;

    //...
    lpConfig = (LPTESTEXPERTCONFIG)(*ppConfig);
    //...
}
```

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26e44-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26e44-118">Requirements</span></span>



| <span data-ttu-id="26e44-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26e44-119">Requirement</span></span> | <span data-ttu-id="26e44-120">Wert</span><span class="sxs-lookup"><span data-stu-id="26e44-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="26e44-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26e44-121">Minimum supported client</span></span><br/> | <span data-ttu-id="26e44-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26e44-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="26e44-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26e44-123">Minimum supported server</span></span><br/> | <span data-ttu-id="26e44-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="26e44-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="26e44-125">Header</span><span class="sxs-lookup"><span data-stu-id="26e44-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="26e44-126"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="26e44-126"><dt>Netmon.h</dt></span></span> </dl> |



 

 




