---
description: Die Clone-Methode erstellt ein neues-Objekt mit einem eigenen Such Zeiger, der auf die gleichen Bytes wie das ursprüngliche ibytebuffer-Objekt verweist.
ms.assetid: 41530f1d-81e5-4bea-a254-d7d741976904
title: 'Ibytebuffer:: Clone-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Clone
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d994ef55665b03da2a7d657689682f893fdf071f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217334"
---
# <a name="ibytebufferclone-method"></a><span data-ttu-id="c50fa-103">Ibytebuffer:: Clone-Methode</span><span class="sxs-lookup"><span data-stu-id="c50fa-103">IByteBuffer::Clone method</span></span>

<span data-ttu-id="c50fa-104">\[Die **Klon** Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c50fa-104">\[The **Clone** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c50fa-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c50fa-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c50fa-106">Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="c50fa-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="c50fa-107">Die **Clone** -Methode erstellt ein neues-Objekt mit einem eigenen Such Zeiger, der auf die gleichen Bytes wie das ursprüngliche [**ibytebuffer**](ibytebuffer.md) -Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="c50fa-107">The **Clone** method creates a new object with its own seek pointer that references the same bytes as the original [**IByteBuffer**](ibytebuffer.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c50fa-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c50fa-108">Syntax</span></span>


```C++
HRESULT Clone(
  [out] LPBYTEBUFFER *ppByteBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="c50fa-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c50fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c50fa-110">*ppbytebuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c50fa-110">*ppByteBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c50fa-111">Bei erfolgreicher Ausführung verweist auf den Speicherort eines [**ibytebuffer**](ibytebuffer.md) -Zeigers auf das neue Streamobjekt.</span><span class="sxs-lookup"><span data-stu-id="c50fa-111">When successful, points to the location of an [**IByteBuffer**](ibytebuffer.md) pointer to the new stream object.</span></span> <span data-ttu-id="c50fa-112">Wenn Sie den **ibytebuffer** -Zeiger nicht mehr verwenden, geben Sie ihn durch Aufrufen der [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) -Funktion frei.</span><span class="sxs-lookup"><span data-stu-id="c50fa-112">When you have finished using the **IByteBuffer** pointer, release it by calling the [**IUnknown::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) function.</span></span> <span data-ttu-id="c50fa-113">Wenn ein Fehler auftritt, ist dieser Parameter **null**.</span><span class="sxs-lookup"><span data-stu-id="c50fa-113">If an error occurs, this parameter is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c50fa-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c50fa-114">Return value</span></span>

<span data-ttu-id="c50fa-115">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c50fa-115">The return value is an **HRESULT**.</span></span> <span data-ttu-id="c50fa-116">Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="c50fa-116">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c50fa-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c50fa-117">Remarks</span></span>

<span data-ttu-id="c50fa-118">Diese Methode erstellt ein neues Streamobjekt für den Zugriff auf die gleichen bytes, jedoch mit einem separaten Such Zeiger.</span><span class="sxs-lookup"><span data-stu-id="c50fa-118">This method creates a new stream object for accessing the same bytes but using a separate seek pointer.</span></span> <span data-ttu-id="c50fa-119">Das neue Streamobjekt sieht die gleichen Daten wie das Quelldaten Strom Objekt.</span><span class="sxs-lookup"><span data-stu-id="c50fa-119">The new stream object sees the same data as the source stream object.</span></span> <span data-ttu-id="c50fa-120">Änderungen, die in ein-Objekt geschrieben werden, sind direkt in der anderen sichtbar.</span><span class="sxs-lookup"><span data-stu-id="c50fa-120">Changes written to one object are immediately visible in the other.</span></span> <span data-ttu-id="c50fa-121">Bereichs Sperren werden zwischen den Streamobjekten freigegeben.</span><span class="sxs-lookup"><span data-stu-id="c50fa-121">Range locking is shared between the stream objects.</span></span>

<span data-ttu-id="c50fa-122">Die anfängliche Einstellung des Such Zeigers in der geklonten Streaminstanz ist mit der aktuellen Einstellung des Such Zeigers im ursprünglichen Stream zum Zeitpunkt des Klon Vorgangs identisch.</span><span class="sxs-lookup"><span data-stu-id="c50fa-122">The initial setting of the seek pointer in the cloned stream instance is the same as the current setting of the seek pointer in the original stream at the time of the clone operation.</span></span>

## <a name="examples"></a><span data-ttu-id="c50fa-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c50fa-123">Examples</span></span>

<span data-ttu-id="c50fa-124">Das folgende Beispiel zeigt das Klonen der [**ibytebuffer**](ibytebuffer.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c50fa-124">The following example shows cloning the [**IByteBuffer**](ibytebuffer.md) interface.</span></span>


```C++
HRESULT  hr;

// Clone the buffer.
hr = pIByteBuff->Clone(&pIByteClone);
if (FAILED(hr))
  printf("Failed IByteBuffer::Clone\n");
```



## <a name="requirements"></a><span data-ttu-id="c50fa-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c50fa-125">Requirements</span></span>



| <span data-ttu-id="c50fa-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c50fa-126">Requirement</span></span> | <span data-ttu-id="c50fa-127">Wert</span><span class="sxs-lookup"><span data-stu-id="c50fa-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c50fa-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c50fa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c50fa-129">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c50fa-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c50fa-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c50fa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c50fa-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c50fa-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c50fa-132">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c50fa-132">End of client support</span></span><br/>    | <span data-ttu-id="c50fa-133">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c50fa-133">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="c50fa-134">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c50fa-134">End of server support</span></span><br/>    | <span data-ttu-id="c50fa-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c50fa-135">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="c50fa-136">Header</span><span class="sxs-lookup"><span data-stu-id="c50fa-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c50fa-137"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c50fa-137"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c50fa-138">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c50fa-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="c50fa-139"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c50fa-139"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c50fa-140">DLL</span><span class="sxs-lookup"><span data-stu-id="c50fa-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c50fa-141"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c50fa-141"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c50fa-142">IID</span><span class="sxs-lookup"><span data-stu-id="c50fa-142">IID</span></span><br/>                      | <span data-ttu-id="c50fa-143">IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.</span><span class="sxs-lookup"><span data-stu-id="c50fa-143">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

