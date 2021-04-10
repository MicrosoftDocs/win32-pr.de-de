---
description: Ruft das Tag ab, das mit der angegebenen TagID verknüpft ist.
ms.assetid: 194d2035-fc2c-445d-a730-90db2ccea8af
title: Sdbgettagfromtagid-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetTagFromTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: d81dac026a9b6acc921586aaded54c8c90ad5bdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126722"
---
# <a name="sdbgettagfromtagid-function"></a><span data-ttu-id="ce59f-103">Sdbgettagfromtagid-Funktion</span><span class="sxs-lookup"><span data-stu-id="ce59f-103">SdbGetTagFromTagID function</span></span>

<span data-ttu-id="ce59f-104">Ruft das Tag ab, das mit der angegebenen **TagID** verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="ce59f-104">Retrieves the TAG associated with the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce59f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce59f-105">Syntax</span></span>


```C++
TAG WINAPI SdbGetTagFromTagID(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="ce59f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce59f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce59f-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce59f-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce59f-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="ce59f-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="ce59f-109">*tiwhat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ce59f-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce59f-110">Die **TagID** für das Tag.</span><span class="sxs-lookup"><span data-stu-id="ce59f-110">The **TAGID** for the TAG.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce59f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce59f-111">Return value</span></span>

<span data-ttu-id="ce59f-112">Die-Funktion gibt das-Tag zurück.</span><span class="sxs-lookup"><span data-stu-id="ce59f-112">The function returns the TAG.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce59f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce59f-113">Requirements</span></span>



| <span data-ttu-id="ce59f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce59f-114">Requirement</span></span> | <span data-ttu-id="ce59f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ce59f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce59f-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce59f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ce59f-117">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce59f-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ce59f-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce59f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ce59f-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce59f-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ce59f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ce59f-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce59f-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce59f-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce59f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce59f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce59f-123">**Tag**</span><span class="sxs-lookup"><span data-stu-id="ce59f-123">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="ce59f-124">**TagID**</span><span class="sxs-lookup"><span data-stu-id="ce59f-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




