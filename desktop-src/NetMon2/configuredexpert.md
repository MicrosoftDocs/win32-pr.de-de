---
description: Die Struktur "konfiguritsxpert" ordnet einen Experten seinen Konfigurationsdaten zu.
ms.assetid: 96a6650b-6d6f-495e-83bb-385d44ff015d
title: Konfigurier-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONFIGUREDEXPERT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3f3d40bf5d38c6b5151691a7d15bd93bef01eee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216219"
---
# <a name="configuredexpert-structure"></a><span data-ttu-id="93ce1-103">Konfigurier-Struktur</span><span class="sxs-lookup"><span data-stu-id="93ce1-103">CONFIGUREDEXPERT structure</span></span>

<span data-ttu-id="93ce1-104">Die Struktur " **konfiguritsxpert** " ordnet einen Experten seinen Konfigurationsdaten zu.</span><span class="sxs-lookup"><span data-stu-id="93ce1-104">The **CONFIGUREDEXPERT** structure associates an expert with its configuration data.</span></span>

## <a name="syntax"></a><span data-ttu-id="93ce1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="93ce1-105">Syntax</span></span>


```C++
typedef struct {
  HEXPERT       hExpert;
  DWORD         StartupFlags;
  PEXPERTCONFIG pConfig;
} CONFIGUREDEXPERT, *PCONFIGUREDEXPERT;
```



## <a name="members"></a><span data-ttu-id="93ce1-106">Member</span><span class="sxs-lookup"><span data-stu-id="93ce1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="93ce1-107">**hexpert**</span><span class="sxs-lookup"><span data-stu-id="93ce1-107">**hExpert**</span></span>
</dt> <dd>

<span data-ttu-id="93ce1-108">Handle für einen Experten.</span><span class="sxs-lookup"><span data-stu-id="93ce1-108">Handle to an expert.</span></span>

</dd> <dt>

<span data-ttu-id="93ce1-109">**StartupFlags**</span><span class="sxs-lookup"><span data-stu-id="93ce1-109">**StartupFlags**</span></span>
</dt> <dd>

<span data-ttu-id="93ce1-110">Startflag-Werte des Experten.</span><span class="sxs-lookup"><span data-stu-id="93ce1-110">Startup flag values of the expert.</span></span>

</dd> <dt>

<span data-ttu-id="93ce1-111">**pConfig**</span><span class="sxs-lookup"><span data-stu-id="93ce1-111">**pConfig**</span></span>
</dt> <dd>

<span data-ttu-id="93ce1-112">Zeiger auf eine " [**expertenconfig**](expertconfig.md) "-Struktur.</span><span class="sxs-lookup"><span data-stu-id="93ce1-112">Pointer to an [**EXPERTCONFIG**](expertconfig.md) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93ce1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93ce1-113">Requirements</span></span>



| <span data-ttu-id="93ce1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93ce1-114">Requirement</span></span> | <span data-ttu-id="93ce1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="93ce1-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="93ce1-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93ce1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="93ce1-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93ce1-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="93ce1-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93ce1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="93ce1-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="93ce1-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="93ce1-120">Header</span><span class="sxs-lookup"><span data-stu-id="93ce1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="93ce1-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="93ce1-121"><dt>Netmon.h</dt></span></span> </dl> |



 

 




