---
description: Die getprotocolstartoffsettthandle-Funktion gibt den Frame Offset eines bestimmten Protokolls zurück.
ms.assetid: b1e3a03b-f211-4c2c-8810-9e220c40136b
title: Getprotocolstarttfflthandle-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProtocolStartOffsetHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: bac8a10e2a0d8be667f1448c523f208c0c3e1512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344402"
---
# <a name="getprotocolstartoffsethandle-function"></a><span data-ttu-id="67093-103">Getprotocolstarthfflthandle-Funktion</span><span class="sxs-lookup"><span data-stu-id="67093-103">GetProtocolStartOffsetHandle function</span></span>

<span data-ttu-id="67093-104">Die **getprotocolstartoffsettthandle** -Funktion gibt den Frame Offset eines bestimmten Protokolls zurück.</span><span class="sxs-lookup"><span data-stu-id="67093-104">The **GetProtocolStartOffsetHandle** function returns the frame offset of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="67093-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="67093-105">Syntax</span></span>


```C++
DWORD WINAPI GetProtocolStartOffsetHandle(
  _In_ HFRAME    hFrame,
  _In_ HPROTOCOL hProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="67093-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="67093-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67093-107">*hframe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67093-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67093-108">Handle für einen Frame.</span><span class="sxs-lookup"><span data-stu-id="67093-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="67093-109">*hprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67093-109">*hProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67093-110">Handle für ein Protokoll.</span><span class="sxs-lookup"><span data-stu-id="67093-110">Handle to a protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67093-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67093-111">Return value</span></span>

<span data-ttu-id="67093-112">Wenn die Funktion erfolgreich ist, ist der Rückgabewert der Offset des Frames, gemessen in Bytes.</span><span class="sxs-lookup"><span data-stu-id="67093-112">If the function is successful, the return value is the offset of the frame   measured in bytes.</span></span>

<span data-ttu-id="67093-113">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert eins (1).</span><span class="sxs-lookup"><span data-stu-id="67093-113">If the function is unsuccessful, the return value is one (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="67093-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67093-114">Remarks</span></span>

<span data-ttu-id="67093-115">[*Experten*](e.md) und [*Parser*](p.md) können die **getprotocolstarto ffabthandle** -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="67093-115">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetProtocolStartOffsetHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="67093-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67093-116">Requirements</span></span>



| <span data-ttu-id="67093-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67093-117">Requirement</span></span> | <span data-ttu-id="67093-118">Wert</span><span class="sxs-lookup"><span data-stu-id="67093-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="67093-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67093-119">Minimum supported client</span></span><br/> | <span data-ttu-id="67093-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67093-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="67093-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67093-121">Minimum supported server</span></span><br/> | <span data-ttu-id="67093-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="67093-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="67093-123">Header</span><span class="sxs-lookup"><span data-stu-id="67093-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="67093-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="67093-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="67093-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="67093-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="67093-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67093-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="67093-127">DLL</span><span class="sxs-lookup"><span data-stu-id="67093-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67093-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67093-128"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




