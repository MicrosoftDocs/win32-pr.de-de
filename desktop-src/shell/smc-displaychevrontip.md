---
description: Benachrichtigt Sie, dass ein Infotipp für das Chevron angezeigt wird, das dem von der zugehörigen smdata-Struktur angegebenen Element zugeordnet ist.
title: SMC_DISPLAYCHEVRONTIP Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e4ec4839-e49a-4563-9bc9-79f9d4d54658
api_name:
- SMC_DISPLAYCHEVRONTIP
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09e01fc6ea169d8dcbf5758ace341198166a3a9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485507"
---
# <a name="smc_displaychevrontip-message"></a><span data-ttu-id="9532f-103">SMC \_ displaychevrontip-Meldung</span><span class="sxs-lookup"><span data-stu-id="9532f-103">SMC\_DISPLAYCHEVRONTIP message</span></span>

<span data-ttu-id="9532f-104">Benachrichtigt Sie, dass ein Infotipp für das Chevron angezeigt wird, das dem von der zugehörigen [**smdata**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) -Struktur angegebenen Element zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9532f-104">Notifies you that an infotip is about to be displayed for the chevron associated with the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DISPLAYCHEVRONTIP
            
```



## <a name="parameters"></a><span data-ttu-id="9532f-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="9532f-105">Parameters</span></span>

<span data-ttu-id="9532f-106">Diese Nachricht weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="9532f-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9532f-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9532f-107">Return value</span></span>

<span data-ttu-id="9532f-108">Gibt "S OK" zurück \_ , um den infotip anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9532f-108">Return S\_OK to display the infotip.</span></span> <span data-ttu-id="9532f-109">Gibt den Wert "false" zurück \_ , um zu verhindern, dass InfoTipp angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9532f-109">Return S\_FALSE to prevent the infotip from being displayed.</span></span>

## <a name="remarks"></a><span data-ttu-id="9532f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9532f-110">Remarks</span></span>

<span data-ttu-id="9532f-111">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="9532f-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9532f-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9532f-112">Requirements</span></span>



| <span data-ttu-id="9532f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9532f-113">Requirement</span></span> | <span data-ttu-id="9532f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="9532f-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9532f-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9532f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9532f-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9532f-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9532f-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9532f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9532f-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9532f-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9532f-119">Header</span><span class="sxs-lookup"><span data-stu-id="9532f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9532f-120"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9532f-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="9532f-121">IDL</span><span class="sxs-lookup"><span data-stu-id="9532f-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9532f-122"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9532f-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




