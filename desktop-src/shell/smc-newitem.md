---
description: Benachrichtigt Sie über ein neues Element, wie von der zugehörigen smdata-Struktur angegeben.
title: SMC_NEWITEM Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e0ccf2db-cb46-469f-bc08-4b5100a410ba
api_name:
- SMC_NEWITEM
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ebd8f1b6454a2fb592374b860811ebfc7a14f09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980160"
---
# <a name="smc_newitem-message"></a><span data-ttu-id="c054d-103">SMC- \_ netwitem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="c054d-103">SMC\_NEWITEM message</span></span>

<span data-ttu-id="c054d-104">Benachrichtigt Sie über ein neues Element, wie von der zugehörigen [**smdata**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) -Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="c054d-104">Notifies you of a new item, as specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_NEWITEM
            
```



## <a name="parameters"></a><span data-ttu-id="c054d-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="c054d-105">Parameters</span></span>

<span data-ttu-id="c054d-106">Diese Nachricht weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="c054d-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c054d-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c054d-107">Return value</span></span>

<span data-ttu-id="c054d-108">Gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="c054d-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c054d-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c054d-109">Remarks</span></span>

<span data-ttu-id="c054d-110">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="c054d-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c054d-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c054d-111">Requirements</span></span>



| <span data-ttu-id="c054d-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c054d-112">Requirement</span></span> | <span data-ttu-id="c054d-113">Wert</span><span class="sxs-lookup"><span data-stu-id="c054d-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c054d-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c054d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c054d-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c054d-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c054d-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c054d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c054d-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c054d-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c054d-118">Header</span><span class="sxs-lookup"><span data-stu-id="c054d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c054d-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c054d-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="c054d-120">IDL</span><span class="sxs-lookup"><span data-stu-id="c054d-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c054d-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c054d-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




