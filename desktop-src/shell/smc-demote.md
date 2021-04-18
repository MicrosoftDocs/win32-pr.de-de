---
description: Herabstufen des Elements, das durch die zugehörige smdata-Struktur angegeben wird.
title: SMC_DEMOTE Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4809fbd1-da66-4453-b4f2-e75cb5b3457c
api_name:
- SMC_DEMOTE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 46e5505571402feec24d81a9184b713e1c61ae0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994855"
---
# <a name="smc_demote-message"></a><span data-ttu-id="d7bf9-103">SMC Herabstufung der \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="d7bf9-103">SMC\_DEMOTE message</span></span>

<span data-ttu-id="d7bf9-104">Herabstufen des Elements, das durch die zugehörige [**smdata**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) -Struktur angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-104">Demote the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DEMOTE
            
```



## <a name="parameters"></a><span data-ttu-id="d7bf9-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7bf9-105">Parameters</span></span>

<span data-ttu-id="d7bf9-106">Diese Nachricht weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d7bf9-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7bf9-107">Return value</span></span>

<span data-ttu-id="d7bf9-108">Gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="d7bf9-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7bf9-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7bf9-109">Remarks</span></span>

<span data-ttu-id="d7bf9-110">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="d7bf9-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7bf9-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d7bf9-111">Requirements</span></span>



| <span data-ttu-id="d7bf9-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7bf9-112">Requirement</span></span> | <span data-ttu-id="d7bf9-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d7bf9-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7bf9-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7bf9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d7bf9-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7bf9-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d7bf9-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7bf9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d7bf9-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7bf9-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7bf9-118">Header</span><span class="sxs-lookup"><span data-stu-id="d7bf9-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7bf9-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7bf9-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7bf9-120">IDL</span><span class="sxs-lookup"><span data-stu-id="d7bf9-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d7bf9-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d7bf9-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




