---
description: Gibt die von der sdbgetmatchingexe-Funktion verwendeten Ressourcen frei.
ms.assetid: 4a784f72-2108-4d5e-86e1-1960ac921c8f
title: Sdbreleasematchingexe-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c98d9a79e8942f4bd3ea4c41119825d862de1418
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041387"
---
# <a name="sdbreleasematchingexe-function"></a><span data-ttu-id="2d1b7-103">Sdbreleasematchingexe-Funktion</span><span class="sxs-lookup"><span data-stu-id="2d1b7-103">SdbReleaseMatchingExe function</span></span>

<span data-ttu-id="2d1b7-104">Gibt die von der [**sdbgetmatchingexe**](sdbgetmatchingexe.md) -Funktion verwendeten Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-104">Releases resources used by the [**SdbGetMatchingExe**](sdbgetmatchingexe.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d1b7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d1b7-105">Syntax</span></span>


```C++
void WINAPI SdbReleaseMatchingExe(
  _In_ HSDB   hSDB,
  _In_ TAGREF trExe
);
```



## <a name="parameters"></a><span data-ttu-id="2d1b7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d1b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d1b7-107">*hsdb* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d1b7-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d1b7-108">Ein Handle für die von der [**sdbinitdatabase**](sdbinitdatabase.md) -Funktion zurückgegebene Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="2d1b7-109">*trexe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2d1b7-109">*trExe* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d1b7-110">Die von [**sdbgetmatchingexe**](sdbgetmatchingexe.md)zurückgegebene [**tagref**](tagref.md) .</span><span class="sxs-lookup"><span data-stu-id="2d1b7-110">The [**TAGREF**](tagref.md) returned by [**SdbGetMatchingExe**](sdbgetmatchingexe.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d1b7-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d1b7-111">Return value</span></span>

<span data-ttu-id="2d1b7-112">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="2d1b7-112">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d1b7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d1b7-113">Requirements</span></span>



| <span data-ttu-id="2d1b7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d1b7-114">Requirement</span></span> | <span data-ttu-id="2d1b7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2d1b7-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d1b7-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d1b7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2d1b7-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d1b7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2d1b7-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d1b7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2d1b7-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d1b7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2d1b7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="2d1b7-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d1b7-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d1b7-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d1b7-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d1b7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d1b7-123">**Sdbgetmatchingexe**</span><span class="sxs-lookup"><span data-stu-id="2d1b7-123">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> <dt>

[<span data-ttu-id="2d1b7-124">**Sdbinitdatabase**</span><span class="sxs-lookup"><span data-stu-id="2d1b7-124">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




