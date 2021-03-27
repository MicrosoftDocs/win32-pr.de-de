---
description: Benachrichtigt Sie, das Menüband zu initialisieren.
title: SMC_INITMENU Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 415ee805-2b57-4f8f-85d9-2b38cd05998d
api_name:
- SMC_INITMENU
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ed7f7be1786192fb2be42f6d36cfb4bf222136fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216825"
---
# <a name="smc_initmenu-message"></a><span data-ttu-id="d5d8c-103">SMC \_ InitMenu-Meldung</span><span class="sxs-lookup"><span data-stu-id="d5d8c-103">SMC\_INITMENU message</span></span>

<span data-ttu-id="d5d8c-104">Benachrichtigt Sie, das Menüband zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="d5d8c-104">Notifies you to initialize the menu band.</span></span>


```C++
SMC_INITMENU
            
```



## <a name="parameters"></a><span data-ttu-id="d5d8c-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5d8c-105">Parameters</span></span>

<span data-ttu-id="d5d8c-106">Diese Nachricht weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="d5d8c-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5d8c-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5d8c-107">Return value</span></span>

<span data-ttu-id="d5d8c-108">Gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="d5d8c-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5d8c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5d8c-109">Remarks</span></span>

<span data-ttu-id="d5d8c-110">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="d5d8c-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5d8c-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d5d8c-111">Requirements</span></span>



| <span data-ttu-id="d5d8c-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5d8c-112">Requirement</span></span> | <span data-ttu-id="d5d8c-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d5d8c-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d8c-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d5d8c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d5d8c-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5d8c-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d5d8c-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d5d8c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d5d8c-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d5d8c-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d5d8c-118">Header</span><span class="sxs-lookup"><span data-stu-id="d5d8c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5d8c-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5d8c-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5d8c-120">IDL</span><span class="sxs-lookup"><span data-stu-id="d5d8c-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d5d8c-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d5d8c-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




