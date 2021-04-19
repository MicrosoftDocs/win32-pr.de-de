---
description: Bestimmt, ob ein Freigabe Name die richtige Syntax verwendet.
ms.assetid: 4ffcff5d-0db5-4761-a31a-acefd2b8d9e2
title: Nddeisvalidsharename-Funktion (nddeapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeIsValidShareName
- NDdeIsValidShareNameA
- NDdeIsValidShareNameW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: cbe1b7ead2d6f8e2d315833c44b354c50cc8b62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346268"
---
# <a name="nddeisvalidsharename-function"></a><span data-ttu-id="3436f-103">Nddeisvalidsharename-Funktion</span><span class="sxs-lookup"><span data-stu-id="3436f-103">NDdeIsValidShareName function</span></span>

<span data-ttu-id="3436f-104">\[Network DDE wird nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3436f-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="3436f-105">Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]</span><span class="sxs-lookup"><span data-stu-id="3436f-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="3436f-106">Bestimmt, ob ein Freigabe Name die richtige Syntax verwendet.</span><span class="sxs-lookup"><span data-stu-id="3436f-106">Determines whether a share name uses the proper syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="3436f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3436f-107">Syntax</span></span>


```C++
BOOL NDdeIsValidShareName(
  _In_ LPTSTR shareName
);
```



## <a name="parameters"></a><span data-ttu-id="3436f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3436f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3436f-109">*ShareName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3436f-109">*shareName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3436f-110">Der Freigabe Name, der überprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="3436f-110">The share name to be validated.</span></span> <span data-ttu-id="3436f-111">Dieser Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="3436f-111">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3436f-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3436f-112">Return value</span></span>

<span data-ttu-id="3436f-113">Wenn der Freigabe Name eine gültige Syntax aufweist, ist der Rückgabewert ungleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="3436f-113">If the share name has valid syntax, the return value is nonzero.</span></span>

<span data-ttu-id="3436f-114">Wenn der Freigabe Name nicht über eine gültige Syntax verfügt, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="3436f-114">If the share name does not have valid syntax, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3436f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3436f-115">Remarks</span></span>

<span data-ttu-id="3436f-116">Diese Funktion wird auch von [**ndabshareadd**](nddeshareadd.md) aufgerufen, wenn Sie die DDE-Freigabe erstellt.</span><span class="sxs-lookup"><span data-stu-id="3436f-116">This function is also called by [**NDdeShareAdd**](nddeshareadd.md) when it creates the DDE share.</span></span>

## <a name="requirements"></a><span data-ttu-id="3436f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3436f-117">Requirements</span></span>



| <span data-ttu-id="3436f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3436f-118">Requirement</span></span> | <span data-ttu-id="3436f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3436f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3436f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3436f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3436f-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3436f-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3436f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3436f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3436f-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3436f-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3436f-124">Header</span><span class="sxs-lookup"><span data-stu-id="3436f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3436f-125"><dt>Ndde API. h</dt></span><span class="sxs-lookup"><span data-stu-id="3436f-125"><dt>Nddeapi.h</dt></span></span> </dl>   |
| <span data-ttu-id="3436f-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3436f-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="3436f-127"><dt>Ndde API. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3436f-127"><dt>Nddeapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="3436f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3436f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3436f-129"><dt>Nddeapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3436f-129"><dt>Nddeapi.dll</dt></span></span> </dl> |
| <span data-ttu-id="3436f-130">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="3436f-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3436f-131">**Nddeisvalidsharenamew** (Unicode) und **nddeisvalidsharenamea** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3436f-131">**NDdeIsValidShareNameW** (Unicode) and **NDdeIsValidShareNameA** (ANSI)</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="3436f-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3436f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3436f-133">Übersicht über das Netzwerk dynamischer Datenaustausch</span><span class="sxs-lookup"><span data-stu-id="3436f-133">Network Dynamic Data Exchange Overview</span></span>](network-dynamic-data-exchange.md)
</dt> <dt>

[<span data-ttu-id="3436f-134">Network DDE-Funktionen</span><span class="sxs-lookup"><span data-stu-id="3436f-134">Network DDE Functions</span></span>](network-dde-functions.md)
</dt> <dt>

[<span data-ttu-id="3436f-135">**Ndabshareadd**</span><span class="sxs-lookup"><span data-stu-id="3436f-135">**NDdeShareAdd**</span></span>](nddeshareadd.md)
</dt> </dl>

 

 




