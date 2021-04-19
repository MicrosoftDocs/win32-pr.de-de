---
description: Benachrichtigt das System, dass die APP Ihre Daten gespeichert hat und bereit ist, angehalten zu werden.
ms.assetid: 5C79AFBA-34E6-4C0B-95A0-731E10D8A17A
title: 'Isuspendingdeferral:: Complete-Methode (Windows. applicationmodel. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral.Complete
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 62febd5fac6aab4a0c5ddd7e6a70fa0e3c3f78ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356764"
---
# <a name="isuspendingdeferralcomplete-method"></a><span data-ttu-id="fb6af-103">Isuspendingdeferral:: Complete-Methode</span><span class="sxs-lookup"><span data-stu-id="fb6af-103">ISuspendingDeferral::Complete method</span></span>

<span data-ttu-id="fb6af-104">Benachrichtigt das System, dass die APP Ihre Daten gespeichert hat und bereit ist, angehalten zu werden.</span><span class="sxs-lookup"><span data-stu-id="fb6af-104">Notifies the system that the app has saved its data and is ready to be suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb6af-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb6af-105">Syntax</span></span>


```C++
HRESULT Complete();
```



## <a name="parameters"></a><span data-ttu-id="fb6af-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb6af-106">Parameters</span></span>

<span data-ttu-id="fb6af-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="fb6af-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb6af-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb6af-108">Return value</span></span>

<span data-ttu-id="fb6af-109">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="fb6af-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fb6af-110">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fb6af-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb6af-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb6af-111">Requirements</span></span>



| <span data-ttu-id="fb6af-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb6af-112">Requirement</span></span> | <span data-ttu-id="fb6af-113">Wert</span><span class="sxs-lookup"><span data-stu-id="fb6af-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb6af-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fb6af-114">Minimum supported client</span></span><br/> | <span data-ttu-id="fb6af-115">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fb6af-115">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="fb6af-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fb6af-116">Minimum supported server</span></span><br/> | <span data-ttu-id="fb6af-117">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fb6af-117">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="fb6af-118">Header</span><span class="sxs-lookup"><span data-stu-id="fb6af-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb6af-119"><dt>Windows. applicationmodel. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb6af-119"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb6af-120">IDL</span><span class="sxs-lookup"><span data-stu-id="fb6af-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb6af-121"><dt>Windows. applicationmodel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb6af-121"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb6af-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb6af-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb6af-123">**Isuspendingdeferral**</span><span class="sxs-lookup"><span data-stu-id="fb6af-123">**ISuspendingDeferral**</span></span>](isuspendingdeferral.md)
</dt> </dl>

 

 




