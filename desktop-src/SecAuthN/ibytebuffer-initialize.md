---
description: Mit der Initialize-Methode wird das ibytebuffer-Objekt für die Verwendung vorbereitet. Diese Methode muss aufgerufen werden, bevor andere Methoden in der ibytebuffer-Schnittstelle aufgerufen werden.
ms.assetid: 1b22e693-0add-4b80-a2c4-925ebd3ab3a6
title: 'Ibytebuffer:: Initialize-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Initialize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 245f9282174ddeef66b130597f0f20ddf21ededc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364185"
---
# <a name="ibytebufferinitialize-method"></a><span data-ttu-id="2c8fb-104">Ibytebuffer:: Initialize-Methode</span><span class="sxs-lookup"><span data-stu-id="2c8fb-104">IByteBuffer::Initialize method</span></span>

<span data-ttu-id="2c8fb-105">\[Die **Initialize** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-105">\[The **Initialize** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2c8fb-106">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later.</span></span> <span data-ttu-id="2c8fb-107">Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="2c8fb-107">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="2c8fb-108">Mit der **Initialize** -Methode wird das [**ibytebuffer**](ibytebuffer.md) -Objekt für die Verwendung vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-108">The **Initialize** method prepares the [**IByteBuffer**](ibytebuffer.md) object for use.</span></span> <span data-ttu-id="2c8fb-109">Diese Methode muss aufgerufen werden, bevor andere Methoden in der **ibytebuffer** -Schnittstelle aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-109">This method must be called prior to calling any other methods in the **IByteBuffer** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c8fb-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c8fb-110">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] LONG lSize,
  [in] BYTE *pData
);
```



## <a name="parameters"></a><span data-ttu-id="2c8fb-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c8fb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c8fb-112">*LSIZE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c8fb-112">*lSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c8fb-113">Anfängliche Größe (in Bytes) der Daten, die der Stream enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-113">Initial size, in bytes, of the data the stream is to contain.</span></span>

</dd> <dt>

<span data-ttu-id="2c8fb-114">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2c8fb-114">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c8fb-115">Wenn nicht **null**, werden die anfänglichen Daten in den Stream geschrieben.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-115">If not **NULL**, the initial data to write to the stream.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c8fb-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2c8fb-116">Return value</span></span>

<span data-ttu-id="2c8fb-117">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="2c8fb-118">Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-118">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c8fb-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2c8fb-119">Remarks</span></span>

<span data-ttu-id="2c8fb-120">Wenn Sie einen neuen [**ibytebuffer**](ibytebuffer.md) -Stream verwenden, wird diese Methode aufgerufen, bevor eine der anderen **ibytebuffer** -Methoden verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-120">When using a new [**IByteBuffer**](ibytebuffer.md) stream, call this method prior to using any of the other **IByteBuffer** methods.</span></span>

## <a name="examples"></a><span data-ttu-id="2c8fb-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c8fb-121">Examples</span></span>

<span data-ttu-id="2c8fb-122">Das folgende Beispiel zeigt die Initialisierung des [**ibytebuffer**](ibytebuffer.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-122">The following example shows initializing the [**IByteBuffer**](ibytebuffer.md) object.</span></span>


```C++
UCHAR    ucFileName[] = {0x3f, 0x00};    // Master File (MF)
HRESULT  hr;

// pIByteRequest is a pointer to an instantiated IByteBuffer object.
hr = pIByteRequest->Initialize(2, ucFileName);
if (FAILED(hr))
    printf("Failed IByteBuffer::Initialize\n");
```



## <a name="requirements"></a><span data-ttu-id="2c8fb-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2c8fb-123">Requirements</span></span>



| <span data-ttu-id="2c8fb-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2c8fb-124">Requirement</span></span> | <span data-ttu-id="2c8fb-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2c8fb-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c8fb-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2c8fb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2c8fb-127">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c8fb-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2c8fb-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2c8fb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2c8fb-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2c8fb-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2c8fb-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="2c8fb-130">End of client support</span></span><br/>    | <span data-ttu-id="2c8fb-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2c8fb-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="2c8fb-132">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="2c8fb-132">End of server support</span></span><br/>    | <span data-ttu-id="2c8fb-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2c8fb-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="2c8fb-134">Header</span><span class="sxs-lookup"><span data-stu-id="2c8fb-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c8fb-135"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="2c8fb-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c8fb-136">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="2c8fb-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c8fb-137"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="2c8fb-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="2c8fb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="2c8fb-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c8fb-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c8fb-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2c8fb-140">IID</span><span class="sxs-lookup"><span data-stu-id="2c8fb-140">IID</span></span><br/>                      | <span data-ttu-id="2c8fb-141">IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.</span><span class="sxs-lookup"><span data-stu-id="2c8fb-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

