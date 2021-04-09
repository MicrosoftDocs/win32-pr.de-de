---
description: Die getprotocolinfo-Funktion gibt einen Zeiger auf einen Protokoll Informationswert zurück.
ms.assetid: 1ba47889-b2ed-47ba-94f9-1b781af6d01f
title: Getprotocolinfo-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2ec9fb58957c2e0fd64bc1c5878892fe6542af8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958708"
---
# <a name="getprotocolinfo-function"></a><span data-ttu-id="30b96-103">Getprotocolinfo-Funktion</span><span class="sxs-lookup"><span data-stu-id="30b96-103">GetProtocolInfo function</span></span>

<span data-ttu-id="30b96-104">Die **getprotocolinfo** -Funktion gibt einen Zeiger auf einen Protokoll Informationswert zurück.</span><span class="sxs-lookup"><span data-stu-id="30b96-104">The **GetProtocolInfo** function returns a pointer to a protocol information value.</span></span>

## <a name="syntax"></a><span data-ttu-id="30b96-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="30b96-105">Syntax</span></span>


```C++
LPPROTOCOLINFO WINAPI GetProtocolInfo(
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="30b96-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="30b96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30b96-107">*hprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30b96-107">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30b96-108">Handle für ein Protokoll.</span><span class="sxs-lookup"><span data-stu-id="30b96-108">Handle to a protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30b96-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30b96-109">Return value</span></span>

<span data-ttu-id="30b96-110">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ein Zeiger auf den Wert der Protokollinformationen.</span><span class="sxs-lookup"><span data-stu-id="30b96-110">If the function is successful, the return value is a pointer to the protocol information value.</span></span>

<span data-ttu-id="30b96-111">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="30b96-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="30b96-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30b96-112">Remarks</span></span>

<span data-ttu-id="30b96-113">[*Experten*](e.md) und [*Parser*](p.md) können die **getprotocolinfo** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="30b96-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolInfo** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="30b96-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30b96-114">Requirements</span></span>



| <span data-ttu-id="30b96-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30b96-115">Requirement</span></span> | <span data-ttu-id="30b96-116">Wert</span><span class="sxs-lookup"><span data-stu-id="30b96-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="30b96-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30b96-117">Minimum supported client</span></span><br/> | <span data-ttu-id="30b96-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30b96-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="30b96-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30b96-119">Minimum supported server</span></span><br/> | <span data-ttu-id="30b96-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30b96-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="30b96-121">Header</span><span class="sxs-lookup"><span data-stu-id="30b96-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="30b96-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="30b96-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="30b96-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30b96-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="30b96-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30b96-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="30b96-125">DLL</span><span class="sxs-lookup"><span data-stu-id="30b96-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30b96-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30b96-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




