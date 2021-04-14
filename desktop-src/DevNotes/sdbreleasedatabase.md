---
description: Schließt die mit der sdbinitdatabase-Funktion initialisierte Shimdatenbank.
ms.assetid: 8452ab14-a1e9-41b3-a1ac-7ff3a7d3a7ed
title: Sdbreleasedatabase-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7df4b62af6b2fe654269a8bea4b2e866d0d765b3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523336"
---
# <a name="sdbreleasedatabase-function"></a><span data-ttu-id="3dd5c-103">Sdbreleasedatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="3dd5c-103">SdbReleaseDatabase function</span></span>

<span data-ttu-id="3dd5c-104">Schließt die mit der [**sdbinitdatabase**](sdbinitdatabase.md) -Funktion initialisierte Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="3dd5c-104">Closes the shim database initialized using the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dd5c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3dd5c-105">Syntax</span></span>


```C++
void WINAPI SdbReleaseDatabase(
  _In_ HSDB hSDB
);
```



## <a name="parameters"></a><span data-ttu-id="3dd5c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3dd5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3dd5c-107">*hsdb* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3dd5c-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3dd5c-108">Ein Handle für die von der [**sdbinitdatabase**](sdbinitdatabase.md) -Funktion zurückgegebene Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="3dd5c-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3dd5c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3dd5c-109">Return value</span></span>

<span data-ttu-id="3dd5c-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3dd5c-110">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3dd5c-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3dd5c-111">Requirements</span></span>



| <span data-ttu-id="3dd5c-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3dd5c-112">Requirement</span></span> | <span data-ttu-id="3dd5c-113">Wert</span><span class="sxs-lookup"><span data-stu-id="3dd5c-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dd5c-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3dd5c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3dd5c-115">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3dd5c-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3dd5c-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3dd5c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3dd5c-117">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3dd5c-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3dd5c-118">DLL</span><span class="sxs-lookup"><span data-stu-id="3dd5c-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dd5c-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dd5c-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dd5c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dd5c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dd5c-121">**Sdbinitdatabase**</span><span class="sxs-lookup"><span data-stu-id="3dd5c-121">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




