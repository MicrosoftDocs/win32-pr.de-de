---
description: 'Entfernt die Zugriffsbeschränkung für einen Bereich von Bytes, der zuvor mithilfe von ibytebuffer:: LockRegion eingeschränkt wurde.'
ms.assetid: f2a1162e-7fc7-4a55-befb-0b017edb9fe2
title: 'Ibytebuffer:: UnlockRegion-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.UnlockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92e49ba000177326ad14d3b83002613a15e96e18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960543"
---
# <a name="ibytebufferunlockregion-method"></a><span data-ttu-id="4572b-103">Ibytebuffer:: UnlockRegion-Methode</span><span class="sxs-lookup"><span data-stu-id="4572b-103">IByteBuffer::UnlockRegion method</span></span>

<span data-ttu-id="4572b-104">\[Die **UnlockRegion** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="4572b-104">\[The **UnlockRegion** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4572b-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4572b-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4572b-106">Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="4572b-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="4572b-107">Die **UnlockRegion** -Methode entfernt die Zugriffsbeschränkung für einen Bereich von Bytes, der zuvor mithilfe von [**ibytebuffer:: LockRegion**](ibytebuffer-lockregion.md)eingeschränkt wurde.</span><span class="sxs-lookup"><span data-stu-id="4572b-107">The **UnlockRegion** method removes the access restriction on a range of bytes previously restricted by using [**IByteBuffer::LockRegion**](ibytebuffer-lockregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4572b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4572b-108">Syntax</span></span>


```C++
HRESULT UnlockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a><span data-ttu-id="4572b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4572b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4572b-110">*liboffset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4572b-110">*libOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4572b-111">Der Byte Offset für den Anfang des Bereichs.</span><span class="sxs-lookup"><span data-stu-id="4572b-111">Byte offset for the beginning of the range.</span></span>

</dd> <dt>

<span data-ttu-id="4572b-112">*CB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4572b-112">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4572b-113">Länge (in Byte) des Bereichs, der eingeschränkt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4572b-113">Length, in bytes, of the range to be restricted.</span></span>

</dd> <dt>

<span data-ttu-id="4572b-114">*dwLockType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4572b-114">*dwLockType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4572b-115">Zugriffs Einschränkungen, die zuvor auf den Bereich gesetzt wurden.</span><span class="sxs-lookup"><span data-stu-id="4572b-115">Access restrictions previously placed on the range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4572b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4572b-116">Return value</span></span>

<span data-ttu-id="4572b-117">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4572b-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="4572b-118">Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="4572b-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4572b-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4572b-119">Remarks</span></span>

<span data-ttu-id="4572b-120">Die **ibytebuffer:: UnlockRegion** -Methode entsperrt einen zuvor gesperrten Bereich mithilfe der [**ibytebuffer:: LockRegion**](ibytebuffer-lockregion.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="4572b-120">The **IByteBuffer::UnlockRegion** method unlocks a region previously locked by using the [**IByteBuffer::LockRegion**](ibytebuffer-lockregion.md) method.</span></span> <span data-ttu-id="4572b-121">Gesperrte Bereiche müssen später explizit entsperrt werden, indem **ibytebuffer:: UnlockRegion** mit exakt denselben Werten für die Parameter *liboffset*, *CB* und *dwLockType* aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4572b-121">Locked regions must later be explicitly unlocked by calling **IByteBuffer::UnlockRegion** with exactly the same values for the *libOffset*, *cb*, and *dwLockType* parameters.</span></span> <span data-ttu-id="4572b-122">Die Region muss entsperrt werden, bevor der Stream freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4572b-122">The region must be unlocked before the stream is released.</span></span> <span data-ttu-id="4572b-123">Zwei angrenzende Regionen können nicht separat gesperrt und dann mit einem einzigen Unlock-Befehl entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="4572b-123">Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.</span></span>

## <a name="examples"></a><span data-ttu-id="4572b-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4572b-124">Examples</span></span>

<span data-ttu-id="4572b-125">Im folgenden Beispiel wird gezeigt, wie ein Bereich von Bytes entsperrt wird.</span><span class="sxs-lookup"><span data-stu-id="4572b-125">The following example shows unlocking a range of bytes.</span></span>


```C++
HRESULT  hr;

// Unlock a region.
hr = pIByteBuff->UnlockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::UnlockRegion\n");
```



## <a name="requirements"></a><span data-ttu-id="4572b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4572b-126">Requirements</span></span>



| <span data-ttu-id="4572b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4572b-127">Requirement</span></span> | <span data-ttu-id="4572b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="4572b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4572b-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4572b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4572b-130">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4572b-130">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4572b-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4572b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4572b-132">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4572b-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4572b-133">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="4572b-133">End of client support</span></span><br/>    | <span data-ttu-id="4572b-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4572b-134">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4572b-135">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="4572b-135">End of server support</span></span><br/>    | <span data-ttu-id="4572b-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4572b-136">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4572b-137">Header</span><span class="sxs-lookup"><span data-stu-id="4572b-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="4572b-138"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="4572b-138"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4572b-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="4572b-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="4572b-140"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4572b-140"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4572b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="4572b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4572b-142"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4572b-142"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4572b-143">IID</span><span class="sxs-lookup"><span data-stu-id="4572b-143">IID</span></span><br/>                      | <span data-ttu-id="4572b-144">IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.</span><span class="sxs-lookup"><span data-stu-id="4572b-144">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

