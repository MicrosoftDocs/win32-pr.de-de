---
description: Legt die Methode fest, die aufgerufen wird, wenn die asynchrone Aktion abgeschlossen ist.
ms.assetid: 632800E4-D02B-4D45-8A9B-B373AC938558
title: Iasyncaction::p ut_Completed-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.put_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: ec26401aeeed61445b0f244880864366fd5c6118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958937"
---
# <a name="iasyncactionput_completed-method"></a><span data-ttu-id="f6a86-103">Iasyncaction: Abgeschlossene:p UT- \_ Methode</span><span class="sxs-lookup"><span data-stu-id="f6a86-103">IAsyncAction::put\_Completed method</span></span>

<span data-ttu-id="f6a86-104">Legt die Methode fest, die aufgerufen wird, wenn die asynchrone Aktion abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="f6a86-104">Sets the method that is called when the asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6a86-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6a86-105">Syntax</span></span>


```C++
HRESULT put_Completed(
  [out] AsyncActionCompletedHandler *handler
);
```



## <a name="parameters"></a><span data-ttu-id="f6a86-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6a86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6a86-107">*Handler* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f6a86-107">*handler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6a86-108">Geben Sie Folgendes ein: \**[**asyncactioncompletedhandler**](asyncactioncompletedhandler.md) \** _</span><span class="sxs-lookup"><span data-stu-id="f6a86-108">Type: \**[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\** _</span></span>

<span data-ttu-id="f6a86-109">Die Methode, die die Abschluss Benachrichtigung behandelt.</span><span class="sxs-lookup"><span data-stu-id="f6a86-109">The method that handles the completion notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6a86-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f6a86-110">Return value</span></span>

<span data-ttu-id="f6a86-111">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f6a86-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f6a86-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="f6a86-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f6a86-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f6a86-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6a86-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f6a86-114">Requirements</span></span>



| <span data-ttu-id="f6a86-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f6a86-115">Requirement</span></span> | <span data-ttu-id="f6a86-116">Wert</span><span class="sxs-lookup"><span data-stu-id="f6a86-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6a86-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f6a86-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f6a86-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f6a86-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="f6a86-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f6a86-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f6a86-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f6a86-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="f6a86-121">Header</span><span class="sxs-lookup"><span data-stu-id="f6a86-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6a86-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f6a86-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6a86-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6a86-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6a86-124">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="f6a86-124">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
