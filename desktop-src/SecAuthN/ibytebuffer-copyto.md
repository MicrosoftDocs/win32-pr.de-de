---
description: Die CopyTo-Methode kopiert eine angegebene Anzahl von Bytes vom aktuellen Such Zeiger im-Objekt in den aktuellen Such Zeiger in einem anderen-Objekt.
ms.assetid: 2044965f-665f-4aa1-abc0-42f5278dd647
title: 'Ibytebuffer:: CopyTo-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.CopyTo
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 9f6b35a2cfa2de459bb5e7acfcb9853e83ae0a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217779"
---
# <a name="ibytebuffercopyto-method"></a><span data-ttu-id="7c3c9-103">Ibytebuffer:: CopyTo-Methode</span><span class="sxs-lookup"><span data-stu-id="7c3c9-103">IByteBuffer::CopyTo method</span></span>

<span data-ttu-id="7c3c9-104">\[Die **CopyTo** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-104">\[The **CopyTo** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7c3c9-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7c3c9-106">Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="7c3c9-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="7c3c9-107">Die **CopyTo** -Methode kopiert eine angegebene Anzahl von Bytes vom aktuellen Such Zeiger im-Objekt in den aktuellen Such Zeiger in einem anderen-Objekt.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-107">The **CopyTo** method copies a specified number of bytes from the current seek pointer in the object to the current seek pointer in another object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c3c9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c3c9-108">Syntax</span></span>


```C++
HRESULT CopyTo(
  [in]  LPBYTEBUFFER *pByteBuffer,
  [in]  LONG         cb,
  [out] LONG         *pcbRead,
  [out] LONG         *pcbWritten
);
```



## <a name="parameters"></a><span data-ttu-id="7c3c9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c3c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c3c9-110">*pbytebuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c3c9-110">*pByteBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c3c9-111">Verweist auf den Zielstream.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-111">Points to the destination stream.</span></span> <span data-ttu-id="7c3c9-112">Der Stream, auf den *pbytebuffer* zeigt, kann ein neuer Datenstrom oder ein Klon des Quelldaten Stroms sein.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-112">The stream pointed to by *pByteBuffer* can be a new stream or a clone of the source stream.</span></span>

</dd> <dt>

<span data-ttu-id="7c3c9-113">*CB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c3c9-113">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c3c9-114">Anzahl der Bytes, die aus dem Quelldaten Strom kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-114">Number of bytes to copy from the source stream.</span></span>

</dd> <dt>

<span data-ttu-id="7c3c9-115">*pcbread* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7c3c9-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c3c9-116">Ein Zeiger auf den Speicherort, an dem diese Methode die tatsächliche Anzahl von Bytes schreibt, die aus der Quelle gelesen wurden.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-116">Pointer to the location where this method writes the actual number of bytes read from the source.</span></span> <span data-ttu-id="7c3c9-117">Sie können diesen Zeiger auf **null** festlegen, um anzugeben, dass dieser Wert nicht von Interesse ist.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-117">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="7c3c9-118">In diesem Fall stellt diese Methode nicht die tatsächliche Anzahl der gelesenen Bytes bereit.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-118">In this case, this method does not provide the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="7c3c9-119">*pcbwritten* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7c3c9-119">*pcbWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c3c9-120">Ein Zeiger auf den Speicherort, an dem diese Methode die tatsächliche Anzahl von Bytes schreibt, die in das Ziel geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-120">Pointer to the location where this method writes the actual number of bytes written to the destination.</span></span> <span data-ttu-id="7c3c9-121">Sie können diesen Zeiger auf **null** festlegen, um anzugeben, dass dieser Wert nicht von Interesse ist.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-121">You can set this pointer to **NULL** to indicate that you are not interested in this value.</span></span> <span data-ttu-id="7c3c9-122">In diesem Fall stellt diese Methode nicht die tatsächliche Anzahl der geschriebenen Bytes bereit.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-122">In this case, this method does not provide the actual number of bytes written.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c3c9-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c3c9-123">Return value</span></span>

<span data-ttu-id="7c3c9-124">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-124">The return value is an **HRESULT**.</span></span> <span data-ttu-id="7c3c9-125">Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-125">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7c3c9-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c3c9-126">Remarks</span></span>

<span data-ttu-id="7c3c9-127">Diese Methode kopiert die angegebenen Bytes von einem Stream in einen anderen.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-127">This method copies the specified bytes from one stream to another.</span></span> <span data-ttu-id="7c3c9-128">Sie kann auch verwendet werden, um einen Datenstrom in sich selbst zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-128">It can also be used to copy a stream to itself.</span></span> <span data-ttu-id="7c3c9-129">Der Such Zeiger in jeder Stream-Instanz wird für die Anzahl der gelesenen oder geschriebenen Bytes angepasst.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-129">The seek pointer in each stream instance is adjusted for the number of bytes read or written.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c3c9-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c3c9-130">Requirements</span></span>



| <span data-ttu-id="7c3c9-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c3c9-131">Requirement</span></span> | <span data-ttu-id="7c3c9-132">Wert</span><span class="sxs-lookup"><span data-stu-id="7c3c9-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c3c9-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c3c9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7c3c9-134">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c3c9-134">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7c3c9-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c3c9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7c3c9-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c3c9-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7c3c9-137">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="7c3c9-137">End of client support</span></span><br/>    | <span data-ttu-id="7c3c9-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7c3c9-138">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7c3c9-139">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="7c3c9-139">End of server support</span></span><br/>    | <span data-ttu-id="7c3c9-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7c3c9-140">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7c3c9-141">Header</span><span class="sxs-lookup"><span data-stu-id="7c3c9-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c3c9-142"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7c3c9-142"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c3c9-143">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7c3c9-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="7c3c9-144"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7c3c9-144"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7c3c9-145">DLL</span><span class="sxs-lookup"><span data-stu-id="7c3c9-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c3c9-146"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c3c9-146"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7c3c9-147">IID</span><span class="sxs-lookup"><span data-stu-id="7c3c9-147">IID</span></span><br/>                      | <span data-ttu-id="7c3c9-148">IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.</span><span class="sxs-lookup"><span data-stu-id="7c3c9-148">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

