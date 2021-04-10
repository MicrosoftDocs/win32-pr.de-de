---
description: Ruft die Methode auf, die aufgerufen wird, wenn die angegebene asynchrone Aktion abgeschlossen ist.
ms.assetid: 97199C1A-7CE3-4BBD-86A3-2CA9B27CC05E
title: 'Asyncactioncompletedhandler:: Aufrufen-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler.Invoke
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 1cba9c48fa955b82fdc337ba641acbd4c62f6406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129248"
---
# <a name="asyncactioncompletedhandlerinvoke-method"></a><span data-ttu-id="a7209-103">Asyncactioncompletedhandler:: Aufrufen-Methode</span><span class="sxs-lookup"><span data-stu-id="a7209-103">AsyncActionCompletedHandler::Invoke method</span></span>

<span data-ttu-id="a7209-104">Ruft die Methode auf, die aufgerufen wird, wenn die angegebene asynchrone Aktion abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a7209-104">Invokes the method that is called when the specified asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7209-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7209-105">Syntax</span></span>


```C++
HRESULT Invoke(
  [in] IAsyncAction *asyncInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a7209-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7209-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7209-107">*asyncinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a7209-107">*asyncInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7209-108">Typ: \**[**iasyncaction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) \** _</span><span class="sxs-lookup"><span data-stu-id="a7209-108">Type: \**[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)\** _</span></span>

<span data-ttu-id="a7209-109">Die asynchrone Aktion, die den Abschluss meldet.</span><span class="sxs-lookup"><span data-stu-id="a7209-109">The asynchronous action that reports completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7209-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7209-110">Return value</span></span>

<span data-ttu-id="a7209-111">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="a7209-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="a7209-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="a7209-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a7209-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a7209-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7209-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7209-114">Requirements</span></span>



| <span data-ttu-id="a7209-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7209-115">Requirement</span></span> | <span data-ttu-id="a7209-116">Wert</span><span class="sxs-lookup"><span data-stu-id="a7209-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7209-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7209-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a7209-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a7209-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="a7209-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7209-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a7209-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a7209-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="a7209-121">Header</span><span class="sxs-lookup"><span data-stu-id="a7209-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7209-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7209-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7209-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7209-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7209-124">**Asyncactioncompletedhandler**</span><span class="sxs-lookup"><span data-stu-id="a7209-124">**AsyncActionCompletedHandler**</span></span>](asyncactioncompletedhandler.md)
</dt> </dl>

 

