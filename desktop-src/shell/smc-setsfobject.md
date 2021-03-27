---
description: Benachrichtigt Sie, das bestandene-Objekt zu speichern.
title: SMC_SETSFOBJECT Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f7e2cf12-7f09-45b0-97d3-eed803e57d9f
api_name:
- SMC_SETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 44aeb41ab7dcd271f8c84bff4eb8b5525ac66e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216824"
---
# <a name="smc_setsfobject-message"></a><span data-ttu-id="473a5-103">SMC- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="473a5-103">SMC\_SETSFOBJECT message</span></span>

<span data-ttu-id="473a5-104">Benachrichtigt Sie, das bestandene-Objekt zu speichern.</span><span class="sxs-lookup"><span data-stu-id="473a5-104">Notifies you to save the passed object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="473a5-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="473a5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="473a5-106">*IID*</span><span class="sxs-lookup"><span data-stu-id="473a5-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="473a5-107">Die IID, die dem Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="473a5-107">The IID associated with the object.</span></span>

</dd> <dt>

<span data-ttu-id="473a5-108">*teuren*</span><span class="sxs-lookup"><span data-stu-id="473a5-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="473a5-109">Ein Zeiger auf die-Schnittstelle für das von *IID* angegebene Objekt.</span><span class="sxs-lookup"><span data-stu-id="473a5-109">A pointer the interface on the object specified by *iid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="473a5-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="473a5-110">Return value</span></span>

<span data-ttu-id="473a5-111">Gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="473a5-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="473a5-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="473a5-112">Remarks</span></span>

<span data-ttu-id="473a5-113">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="473a5-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

<span data-ttu-id="473a5-114">Die **SMC \_** -Abmelde Benachrichtigung wird mit dem IID- \_ Stream verwendet.</span><span class="sxs-lookup"><span data-stu-id="473a5-114">The **SMC\_SETSFOBJECT** notification is used with IID\_Stream.</span></span> <span data-ttu-id="473a5-115">Das Objekt wird in einem persistenten Formular in der Registrierung gespeichert, und es wird nichts mit dem Verweis Zähler für das über gegebene Objekt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="473a5-115">The object is saved into a persisted form in the registry and nothing is done with the reference count on the object passed in.</span></span>

## <a name="requirements"></a><span data-ttu-id="473a5-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="473a5-116">Requirements</span></span>



| <span data-ttu-id="473a5-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="473a5-117">Requirement</span></span> | <span data-ttu-id="473a5-118">Wert</span><span class="sxs-lookup"><span data-stu-id="473a5-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="473a5-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="473a5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="473a5-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="473a5-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="473a5-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="473a5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="473a5-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="473a5-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="473a5-123">Header</span><span class="sxs-lookup"><span data-stu-id="473a5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="473a5-124"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="473a5-124"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="473a5-125">IDL</span><span class="sxs-lookup"><span data-stu-id="473a5-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="473a5-126"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="473a5-126"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




