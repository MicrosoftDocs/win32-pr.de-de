---
description: 'Die Revert-Methode verwirft alle Änderungen, die seit dem letzten ibytebuffer:: Commit-Befehl an einem transaktiven Datenstrom vorgenommen wurden.'
ms.assetid: da3d9810-6511-43d5-af87-03a392f8be75
title: 'Ibytebuffer:: Revert-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Revert
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: cf7873407196c98868ca45c73db503568f8259e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214530"
---
# <a name="ibytebufferrevert-method"></a><span data-ttu-id="32373-103">Ibytebuffer:: Revert-Methode</span><span class="sxs-lookup"><span data-stu-id="32373-103">IByteBuffer::Revert method</span></span>

<span data-ttu-id="32373-104">\[Die **Revert** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="32373-104">\[The **Revert** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="32373-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="32373-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="32373-106">Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="32373-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="32373-107">Die **Revert** -Methode verwirft alle Änderungen, die seit dem letzten [**ibytebuffer:: Commit**](ibytebuffer-commit.md) -Befehl an einem transaktiven Datenstrom vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="32373-107">The **Revert** method discards all changes that have been made to a transacted stream since the last [**IByteBuffer::Commit**](ibytebuffer-commit.md) call.</span></span>

## <a name="syntax"></a><span data-ttu-id="32373-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="32373-108">Syntax</span></span>


```C++
HRESULT Revert();
```



## <a name="parameters"></a><span data-ttu-id="32373-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="32373-109">Parameters</span></span>

<span data-ttu-id="32373-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="32373-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32373-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="32373-111">Return value</span></span>

<span data-ttu-id="32373-112">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="32373-112">The return value is an **HRESULT**.</span></span> <span data-ttu-id="32373-113">Der Wert S \_ OK gibt an, dass der-Rückruf erfolgreich war und der Stream auf seine vorherige Version zurückgesetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="32373-113">A value of S\_OK indicates the call was successful and the stream was reverted to its previous version.</span></span>

## <a name="remarks"></a><span data-ttu-id="32373-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="32373-114">Remarks</span></span>

<span data-ttu-id="32373-115">Diese Methode verwirft Änderungen, die seit dem letzten Commitvorgang an einem transaktiven Datenstrom vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="32373-115">This method discards changes made to a transacted stream since the last commit operation.</span></span>

## <a name="examples"></a><span data-ttu-id="32373-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32373-116">Examples</span></span>

<span data-ttu-id="32373-117">Das folgende Beispiel zeigt das Zurücksetzen eines transaktiven Streams auf den Vorgang mit dem letzten Commit.</span><span class="sxs-lookup"><span data-stu-id="32373-117">The following example shows reverting a transacted stream to the last-committed operation.</span></span>


```C++
HRESULT  hr;

hr = pIByteBuff->Revert();
if (FAILED(hr))
  printf("Failed IByteBuffer::Revert\n");
```



## <a name="requirements"></a><span data-ttu-id="32373-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32373-118">Requirements</span></span>



| <span data-ttu-id="32373-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32373-119">Requirement</span></span> | <span data-ttu-id="32373-120">Wert</span><span class="sxs-lookup"><span data-stu-id="32373-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32373-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32373-121">Minimum supported client</span></span><br/> | <span data-ttu-id="32373-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32373-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="32373-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32373-123">Minimum supported server</span></span><br/> | <span data-ttu-id="32373-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="32373-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="32373-125">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="32373-125">End of client support</span></span><br/>    | <span data-ttu-id="32373-126">Windows XP</span><span class="sxs-lookup"><span data-stu-id="32373-126">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="32373-127">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="32373-127">End of server support</span></span><br/>    | <span data-ttu-id="32373-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="32373-128">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="32373-129">Header</span><span class="sxs-lookup"><span data-stu-id="32373-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="32373-130"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="32373-130"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="32373-131">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="32373-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="32373-132"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="32373-132"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="32373-133">DLL</span><span class="sxs-lookup"><span data-stu-id="32373-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32373-134"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32373-134"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="32373-135">IID</span><span class="sxs-lookup"><span data-stu-id="32373-135">IID</span></span><br/>                      | <span data-ttu-id="32373-136">IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.</span><span class="sxs-lookup"><span data-stu-id="32373-136">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

