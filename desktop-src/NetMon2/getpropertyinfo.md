---
description: Die GetPropertyInfo-Funktion gibt einen Zeiger auf die Eigenschafts Informationen eines bestimmten Protokolls zurück.
ms.assetid: f65166ba-1d94-4d65-b9d7-edb84ada0826
title: GetPropertyInfo-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 007332a85f170f865604526199681cad6d68cdcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862007"
---
# <a name="getpropertyinfo-function"></a><span data-ttu-id="df10c-103">GetPropertyInfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="df10c-103">GetPropertyInfo function</span></span>

<span data-ttu-id="df10c-104">Die **GetPropertyInfo** -Funktion gibt einen Zeiger auf die Eigenschafts Informationen eines bestimmten Protokolls zurück.</span><span class="sxs-lookup"><span data-stu-id="df10c-104">The **GetPropertyInfo** function returns a pointer to the property information of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="df10c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="df10c-105">Syntax</span></span>


```C++
LPPROPERTYINFO WINAPI GetPropertyInfo(
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a><span data-ttu-id="df10c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="df10c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df10c-107">*hproperty* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="df10c-107">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df10c-108">Handle für eine Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="df10c-108">Handle to a property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df10c-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df10c-109">Return value</span></span>

<span data-ttu-id="df10c-110">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="df10c-110">If the function is successful, the return value is a pointer to the property.</span></span>

<span data-ttu-id="df10c-111">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="df10c-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="df10c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df10c-112">Remarks</span></span>

<span data-ttu-id="df10c-113">[*Experten*](e.md) und [*Parser*](p.md) können die **GetPropertyInfo** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="df10c-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPropertyInfo** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="df10c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df10c-114">Requirements</span></span>



| <span data-ttu-id="df10c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df10c-115">Requirement</span></span> | <span data-ttu-id="df10c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="df10c-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="df10c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="df10c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="df10c-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df10c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="df10c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="df10c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="df10c-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="df10c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="df10c-121">Header</span><span class="sxs-lookup"><span data-stu-id="df10c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="df10c-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="df10c-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="df10c-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="df10c-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="df10c-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df10c-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="df10c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="df10c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df10c-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df10c-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




