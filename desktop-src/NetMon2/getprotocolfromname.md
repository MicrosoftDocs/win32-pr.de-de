---
description: Die GetProtocolFromName-Funktion gibt ein Handle für ein Protokoll mit einem bestimmten Namen zurück.
ms.assetid: 18f5a9a7-4245-479d-a0da-2ede362a60b8
title: GetProtocolFromName-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolFromName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e104c066be2a5465083c7983aaefebd46f548b7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750073"
---
# <a name="getprotocolfromname-function"></a><span data-ttu-id="e811a-103">GetProtocolFromName-Funktion</span><span class="sxs-lookup"><span data-stu-id="e811a-103">GetProtocolFromName function</span></span>

<span data-ttu-id="e811a-104">Die **GetProtocolFromName** -Funktion gibt ein Handle für ein Protokoll mit einem bestimmten Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="e811a-104">The **GetProtocolFromName** function returns a handle to a protocol of a given name.</span></span>

## <a name="syntax"></a><span data-ttu-id="e811a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e811a-105">Syntax</span></span>


```C++
HPROTOCOL WINAPI GetProtocolFromName(
  _In_ LPSTR ProtocolName
);
```



## <a name="parameters"></a><span data-ttu-id="e811a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e811a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e811a-107">*ProtocolName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e811a-107">*ProtocolName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e811a-108">Der Protokoll Name (z. b. IP).</span><span class="sxs-lookup"><span data-stu-id="e811a-108">Protocol name (for example, IP).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e811a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e811a-109">Return value</span></span>

<span data-ttu-id="e811a-110">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Protokoll handle.</span><span class="sxs-lookup"><span data-stu-id="e811a-110">If the function is successful, the return value is a protocol handle.</span></span>

<span data-ttu-id="e811a-111">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="e811a-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e811a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e811a-112">Remarks</span></span>

<span data-ttu-id="e811a-113">[*Experten*](e.md) und [*Parser*](p.md) können die **GetProtocolFromName** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e811a-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolFromName** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e811a-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e811a-114">Requirements</span></span>



| <span data-ttu-id="e811a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e811a-115">Requirement</span></span> | <span data-ttu-id="e811a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e811a-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e811a-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e811a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e811a-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e811a-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e811a-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e811a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e811a-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e811a-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e811a-121">Header</span><span class="sxs-lookup"><span data-stu-id="e811a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e811a-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e811a-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e811a-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e811a-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="e811a-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e811a-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e811a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e811a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e811a-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e811a-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




