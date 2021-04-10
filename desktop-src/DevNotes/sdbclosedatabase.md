---
description: Schließt die angegebene Shimdatenbank.
ms.assetid: e4480860-8055-4134-b6ed-926c010d462f
title: Sdbclosedatabase-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 376d97b8386f127a945cb118639be1e38ae68737
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041421"
---
# <a name="sdbclosedatabase-function"></a><span data-ttu-id="d3c26-103">Sdbclosedatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="d3c26-103">SdbCloseDatabase function</span></span>

<span data-ttu-id="d3c26-104">Schließt die angegebene Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="d3c26-104">Closes the specified shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c26-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3c26-105">Syntax</span></span>


```C++
void WINAPI SdbCloseDatabase(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="d3c26-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3c26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3c26-107">*PDB* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d3c26-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c26-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="d3c26-108">A handle to the shim database.</span></span> <span data-ttu-id="d3c26-109">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="d3c26-109">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3c26-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3c26-110">Return value</span></span>

<span data-ttu-id="d3c26-111">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d3c26-111">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3c26-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d3c26-112">Requirements</span></span>



| <span data-ttu-id="d3c26-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3c26-113">Requirement</span></span> | <span data-ttu-id="d3c26-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d3c26-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c26-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3c26-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d3c26-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3c26-116">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d3c26-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3c26-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d3c26-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3c26-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d3c26-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d3c26-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3c26-120"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3c26-120"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3c26-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3c26-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c26-122">**Sdbopendatabase**</span><span class="sxs-lookup"><span data-stu-id="d3c26-122">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




