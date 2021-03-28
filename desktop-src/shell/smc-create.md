---
description: Benachrichtigt Sie, dass ein Menüband erstellt wurde.
title: SMC_CREATE Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8eeca6f6-1718-4ff6-b4a7-4b68b9527468
api_name:
- SMC_CREATE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 59219f376288431fa20e198d8c427ff40c7fba62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994863"
---
# <a name="smc_create-message"></a><span data-ttu-id="90205-103">SMC \_ Create-Meldung</span><span class="sxs-lookup"><span data-stu-id="90205-103">SMC\_CREATE message</span></span>

<span data-ttu-id="90205-104">Benachrichtigt Sie, dass ein Menüband erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="90205-104">Notifies you that a menu band has been created.</span></span>


```C++
SMC_CREATE 
    lParam = (LPARAM) (LPSMDATA) psmd
            
```



## <a name="parameters"></a><span data-ttu-id="90205-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="90205-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90205-106">*psmd*</span><span class="sxs-lookup"><span data-stu-id="90205-106">*psmd*</span></span> 
</dt> <dd>

<span data-ttu-id="90205-107">Ein Zeiger auf den **pvuserdata** -Member einer [**smdata**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="90205-107">A pointer to the **pvUserData** member of an [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90205-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="90205-108">Return value</span></span>

<span data-ttu-id="90205-109">Gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="90205-109">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="90205-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90205-110">Remarks</span></span>

<span data-ttu-id="90205-111">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="90205-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="90205-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="90205-112">Requirements</span></span>



| <span data-ttu-id="90205-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90205-113">Requirement</span></span> | <span data-ttu-id="90205-114">Wert</span><span class="sxs-lookup"><span data-stu-id="90205-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="90205-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90205-115">Minimum supported client</span></span><br/> | <span data-ttu-id="90205-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90205-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="90205-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90205-117">Minimum supported server</span></span><br/> | <span data-ttu-id="90205-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90205-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="90205-119">Header</span><span class="sxs-lookup"><span data-stu-id="90205-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="90205-120"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="90205-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="90205-121">IDL</span><span class="sxs-lookup"><span data-stu-id="90205-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="90205-122"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="90205-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




