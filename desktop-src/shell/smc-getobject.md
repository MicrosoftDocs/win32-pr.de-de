---
description: 'SMC_GETOBJECT: Fordert einen Zeiger auf ein angegebenes Objekt an.'
title: SMC_GETOBJECT (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36e8f304-a92a-485f-8413-b9c416087ec9
api_name:
- SMC_GETOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 58741290d741cc18fd788282d0f302ef87bb15dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108100438"
---
# <a name="smc_getobject-message"></a><span data-ttu-id="4b541-103">SMC \_ GETOBJECT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="4b541-103">SMC\_GETOBJECT message</span></span>

<span data-ttu-id="4b541-104">Fordert einen Zeiger auf ein angegebenes Objekt an.</span><span class="sxs-lookup"><span data-stu-id="4b541-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="4b541-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b541-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b541-106">*Iid*</span><span class="sxs-lookup"><span data-stu-id="4b541-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="4b541-107">Die IID, die dem angeforderten Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4b541-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="4b541-108">*Pv*</span><span class="sxs-lookup"><span data-stu-id="4b541-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="4b541-109">Ein void-Zeiger, der einen Zeiger auf die angeforderte Schnittstelle empfängt.</span><span class="sxs-lookup"><span data-stu-id="4b541-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b541-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4b541-110">Return value</span></span>

<span data-ttu-id="4b541-111">Geben Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="4b541-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b541-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4b541-112">Remarks</span></span>

<span data-ttu-id="4b541-113">Diese Benachrichtigung wird von der [**IShellMenuCallback::CallbackSM-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) empfangen.</span><span class="sxs-lookup"><span data-stu-id="4b541-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="4b541-114">Erstellen Sie das angeforderte Objekt, und weisen Sie pv einen Zeiger auf die angeforderte Schnittstelle *zu.*</span><span class="sxs-lookup"><span data-stu-id="4b541-114">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="4b541-115">Die folgenden Schnittstellen können angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="4b541-115">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="4b541-116">**IShellMenu**</span><span class="sxs-lookup"><span data-stu-id="4b541-116">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="4b541-117">**IContextMenu**</span><span class="sxs-lookup"><span data-stu-id="4b541-117">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
-   [<span data-ttu-id="4b541-118">**IShellMenuCallback**</span><span class="sxs-lookup"><span data-stu-id="4b541-118">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)
-   [<span data-ttu-id="4b541-119">**Idroptarget**</span><span class="sxs-lookup"><span data-stu-id="4b541-119">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

## <a name="requirements"></a><span data-ttu-id="4b541-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b541-120">Requirements</span></span>



| <span data-ttu-id="4b541-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b541-121">Requirement</span></span> | <span data-ttu-id="4b541-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4b541-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b541-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b541-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4b541-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b541-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4b541-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b541-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4b541-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b541-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4b541-127">Header</span><span class="sxs-lookup"><span data-stu-id="4b541-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b541-128"><dt>Shobjidl.h</dt></span><span class="sxs-lookup"><span data-stu-id="4b541-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="4b541-129">Idl</span><span class="sxs-lookup"><span data-stu-id="4b541-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4b541-130"><dt>Shobjidl.idl</dt></span><span class="sxs-lookup"><span data-stu-id="4b541-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
