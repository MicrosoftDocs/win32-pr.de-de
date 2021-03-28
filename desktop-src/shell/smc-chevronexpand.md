---
description: Der Benutzer hat auf ein Chevron geklickt, um das von der zugehörigen smdata-Struktur angegebene Element zu erweitern.
title: SMC_CHEVRONEXPAND Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cb0b3cf1-1a12-4236-96e9-cc04360d269f
api_name:
- SMC_CHEVRONEXPAND
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6ecf8f86e111326b3f37f3111c382d2d04ef2fa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216830"
---
# <a name="smc_chevronexpand-message"></a><span data-ttu-id="94877-103">SMC \_ chevronexpand-Nachricht</span><span class="sxs-lookup"><span data-stu-id="94877-103">SMC\_CHEVRONEXPAND message</span></span>

<span data-ttu-id="94877-104">Der Benutzer hat auf ein Chevron geklickt, um das von der zugehörigen [**smdata**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) -Struktur angegebene Element zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="94877-104">The user has clicked a chevron to expand the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_CHEVRONEXPAND
            
```



## <a name="parameters"></a><span data-ttu-id="94877-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="94877-105">Parameters</span></span>

<span data-ttu-id="94877-106">Diese Nachricht weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="94877-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="94877-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94877-107">Return value</span></span>

<span data-ttu-id="94877-108">Gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="94877-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="94877-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94877-109">Remarks</span></span>

<span data-ttu-id="94877-110">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="94877-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="94877-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="94877-111">Requirements</span></span>



| <span data-ttu-id="94877-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94877-112">Requirement</span></span> | <span data-ttu-id="94877-113">Wert</span><span class="sxs-lookup"><span data-stu-id="94877-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94877-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94877-114">Minimum supported client</span></span><br/> | <span data-ttu-id="94877-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94877-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="94877-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94877-116">Minimum supported server</span></span><br/> | <span data-ttu-id="94877-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94877-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="94877-118">Header</span><span class="sxs-lookup"><span data-stu-id="94877-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="94877-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="94877-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="94877-120">IDL</span><span class="sxs-lookup"><span data-stu-id="94877-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="94877-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="94877-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




