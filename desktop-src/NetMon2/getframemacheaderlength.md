---
description: Die getframemacheaderlength-Funktion gibt die Länge des Mac-Headers des Frames in Byte zurück.
ms.assetid: 4a0f6a8c-04e0-47cb-abd1-b4011cd2d062
title: Getframemacheaderlength-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacHeaderLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4d11a0efac2086884e984edae986720ef704cf81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343644"
---
# <a name="getframemacheaderlength-function"></a><span data-ttu-id="32f5f-103">Getframemacheaderlength-Funktion</span><span class="sxs-lookup"><span data-stu-id="32f5f-103">GetFrameMacHeaderLength function</span></span>

<span data-ttu-id="32f5f-104">Die **getframemacheaderlength** -Funktion gibt die Länge des Mac-Headers des Frames in Byte zurück.</span><span class="sxs-lookup"><span data-stu-id="32f5f-104">The **GetFrameMacHeaderLength** function returns the length, in bytes, of the MAC header of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="32f5f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="32f5f-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameMacHeaderLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="32f5f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="32f5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32f5f-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32f5f-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32f5f-108">Handle für den Frame.</span><span class="sxs-lookup"><span data-stu-id="32f5f-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32f5f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32f5f-109">Return value</span></span>

<span data-ttu-id="32f5f-110">Wenn die Funktion erfolgreich ist, ist der Rückgabewert die Länge in Bytes des Mac-Headers.</span><span class="sxs-lookup"><span data-stu-id="32f5f-110">If the function is successful, the return value is the length   in bytes   of the MAC header.</span></span>

<span data-ttu-id="32f5f-111">Wenn die Funktion nicht erfolgreich ist oder ein unbekannter Mac-Typ gefunden wird, ist der Rückgabewert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="32f5f-111">If the function is not successful, or an unknown MAC type is encountered, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="32f5f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32f5f-112">Remarks</span></span>

<span data-ttu-id="32f5f-113">[*Experten*](e.md) und [*Parser*](p.md) können die **getframemacheaderlength** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="32f5f-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameMacHeaderLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="32f5f-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32f5f-114">Requirements</span></span>



| <span data-ttu-id="32f5f-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32f5f-115">Requirement</span></span> | <span data-ttu-id="32f5f-116">Wert</span><span class="sxs-lookup"><span data-stu-id="32f5f-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="32f5f-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32f5f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="32f5f-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32f5f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="32f5f-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32f5f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="32f5f-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32f5f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="32f5f-121">Header</span><span class="sxs-lookup"><span data-stu-id="32f5f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="32f5f-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="32f5f-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="32f5f-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="32f5f-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="32f5f-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32f5f-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="32f5f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="32f5f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32f5f-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32f5f-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




