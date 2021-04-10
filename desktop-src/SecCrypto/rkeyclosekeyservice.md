---
description: Die rkeyclosekeyservice-Funktion wird nicht unterstützt.
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: Rkeyclosekeyservice-Funktion (rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyCloseKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 3a35362876c067de011ec69a858e20150308cbd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862623"
---
# <a name="rkeyclosekeyservice-function"></a><span data-ttu-id="489fe-103">Rkeyclosekeyservice-Funktion</span><span class="sxs-lookup"><span data-stu-id="489fe-103">RKeyCloseKeyService function</span></span>

<span data-ttu-id="489fe-104">Die **rkeyclosekeyservice** -Funktion wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="489fe-104">The **RKeyCloseKeyService** function is not supported.</span></span>

<span data-ttu-id="489fe-105">**Windows Server 2003:** Die Funktion **rkeyclosekeyservice** schließt ein Schlüsseldienst handle, das durch einen vorherigen aufrufsbefehl der [**rkeyopenkeyservice**](rkeyopenkeyservice.md) -Funktion geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="489fe-105">**Windows Server 2003:** The **RKeyCloseKeyService** function closes a key service handle opened by a previous call to the [**RKeyOpenKeyService**](rkeyopenkeyservice.md) function.</span></span> <span data-ttu-id="489fe-106">Beachten Sie, dass sich dieses Verhalten in Windows Server 2003 mit Service Pack 1 (SP1) geändert hat.</span><span class="sxs-lookup"><span data-stu-id="489fe-106">Note that this behavior has changed with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="syntax"></a><span data-ttu-id="489fe-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="489fe-107">Syntax</span></span>


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a><span data-ttu-id="489fe-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="489fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="489fe-109">*hkeysvccli* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="489fe-109">*hKeySvcCli* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="489fe-110">Ein [**keysvcc \_ handle**](keysvcc-handle.md) -handle, das zuvor von [**rkeyopenkeyservice**](rkeyopenkeyservice.md)geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="489fe-110">A [**KEYSVCC\_HANDLE**](keysvcc-handle.md) handle previously opened by [**RKeyOpenKeyService**](rkeyopenkeyservice.md).</span></span> <span data-ttu-id="489fe-111">Dieser Wert darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="489fe-111">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="489fe-112">*beibehalten* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="489fe-112">*pReserved* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="489fe-113">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="489fe-113">Reserved.</span></span> <span data-ttu-id="489fe-114">Legen Sie diesen Wert auf **null** fest.</span><span class="sxs-lookup"><span data-stu-id="489fe-114">Set this value to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="489fe-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="489fe-115">Return value</span></span>

<span data-ttu-id="489fe-116">Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="489fe-116">If the function is successful, the return value is S\_OK.</span></span>

<span data-ttu-id="489fe-117">Wenn die Funktion fehlschlägt, ist der Rückgabewert ein **ulong** -Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="489fe-117">If the function fails, the return value is a **ULONG** that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="489fe-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="489fe-118">Requirements</span></span>



| <span data-ttu-id="489fe-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="489fe-119">Requirement</span></span> | <span data-ttu-id="489fe-120">Wert</span><span class="sxs-lookup"><span data-stu-id="489fe-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="489fe-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="489fe-121">Minimum supported client</span></span><br/> | <span data-ttu-id="489fe-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="489fe-122">None supported</span></span><br/>                                                             |
| <span data-ttu-id="489fe-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="489fe-123">Minimum supported server</span></span><br/> | <span data-ttu-id="489fe-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="489fe-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="489fe-125">Header</span><span class="sxs-lookup"><span data-stu-id="489fe-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="489fe-126"><dt>Rkeysvcc. h</dt></span><span class="sxs-lookup"><span data-stu-id="489fe-126"><dt>Rkeysvcc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="489fe-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="489fe-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="489fe-128">**Rkeyopenkeyservice**</span><span class="sxs-lookup"><span data-stu-id="489fe-128">**RKeyOpenKeyService**</span></span>](rkeyopenkeyservice.md)
</dt> <dt>

[<span data-ttu-id="489fe-129">**Rkeypfxinstall**</span><span class="sxs-lookup"><span data-stu-id="489fe-129">**RKeyPFXInstall**</span></span>](rkeypfxinstall.md)
</dt> </dl>

 

 




