---
description: Ruft das Ergebnis einer asynchronen Aktion ab.
ms.assetid: E5AF357D-B1EE-4581-AEBC-6F1C89D7DBB0
title: 'Iasyncaction:: GetResults-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.GetResults
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 292c73846227f1bb8884b24b7e709bc6b2296e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214607"
---
# <a name="iasyncactiongetresults-method"></a><span data-ttu-id="45a12-103">Iasyncaction:: GetResults-Methode</span><span class="sxs-lookup"><span data-stu-id="45a12-103">IAsyncAction::GetResults method</span></span>

<span data-ttu-id="45a12-104">Ruft das Ergebnis einer asynchronen Aktion ab.</span><span class="sxs-lookup"><span data-stu-id="45a12-104">Gets the outcome of an asynchronous action.</span></span>

## <a name="syntax"></a><span data-ttu-id="45a12-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="45a12-105">Syntax</span></span>


```C++
HRESULT GetResults();
```



## <a name="parameters"></a><span data-ttu-id="45a12-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="45a12-106">Parameters</span></span>

<span data-ttu-id="45a12-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="45a12-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="45a12-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="45a12-108">Return value</span></span>

<span data-ttu-id="45a12-109">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="45a12-109">Type: **HRESULT**</span></span>

<span data-ttu-id="45a12-110">Diese Methode gibt immer **\_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="45a12-110">This method always returns **S\_OK**.</span></span>

## <a name="remarks"></a><span data-ttu-id="45a12-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45a12-111">Remarks</span></span>

<span data-ttu-id="45a12-112">Das Aufrufen der **GetResults** -Methode hat keine Auswirkungen, wenn die aktuelle Implementierung einen dynamischen [**iasyncaction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)-Typ aufweist.</span><span class="sxs-lookup"><span data-stu-id="45a12-112">Calling the **GetResults** method has no effect if the current implementation has a dynamic type of [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction).</span></span>

## <a name="requirements"></a><span data-ttu-id="45a12-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45a12-113">Requirements</span></span>



| <span data-ttu-id="45a12-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45a12-114">Requirement</span></span> | <span data-ttu-id="45a12-115">Wert</span><span class="sxs-lookup"><span data-stu-id="45a12-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45a12-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45a12-116">Minimum supported client</span></span><br/> | <span data-ttu-id="45a12-117">Windows 8</span><span class="sxs-lookup"><span data-stu-id="45a12-117">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="45a12-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45a12-118">Minimum supported server</span></span><br/> | <span data-ttu-id="45a12-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="45a12-119">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="45a12-120">Header</span><span class="sxs-lookup"><span data-stu-id="45a12-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="45a12-121"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="45a12-121"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45a12-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45a12-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45a12-123">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="45a12-123">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
