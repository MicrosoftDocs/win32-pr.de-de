---
description: Ruft die Methode ab, die aufgerufen wird, wenn die asynchrone Aktion abgeschlossen ist.
ms.assetid: 5050BF84-F9E0-4B3E-9252-6C5C1060826E
title: 'Iasyncaction:: get_Completed-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.get_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: bc018912b2b4643cc4ef2f48cc76eb997a2627fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129240"
---
# <a name="iasyncactionget_completed-method"></a><span data-ttu-id="6a45b-103">Iasyncaction:: get- \_ Methode abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="6a45b-103">IAsyncAction::get\_Completed method</span></span>

<span data-ttu-id="6a45b-104">Ruft die Methode ab, die aufgerufen wird, wenn die asynchrone Aktion abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6a45b-104">Gets the method that is called when the asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a45b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a45b-105">Syntax</span></span>


```C++
HRESULT get_Completed(
  [out] AsyncActionCompletedHandler **handler
);
```



## <a name="parameters"></a><span data-ttu-id="6a45b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a45b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a45b-107">*Handler* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6a45b-107">*handler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a45b-108">Typ: **[ **asyncactioncompletedhandler**](asyncactioncompletedhandler.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6a45b-108">Type: **[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***</span></span>

<span data-ttu-id="6a45b-109">Die Methode, die die Abschluss Benachrichtigung behandelt.</span><span class="sxs-lookup"><span data-stu-id="6a45b-109">The method that handles the completion notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a45b-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a45b-110">Return value</span></span>

<span data-ttu-id="6a45b-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6a45b-111">Type: **HRESULT**</span></span>

<span data-ttu-id="6a45b-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="6a45b-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6a45b-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6a45b-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a45b-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a45b-114">Requirements</span></span>



| <span data-ttu-id="6a45b-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a45b-115">Requirement</span></span> | <span data-ttu-id="6a45b-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6a45b-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a45b-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a45b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6a45b-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6a45b-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="6a45b-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a45b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6a45b-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6a45b-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="6a45b-121">Header</span><span class="sxs-lookup"><span data-stu-id="6a45b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a45b-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6a45b-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a45b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a45b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a45b-124">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="6a45b-124">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
