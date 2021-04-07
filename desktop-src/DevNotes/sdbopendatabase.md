---
description: Öffnet die angegebene Shimdatenbank.
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: Sdbopendatabase-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ae0bca035f203593c43bb36e70119fbaf3024059
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747856"
---
# <a name="sdbopendatabase-function"></a><span data-ttu-id="1b470-103">Sdbopendatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="1b470-103">SdbOpenDatabase function</span></span>

<span data-ttu-id="1b470-104">Öffnet die angegebene Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="1b470-104">Opens the specified shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b470-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b470-105">Syntax</span></span>


```C++
PDB WINAPI SdbOpenDatabase(
  _In_ LPCTSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a><span data-ttu-id="1b470-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b470-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b470-107">*pwszpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b470-107">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b470-108">Der Daten Bank Pfad.</span><span class="sxs-lookup"><span data-stu-id="1b470-108">The database path.</span></span> <span data-ttu-id="1b470-109">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="1b470-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1b470-110">*ETYPE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b470-110">*eType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b470-111">Der Pfadtyp.</span><span class="sxs-lookup"><span data-stu-id="1b470-111">The path type.</span></span> <span data-ttu-id="1b470-112">Eine Liste der Werte finden Sie unter [**path \_ Type**](path-type.md) .</span><span class="sxs-lookup"><span data-stu-id="1b470-112">See [**PATH\_TYPE**](path-type.md) for a list of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b470-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b470-113">Return value</span></span>

<span data-ttu-id="1b470-114">Die-Funktion gibt ein Handle für die Shimdatenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="1b470-114">The function returns a handle to the shim database.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b470-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b470-115">Requirements</span></span>



| <span data-ttu-id="1b470-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b470-116">Requirement</span></span> | <span data-ttu-id="1b470-117">Wert</span><span class="sxs-lookup"><span data-stu-id="1b470-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1b470-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b470-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1b470-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b470-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1b470-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b470-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1b470-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b470-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1b470-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1b470-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b470-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b470-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b470-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b470-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b470-125">**Sdbkreatedatabase**</span><span class="sxs-lookup"><span data-stu-id="1b470-125">**SdbCreateDatabase**</span></span>](sdbcreatedatabase.md)
</dt> </dl>

 

 




