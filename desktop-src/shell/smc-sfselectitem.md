---
description: Der Benutzer hat das von der zugehörigen smdata-Struktur angegebene Element ausgewählt.
title: SMC_SFSELECTITEM Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 82c3dfca-98a8-43ca-bebc-85bfdf640d38
api_name:
- SMC_SFSELECTITEM
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cfb3384fcfff73d264d21c53a91ede554cc7da5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979808"
---
# <a name="smc_sfselectitem-message"></a><span data-ttu-id="121de-103">SMC \_ sfselectitem-Nachricht</span><span class="sxs-lookup"><span data-stu-id="121de-103">SMC\_SFSELECTITEM message</span></span>

<span data-ttu-id="121de-104">Der Benutzer hat das von der zugehörigen [**smdata**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) -Struktur angegebene Element ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="121de-104">The user has selected the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFSELECTITEM
            
```



## <a name="parameters"></a><span data-ttu-id="121de-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="121de-105">Parameters</span></span>

<span data-ttu-id="121de-106">Diese Nachricht weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="121de-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="121de-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="121de-107">Return value</span></span>

<span data-ttu-id="121de-108">Gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="121de-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="121de-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="121de-109">Remarks</span></span>

<span data-ttu-id="121de-110">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="121de-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="121de-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="121de-111">Requirements</span></span>



| <span data-ttu-id="121de-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="121de-112">Requirement</span></span> | <span data-ttu-id="121de-113">Wert</span><span class="sxs-lookup"><span data-stu-id="121de-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="121de-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="121de-114">Minimum supported client</span></span><br/> | <span data-ttu-id="121de-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="121de-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="121de-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="121de-116">Minimum supported server</span></span><br/> | <span data-ttu-id="121de-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="121de-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="121de-118">Header</span><span class="sxs-lookup"><span data-stu-id="121de-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="121de-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="121de-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="121de-120">IDL</span><span class="sxs-lookup"><span data-stu-id="121de-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="121de-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="121de-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




