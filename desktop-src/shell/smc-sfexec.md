---
description: Führen Sie das in der zugehörigen smdata-Struktur angegebene shellordnerelement aus.
title: SMC_SFEXEC Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bb8f6434-0936-460f-b7dc-39be58bb70ce
api_name:
- SMC_SFEXEC
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b4e414cd7dab9968882272b19b9b21b95da0f1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980144"
---
# <a name="smc_sfexec-message"></a><span data-ttu-id="31ed4-103">SMC \_ sfexec-Nachricht</span><span class="sxs-lookup"><span data-stu-id="31ed4-103">SMC\_SFEXEC message</span></span>

<span data-ttu-id="31ed4-104">Führen Sie das in der zugehörigen [**smdata**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) -Struktur angegebene shellordnerelement aus.</span><span class="sxs-lookup"><span data-stu-id="31ed4-104">Execute the Shell folder item specified in the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFEXEC
            
```



## <a name="parameters"></a><span data-ttu-id="31ed4-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="31ed4-105">Parameters</span></span>

<span data-ttu-id="31ed4-106">Diese Nachricht weist keine Parameter auf.</span><span class="sxs-lookup"><span data-stu-id="31ed4-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="31ed4-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="31ed4-107">Return value</span></span>

<span data-ttu-id="31ed4-108">Gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="31ed4-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="31ed4-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31ed4-109">Remarks</span></span>

<span data-ttu-id="31ed4-110">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="31ed4-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="31ed4-111">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="31ed4-111">Requirements</span></span>



| <span data-ttu-id="31ed4-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31ed4-112">Requirement</span></span> | <span data-ttu-id="31ed4-113">Wert</span><span class="sxs-lookup"><span data-stu-id="31ed4-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31ed4-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="31ed4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="31ed4-115">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31ed4-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="31ed4-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="31ed4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="31ed4-117">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="31ed4-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31ed4-118">Header</span><span class="sxs-lookup"><span data-stu-id="31ed4-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="31ed4-119"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="31ed4-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="31ed4-120">IDL</span><span class="sxs-lookup"><span data-stu-id="31ed4-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="31ed4-121"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="31ed4-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




