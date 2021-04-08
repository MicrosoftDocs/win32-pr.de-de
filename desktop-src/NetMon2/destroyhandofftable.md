---
description: Die Funktion "destroyhandofftable" zerstört eine mit "" von "" "" "" "mit" "" erstelltes Tabelle
ms.assetid: 01ae9899-4f7c-4706-a2ce-9f55b112351d
title: Destroyhandofftable-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyHandoffTable
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7afccfd1932c57b2a0d77dbb5467afc31726c6fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959648"
---
# <a name="destroyhandofftable-function"></a><span data-ttu-id="e42e1-103">Destroyhandofftable-Funktion</span><span class="sxs-lookup"><span data-stu-id="e42e1-103">DestroyHandoffTable function</span></span>

<span data-ttu-id="e42e1-104">Die Funktion " **destroyhandofftable** " zerstört **eine mit "" von "**" "" "" "mit" "" erstelltes Tabelle</span><span class="sxs-lookup"><span data-stu-id="e42e1-104">The **DestroyHandoffTable** function destroys a handoff table created with **CreateHandoffTable**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e42e1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e42e1-105">Syntax</span></span>


```C++
VOID WINAPI DestroyHandoffTable(
  _In_ LPHANDOFFTABLE hTable
);
```



## <a name="parameters"></a><span data-ttu-id="e42e1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e42e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e42e1-107">*htable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e42e1-107">*hTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e42e1-108">Handle für die zerstörte Übergabe-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e42e1-108">Handle to the destroyed handoff table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e42e1-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e42e1-109">Return value</span></span>

<span data-ttu-id="e42e1-110">Keine.</span><span class="sxs-lookup"><span data-stu-id="e42e1-110">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="e42e1-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e42e1-111">Requirements</span></span>



| <span data-ttu-id="e42e1-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e42e1-112">Requirement</span></span> | <span data-ttu-id="e42e1-113">Wert</span><span class="sxs-lookup"><span data-stu-id="e42e1-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e42e1-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e42e1-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e42e1-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e42e1-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e42e1-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e42e1-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e42e1-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e42e1-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e42e1-118">Header</span><span class="sxs-lookup"><span data-stu-id="e42e1-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e42e1-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e42e1-119"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e42e1-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e42e1-120">Library</span></span><br/>                  | <dl> <span data-ttu-id="e42e1-121"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e42e1-121"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e42e1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e42e1-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e42e1-123"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e42e1-123"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




