---
description: Die SetSize-Methode ändert die Größe des Datenstrom Objekts.
ms.assetid: e4027a98-fce4-4db4-a9fe-e7e7436b5147
title: 'Ibytebuffer:: SetSize-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.SetSize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 85a6abc11f3e007f3c8d1057cb5c8785c8519ebf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960544"
---
# <a name="ibytebuffersetsize-method"></a><span data-ttu-id="1e115-103">Ibytebuffer:: SetSize-Methode</span><span class="sxs-lookup"><span data-stu-id="1e115-103">IByteBuffer::SetSize method</span></span>

<span data-ttu-id="1e115-104">\[Die **SetSize** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="1e115-104">\[The **SetSize** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1e115-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1e115-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1e115-106">Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="1e115-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="1e115-107">Die **SetSize** -Methode ändert die Größe des Datenstrom Objekts.</span><span class="sxs-lookup"><span data-stu-id="1e115-107">The **SetSize** method changes the size of the stream object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e115-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e115-108">Syntax</span></span>


```C++
HRESULT SetSize(
  [in] LONG libNewSize
);
```



## <a name="parameters"></a><span data-ttu-id="1e115-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1e115-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e115-110">*libnewsize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1e115-110">*libNewSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e115-111">Neue Größe des Streams als Anzahl von Bytes</span><span class="sxs-lookup"><span data-stu-id="1e115-111">New size of the stream as a number of bytes</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e115-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1e115-112">Return value</span></span>

<span data-ttu-id="1e115-113">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1e115-113">The return value is an **HRESULT**.</span></span> <span data-ttu-id="1e115-114">Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="1e115-114">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e115-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e115-115">Remarks</span></span>

<span data-ttu-id="1e115-116">Die **ibytebuffer:: SetSize** -Methode ändert die Größe des Datenstrom Objekts.</span><span class="sxs-lookup"><span data-stu-id="1e115-116">The **IByteBuffer::SetSize** method changes the size of the stream object.</span></span> <span data-ttu-id="1e115-117">Rufen Sie diese Methode auf, um Speicherplatz für den Stream vorab zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="1e115-117">Call this method to preallocate space for the stream.</span></span> <span data-ttu-id="1e115-118">Wenn der *libnewsize* -Parameter größer als die aktuelle Streamgröße ist, wird der Datenstrom auf die für die Größe definierte Größe erweitert, indem der dazwischen liegende Bereich mit Bytes von undefiniertem Wert aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="1e115-118">If the *libNewSize* parameter is larger than the current stream size, the stream is extended to the indicated size by filling the intervening space with bytes of undefined value.</span></span> <span data-ttu-id="1e115-119">Dieser Vorgang ähnelt der [**ibytebuffer:: Write**](ibytebuffer-write.md) -Methode, wenn sich der Suchzeiger hinter dem aktuellen Streamende befindet.</span><span class="sxs-lookup"><span data-stu-id="1e115-119">This operation is similar to the [**IByteBuffer::Write**](ibytebuffer-write.md) method if the seek pointer is past the current end-of-stream.</span></span>

<span data-ttu-id="1e115-120">Wenn der *libnewsize* -Parameter kleiner als der aktuelle Stream ist, wird der Stream auf die markierte Größe gekürzt.</span><span class="sxs-lookup"><span data-stu-id="1e115-120">If the *libNewSize* parameter is smaller than the current stream, then the stream is truncated to the indicated size.</span></span>

<span data-ttu-id="1e115-121">Der Such Zeiger ist von der Änderung der Streamgröße nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="1e115-121">The seek pointer is not affected by the change in stream size.</span></span>

<span data-ttu-id="1e115-122">Der Aufruf von **ibytebuffer:: SetSize** kann eine effektive Methode sein, um einen großen Anteil von zusammenhängenden Speicherplatz zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1e115-122">Calling **IByteBuffer::SetSize** can be an effective way of trying to obtain a large chunk of contiguous space.</span></span>

## <a name="examples"></a><span data-ttu-id="1e115-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1e115-123">Examples</span></span>

<span data-ttu-id="1e115-124">Im folgenden Beispiel wird gezeigt, wie die Puffergröße festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="1e115-124">The following example shows setting the buffer size.</span></span>


```C++
LONG     lNewSize = 256;
HRESULT  hr;

// Change the buffer size.
hr = pIByteBuff->SetSize(lNewSize);
if (FAILED(hr))
  printf("Failed IByteBuffer::SetSize\n");
```



## <a name="requirements"></a><span data-ttu-id="1e115-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1e115-125">Requirements</span></span>



| <span data-ttu-id="1e115-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1e115-126">Requirement</span></span> | <span data-ttu-id="1e115-127">Wert</span><span class="sxs-lookup"><span data-stu-id="1e115-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e115-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1e115-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1e115-129">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e115-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1e115-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1e115-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1e115-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1e115-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1e115-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="1e115-132">End of client support</span></span><br/>    | <span data-ttu-id="1e115-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1e115-133">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="1e115-134">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="1e115-134">End of server support</span></span><br/>    | <span data-ttu-id="1e115-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1e115-135">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="1e115-136">Header</span><span class="sxs-lookup"><span data-stu-id="1e115-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e115-137"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="1e115-137"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1e115-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1e115-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="1e115-139"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1e115-139"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1e115-140">DLL</span><span class="sxs-lookup"><span data-stu-id="1e115-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e115-141"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e115-141"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1e115-142">IID</span><span class="sxs-lookup"><span data-stu-id="1e115-142">IID</span></span><br/>                      | <span data-ttu-id="1e115-143">IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.</span><span class="sxs-lookup"><span data-stu-id="1e115-143">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

