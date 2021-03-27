---
description: Sendet eine Benachrichtigung, dass die Menüs vollständig aktualisiert wurden, und Sie können den Status zurücksetzen.
title: SMC_REFRESH Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8c79d9d5-b7dc-4271-9edb-93b40606c9be
api_name:
- SMC_REFRESH
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: aab18245c6502d4d3424e6ed6727eceb5a329d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866539"
---
# <a name="smc_refresh-message"></a><span data-ttu-id="840e5-103">SMC- \_ Aktualisierungs Meldung</span><span class="sxs-lookup"><span data-stu-id="840e5-103">SMC\_REFRESH message</span></span>

<span data-ttu-id="840e5-104">Sendet eine Benachrichtigung, dass die Menüs vollständig aktualisiert wurden, und Sie können den Status zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="840e5-104">Sends notification that the menus have completely refreshed and you can reset your state.</span></span>


```C++
SMC_REFRESH
            
```



## <a name="parameters"></a><span data-ttu-id="840e5-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="840e5-105">Parameters</span></span>

<span data-ttu-id="840e5-106">Diese Nachricht weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="840e5-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="840e5-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="840e5-107">Return value</span></span>

<span data-ttu-id="840e5-108">Gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="840e5-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="840e5-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="840e5-109">Remarks</span></span>

<span data-ttu-id="840e5-110">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="840e5-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="840e5-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="840e5-111">Requirements</span></span>



| <span data-ttu-id="840e5-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="840e5-112">Requirement</span></span> | <span data-ttu-id="840e5-113">Wert</span><span class="sxs-lookup"><span data-stu-id="840e5-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="840e5-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="840e5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="840e5-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="840e5-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="840e5-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="840e5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="840e5-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="840e5-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="840e5-118">Header</span><span class="sxs-lookup"><span data-stu-id="840e5-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="840e5-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="840e5-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="840e5-120">IDL</span><span class="sxs-lookup"><span data-stu-id="840e5-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="840e5-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="840e5-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




