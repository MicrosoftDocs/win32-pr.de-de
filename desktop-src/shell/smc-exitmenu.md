---
description: Benachrichtigt Sie, dass das Menü reduziert wird.
title: SMC_EXITMENU Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 868b4819-1dbf-497a-9c79-5935f503969a
api_name:
- SMC_EXITMENU
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e9a8680617a17ce0069a8633e1c70ff6b32a4be7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960084"
---
# <a name="smc_exitmenu-message"></a><span data-ttu-id="b8460-103">SMC- \_ exitmenu-Meldung</span><span class="sxs-lookup"><span data-stu-id="b8460-103">SMC\_EXITMENU message</span></span>

<span data-ttu-id="b8460-104">Benachrichtigt Sie, dass das Menü reduziert wird.</span><span class="sxs-lookup"><span data-stu-id="b8460-104">Notifies you that the menu is collapsing.</span></span>


```C++
SMC_EXITMENU
            
```



## <a name="parameters"></a><span data-ttu-id="b8460-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="b8460-105">Parameters</span></span>

<span data-ttu-id="b8460-106">Diese Nachricht weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="b8460-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b8460-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b8460-107">Return value</span></span>

<span data-ttu-id="b8460-108">Gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="b8460-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8460-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8460-109">Remarks</span></span>

<span data-ttu-id="b8460-110">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="b8460-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8460-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="b8460-111">Requirements</span></span>



| <span data-ttu-id="b8460-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8460-112">Requirement</span></span> | <span data-ttu-id="b8460-113">Wert</span><span class="sxs-lookup"><span data-stu-id="b8460-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8460-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8460-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b8460-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8460-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b8460-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8460-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b8460-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8460-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b8460-118">Header</span><span class="sxs-lookup"><span data-stu-id="b8460-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8460-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8460-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="b8460-120">IDL</span><span class="sxs-lookup"><span data-stu-id="b8460-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b8460-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b8460-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




