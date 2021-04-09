---
description: "\"Cabinetdllversioninfo\" enthält die Versionsinformationen für Cabinet.dll."
ms.assetid: 1dc6962c-3087-4f56-8b65-fbf55e17eeb6
title: Cabinetdllversioninfo-Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CABINETDLLVERSIONINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: b6dfcd68f1bc684554d45feb13b9976465b70efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861008"
---
# <a name="cabinetdllversioninfo-structure"></a><span data-ttu-id="72af4-103">Cabinetdllversioninfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="72af4-103">CABINETDLLVERSIONINFO structure</span></span>

<span data-ttu-id="72af4-104">\[Diese Struktur enthält Informationen, die nur erforderlich sind, wenn die **dllgetversion** -Funktion verwendet wird, die nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="72af4-104">\[This structure contains information required only when using the **DllGetVersion** function, which is not supported.</span></span> <span data-ttu-id="72af4-105">Diese Dokumentation wird nur zu Informationszwecken bereitgestellt.\]</span><span class="sxs-lookup"><span data-stu-id="72af4-105">This documentation is provided for informational purposes only.\]</span></span>

<span data-ttu-id="72af4-106">" **Cabinetdllversioninfo** " enthält die Versionsinformationen für Cabinet.dll.</span><span class="sxs-lookup"><span data-stu-id="72af4-106">The **CABINETDLLVERSIONINFO** contains the version information for Cabinet.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="72af4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="72af4-107">Syntax</span></span>


```C++
typedef struct {
  DWORD cbStruct;
  DWORD dwReserved1;
  DWORD dwReserved2;
  DWORD dwFileVersionMS;
  DWORD dwFileVersionLS;
} CABINETDLLVERSIONINFO, *PCABINETDLLVERSIONINFO;
```



## <a name="members"></a><span data-ttu-id="72af4-108">Member</span><span class="sxs-lookup"><span data-stu-id="72af4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="72af4-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="72af4-109">**cbStruct**</span></span>
</dt> <dd>

<span data-ttu-id="72af4-110">Die Größe der-Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="72af4-110">The size of this structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="72af4-111">**dwReserved1**</span><span class="sxs-lookup"><span data-stu-id="72af4-111">**dwReserved1**</span></span>
</dt> <dd>

<span data-ttu-id="72af4-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="72af4-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="72af4-113">**dwReserved2**</span><span class="sxs-lookup"><span data-stu-id="72af4-113">**dwReserved2**</span></span>
</dt> <dd>

<span data-ttu-id="72af4-114">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="72af4-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="72af4-115">**dwfileversionms**</span><span class="sxs-lookup"><span data-stu-id="72af4-115">**dwFileVersionMS**</span></span>
</dt> <dd>

<span data-ttu-id="72af4-116">Enthält die wichtigsten Bits der Versionsinformationen.</span><span class="sxs-lookup"><span data-stu-id="72af4-116">Contains the most significant bits of the version information.</span></span> <span data-ttu-id="72af4-117">Bits 0-15 enthalten die neben Version, und Bits 16-31 enthalten die Hauptversion.</span><span class="sxs-lookup"><span data-stu-id="72af4-117">Bits 0-15 contain the minor version, and bits 16-31 contain the major version.</span></span>

</dd> <dt>

<span data-ttu-id="72af4-118">**dwfileversionls**</span><span class="sxs-lookup"><span data-stu-id="72af4-118">**dwFileVersionLS**</span></span>
</dt> <dd>

<span data-ttu-id="72af4-119">Enthält die am wenigsten wichtigen Bits der Versionsinformationen.</span><span class="sxs-lookup"><span data-stu-id="72af4-119">Contains the least significant bits of the version information.</span></span> <span data-ttu-id="72af4-120">Bits 0-15 enthalten die Revisionsnummer, und Bits 16-31 enthalten die Buildnummer.</span><span class="sxs-lookup"><span data-stu-id="72af4-120">Bits 0-15 contain the revision number, and bits 16-31 contain the build number.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="72af4-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72af4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72af4-122">**Dllgetversion**</span><span class="sxs-lookup"><span data-stu-id="72af4-122">**DllGetVersion**</span></span>](dllgetversion.md)
</dt> </dl>

 

 



