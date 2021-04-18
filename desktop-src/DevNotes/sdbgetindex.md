---
description: Ruft den Index für das angegebene Tag und den angegebenen Schlüsseltyp aus der angegebenen Datenbank ab.
ms.assetid: 5fa44252-ba26-43ed-9de0-5917e4ec797c
title: Sdbgetindex-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c7bcc211e4277a2ffee6a68258d7616cb7aa2a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483230"
---
# <a name="sdbgetindex-function"></a><span data-ttu-id="076f9-103">Sdbgetindex-Funktion</span><span class="sxs-lookup"><span data-stu-id="076f9-103">SdbGetIndex function</span></span>

<span data-ttu-id="076f9-104">Ruft den Index für das angegebene Tag und den angegebenen Schlüsseltyp aus der angegebenen Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="076f9-104">Retrieves the index for the specified tag and key type from the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="076f9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="076f9-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetIndex(
  _In_      PDB     pdb,
  _In_      TAG     tWhich,
  _In_      TAG     tKey,
  _Out_opt_ LPDWORD lpdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="076f9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="076f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="076f9-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="076f9-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="076f9-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="076f9-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="076f9-109">*TDas* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="076f9-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="076f9-110">Das-Tag.</span><span class="sxs-lookup"><span data-stu-id="076f9-110">The TAG.</span></span>

</dd> <dt>

<span data-ttu-id="076f9-111">*TKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="076f9-111">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="076f9-112">Der Schlüsseltyp.</span><span class="sxs-lookup"><span data-stu-id="076f9-112">The key type.</span></span>

</dd> <dt>

<span data-ttu-id="076f9-113">*lpdwflags* \[ Out, optional\]</span><span class="sxs-lookup"><span data-stu-id="076f9-113">*lpdwFlags* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="076f9-114">Dieser Parameter kann 0 oder ein eindeutiger **shimdb- \_ Index \_ \_ Schlüssel** (0x00000001) sein.</span><span class="sxs-lookup"><span data-stu-id="076f9-114">This parameter can be 0 or **SHIMDB\_INDEX\_UNIQUE\_KEY** (0x00000001).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="076f9-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="076f9-115">Return value</span></span>

<span data-ttu-id="076f9-116">Die **TagID** des Indexes oder der **TagID \_ null**.</span><span class="sxs-lookup"><span data-stu-id="076f9-116">The **TAGID** of the index or **TAGID\_NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="076f9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="076f9-117">Remarks</span></span>

<span data-ttu-id="076f9-118">Der resultierende Index kann für Lesevorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="076f9-118">The resulting index can be used for read operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="076f9-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="076f9-119">Requirements</span></span>



| <span data-ttu-id="076f9-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="076f9-120">Requirement</span></span> | <span data-ttu-id="076f9-121">Wert</span><span class="sxs-lookup"><span data-stu-id="076f9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="076f9-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="076f9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="076f9-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="076f9-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="076f9-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="076f9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="076f9-125">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="076f9-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="076f9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="076f9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="076f9-127"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="076f9-127"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




