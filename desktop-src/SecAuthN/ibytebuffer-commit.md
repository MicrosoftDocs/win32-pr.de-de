---
description: Die Commit-Methode stellt sicher, dass alle Änderungen, die an einem im transaktiven Modus geöffneten Objekt vorgenommen werden, im übergeordneten Speicher widergespiegelt werden.
ms.assetid: 00986e48-c5b9-4ac9-a204-a0774cb5e03e
title: 'Ibytebuffer:: Commit-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Commit
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 066925361d0ee4391bcd1eaafe33e0ae2d4b9120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356945"
---
# <a name="ibytebuffercommit-method"></a><span data-ttu-id="40ec6-103">Ibytebuffer:: Commit-Methode</span><span class="sxs-lookup"><span data-stu-id="40ec6-103">IByteBuffer::Commit method</span></span>

<span data-ttu-id="40ec6-104">\[Die **Commit** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="40ec6-104">\[The **Commit** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="40ec6-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="40ec6-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="40ec6-106">Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="40ec6-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="40ec6-107">Die **Commit** -Methode stellt sicher, dass alle Änderungen, die an einem im transaktiven Modus geöffneten Objekt vorgenommen werden, im übergeordneten Speicher widergespiegelt werden.</span><span class="sxs-lookup"><span data-stu-id="40ec6-107">The **Commit** method ensures that any changes made to an object open in transacted mode are reflected in the parent storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="40ec6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="40ec6-108">Syntax</span></span>


```C++
HRESULT Commit(
  [in] LONG grfCommitFlags
);
```



## <a name="parameters"></a><span data-ttu-id="40ec6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="40ec6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40ec6-110">*GRF commitflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40ec6-110">*grfCommitFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40ec6-111">Steuert, auf welche Weise ein Commit für die Änderungen am Streamobjekt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40ec6-111">Controls how the changes for the stream object are committed.</span></span> <span data-ttu-id="40ec6-112">Eine Definition dieser Werte finden Sie in der stgc-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="40ec6-112">For a definition of these values, see the STGC enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40ec6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40ec6-113">Return value</span></span>

<span data-ttu-id="40ec6-114">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="40ec6-114">The return value is an **HRESULT**.</span></span> <span data-ttu-id="40ec6-115">Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="40ec6-115">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="40ec6-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40ec6-116">Remarks</span></span>

<span data-ttu-id="40ec6-117">Diese Methode stellt sicher, dass Änderungen an einem im Transaktionsmodus geöffneten Datenstrom Objekt im übergeordneten Speicher widergespiegelt werden.</span><span class="sxs-lookup"><span data-stu-id="40ec6-117">This method ensures that changes to a stream object opened in transacted mode are reflected in the parent storage.</span></span> <span data-ttu-id="40ec6-118">Änderungen, die seit dem Öffnen oder letzten Commit an dem Stream vorgenommen wurden, werden in das übergeordnete Speicher Objekt übernommen.</span><span class="sxs-lookup"><span data-stu-id="40ec6-118">Changes that have been made to the stream since it was opened or last committed are reflected to the parent storage object.</span></span> <span data-ttu-id="40ec6-119">Wenn das übergeordnete Element im transaktiven Modus geöffnet wird, kann das übergeordnete Element immer noch zu einem späteren Zeitpunkt wieder hergestellt werden, um die Änderungen auf dieses Streamobjekt zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="40ec6-119">If the parent is opened in transacted mode, the parent may still revert at a later time rolling back the changes to this stream object.</span></span> <span data-ttu-id="40ec6-120">Die Implementierung von Verbund Dateien unterstützt das Öffnen von Datenströmen im transaktiven Modus nicht. Daher hat diese Methode nur wenig Auswirkungen als das Leeren von Speicher Puffern.</span><span class="sxs-lookup"><span data-stu-id="40ec6-120">The compound file implementation does not support opening streams in transacted mode, so this method has very little effect other than to flush memory buffers.</span></span>

## <a name="examples"></a><span data-ttu-id="40ec6-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40ec6-121">Examples</span></span>

<span data-ttu-id="40ec6-122">Im folgenden Beispiel wird das übernehmen von Änderungen am Speicher veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="40ec6-122">The following example shows committing changes to storage.</span></span>


```C++
HRESULT  hr;

// Commit the buffer.
hr = pIByteBuff->Commit(STGC_DEFAULT | STGC_CONSOLIDATE);
if (FAILED(hr))
  printf("Failed IByteBuffer::Commit\n");
```



## <a name="requirements"></a><span data-ttu-id="40ec6-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40ec6-123">Requirements</span></span>



| <span data-ttu-id="40ec6-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40ec6-124">Requirement</span></span> | <span data-ttu-id="40ec6-125">Wert</span><span class="sxs-lookup"><span data-stu-id="40ec6-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40ec6-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40ec6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="40ec6-127">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40ec6-127">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="40ec6-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40ec6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="40ec6-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="40ec6-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="40ec6-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="40ec6-130">End of client support</span></span><br/>    | <span data-ttu-id="40ec6-131">Windows XP</span><span class="sxs-lookup"><span data-stu-id="40ec6-131">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="40ec6-132">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="40ec6-132">End of server support</span></span><br/>    | <span data-ttu-id="40ec6-133">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="40ec6-133">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="40ec6-134">Header</span><span class="sxs-lookup"><span data-stu-id="40ec6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="40ec6-135"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="40ec6-135"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="40ec6-136">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="40ec6-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="40ec6-137"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="40ec6-137"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="40ec6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="40ec6-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40ec6-139"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40ec6-139"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="40ec6-140">IID</span><span class="sxs-lookup"><span data-stu-id="40ec6-140">IID</span></span><br/>                      | <span data-ttu-id="40ec6-141">IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.</span><span class="sxs-lookup"><span data-stu-id="40ec6-141">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

