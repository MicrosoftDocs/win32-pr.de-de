---
description: Stufen Sie das von der zugehörigen smdata-Struktur angegebene Element höher.
title: SMC_PROMOTE Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b1208673-06b4-42b2-b4ac-872fd22927df
api_name:
- SMC_PROMOTE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 22718e51d6ef1bf7e3c5652741b95cadb4db9937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980152"
---
# <a name="smc_promote-message"></a><span data-ttu-id="e6479-103">SMC \_ Promote-Nachricht</span><span class="sxs-lookup"><span data-stu-id="e6479-103">SMC\_PROMOTE message</span></span>

<span data-ttu-id="e6479-104">Stufen Sie das von der zugehörigen [**smdata**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) -Struktur angegebene Element höher.</span><span class="sxs-lookup"><span data-stu-id="e6479-104">Promote the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_PROMOTE
```



## <a name="parameters"></a><span data-ttu-id="e6479-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6479-105">Parameters</span></span>

<span data-ttu-id="e6479-106">Diese Nachricht weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="e6479-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6479-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6479-107">Return value</span></span>

<span data-ttu-id="e6479-108">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="e6479-108">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6479-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6479-109">Remarks</span></span>

<span data-ttu-id="e6479-110">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="e6479-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6479-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="e6479-111">Requirements</span></span>



| <span data-ttu-id="e6479-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6479-112">Requirement</span></span> | <span data-ttu-id="e6479-113">Wert</span><span class="sxs-lookup"><span data-stu-id="e6479-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6479-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6479-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e6479-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6479-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e6479-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6479-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e6479-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6479-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e6479-118">Header</span><span class="sxs-lookup"><span data-stu-id="e6479-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6479-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6479-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="e6479-120">IDL</span><span class="sxs-lookup"><span data-stu-id="e6479-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e6479-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e6479-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




