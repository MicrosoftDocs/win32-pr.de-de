---
title: RBN_MINMAX Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Grund leisten-Steuerelement gesendet, bevor ein Band maximiert oder minimiert wird. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 75619cb0-ef0b-44fa-83b2-15a5e5e92c60
keywords:
- Windows-Steuerelemente für RBN_MINMAX Benachrichtigungs
topic_type:
- apiref
api_name:
- RBN_MINMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3569a28d0c0a610ccccf42d11ff4b2e5b4b0007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341391"
---
# <a name="rbn_minmax-notification-code"></a><span data-ttu-id="81f74-105">RBN- \_ MinMax-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="81f74-105">RBN\_MINMAX notification code</span></span>

<span data-ttu-id="81f74-106">Wird von einem Grund leisten-Steuerelement gesendet, bevor ein Band maximiert oder minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="81f74-106">Sent by a rebar control prior to maximizing or minimizing a band.</span></span> <span data-ttu-id="81f74-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="81f74-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_MINMAX
```



## <a name="parameters"></a><span data-ttu-id="81f74-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="81f74-108">Parameters</span></span>

<span data-ttu-id="81f74-109">Dieser Benachrichtigungs Code weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="81f74-109">This notification code has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81f74-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="81f74-110">Return value</span></span>

<span data-ttu-id="81f74-111">Gibt einen Wert ungleich 0 (null) zurück, um zu verhindern, dass der Vorgang stattfindet, und NULL, um den Vorgang fortzusetzen</span><span class="sxs-lookup"><span data-stu-id="81f74-111">Return a nonzero value to prevent the operation from taking place, zero to allow it to continue.</span></span>

## <a name="requirements"></a><span data-ttu-id="81f74-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="81f74-112">Requirements</span></span>



| <span data-ttu-id="81f74-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="81f74-113">Requirement</span></span> | <span data-ttu-id="81f74-114">Wert</span><span class="sxs-lookup"><span data-stu-id="81f74-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81f74-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="81f74-115">Minimum supported client</span></span><br/> | <span data-ttu-id="81f74-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81f74-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="81f74-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="81f74-117">Minimum supported server</span></span><br/> | <span data-ttu-id="81f74-118">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="81f74-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="81f74-119">Header</span><span class="sxs-lookup"><span data-stu-id="81f74-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="81f74-120"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="81f74-120"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





