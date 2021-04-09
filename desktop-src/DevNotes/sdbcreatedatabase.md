---
description: Erstellt eine neue Shimdatenbank.
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: Sdbkreatedatabase-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCreateDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 1ab8b8071cc210f6129545985d2d2e089680f0f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958364"
---
# <a name="sdbcreatedatabase-function"></a><span data-ttu-id="5e4fc-103">Sdbkreatedatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="5e4fc-103">SdbCreateDatabase function</span></span>

<span data-ttu-id="5e4fc-104">Erstellt eine neue Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="5e4fc-104">Creates a new shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e4fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e4fc-105">Syntax</span></span>


```C++
PDB WINAPI SdbCreateDatabase(
  _In_ LPCWSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a><span data-ttu-id="5e4fc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e4fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e4fc-107">*pwszpath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e4fc-107">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e4fc-108">Der Pfad, in dem die Datenbank gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e4fc-108">The path where the database should be saved.</span></span> <span data-ttu-id="5e4fc-109">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="5e4fc-109">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5e4fc-110">*ETYPE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5e4fc-110">*eType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e4fc-111">Der Pfadtyp.</span><span class="sxs-lookup"><span data-stu-id="5e4fc-111">The path type.</span></span> <span data-ttu-id="5e4fc-112">Eine Liste der Werte finden Sie unter [**path \_ Type**](path-type.md) .</span><span class="sxs-lookup"><span data-stu-id="5e4fc-112">See [**PATH\_TYPE**](path-type.md) for a list of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e4fc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e4fc-113">Return value</span></span>

<span data-ttu-id="5e4fc-114">Die-Funktion gibt ein Handle für die Shimdatenbank oder **null** bei einem Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="5e4fc-114">The function returns a handle to the shim database or **NULL** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e4fc-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e4fc-115">Requirements</span></span>



| <span data-ttu-id="5e4fc-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e4fc-116">Requirement</span></span> | <span data-ttu-id="5e4fc-117">Wert</span><span class="sxs-lookup"><span data-stu-id="5e4fc-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e4fc-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e4fc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5e4fc-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e4fc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5e4fc-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e4fc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5e4fc-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e4fc-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5e4fc-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5e4fc-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e4fc-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e4fc-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e4fc-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e4fc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e4fc-125">**Sdbopendatabase**</span><span class="sxs-lookup"><span data-stu-id="5e4fc-125">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




