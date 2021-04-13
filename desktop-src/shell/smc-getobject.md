---
description: Fordert einen Zeiger auf ein angegebenes Objekt an.
title: SMC_GETOBJECT Meldung (shobjidl. h)
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
ms.openlocfilehash: 5d0c0592356bff13e60c122b3c88cad05733e4f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994846"
---
# <a name="smc_getobject-message"></a><span data-ttu-id="f9e0e-103">SMC- \_ GetObject-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f9e0e-103">SMC\_GETOBJECT message</span></span>

<span data-ttu-id="f9e0e-104">Fordert einen Zeiger auf ein angegebenes Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f9e0e-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="f9e0e-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9e0e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9e0e-106">*IID*</span><span class="sxs-lookup"><span data-stu-id="f9e0e-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="f9e0e-107">Die dem angeforderten Objekt zugeordnete IID.</span><span class="sxs-lookup"><span data-stu-id="f9e0e-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="f9e0e-108">*teuren*</span><span class="sxs-lookup"><span data-stu-id="f9e0e-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="f9e0e-109">Ein void-Zeiger, der einen Zeiger auf die angeforderte Schnittstelle empfängt.</span><span class="sxs-lookup"><span data-stu-id="f9e0e-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9e0e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9e0e-110">Return value</span></span>

<span data-ttu-id="f9e0e-111">Gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="f9e0e-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9e0e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9e0e-112">Remarks</span></span>

<span data-ttu-id="f9e0e-113">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="f9e0e-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="f9e0e-114">Erstellen Sie das angeforderte Objekt, und weisen Sie der angeforderten Schnittstelle einen Zeiger auf *PV* zu.</span><span class="sxs-lookup"><span data-stu-id="f9e0e-114">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="f9e0e-115">Die folgenden Schnittstellen können angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f9e0e-115">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="f9e0e-116">**Ishellmenu**</span><span class="sxs-lookup"><span data-stu-id="f9e0e-116">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="f9e0e-117">**IContextMenu**</span><span class="sxs-lookup"><span data-stu-id="f9e0e-117">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
-   [<span data-ttu-id="f9e0e-118">**Ishellmenucallback**</span><span class="sxs-lookup"><span data-stu-id="f9e0e-118">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)
-   [<span data-ttu-id="f9e0e-119">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="f9e0e-119">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

## <a name="requirements"></a><span data-ttu-id="f9e0e-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f9e0e-120">Requirements</span></span>



| <span data-ttu-id="f9e0e-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9e0e-121">Requirement</span></span> | <span data-ttu-id="f9e0e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="f9e0e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e0e-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9e0e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f9e0e-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9e0e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f9e0e-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9e0e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f9e0e-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9e0e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f9e0e-127">Header</span><span class="sxs-lookup"><span data-stu-id="f9e0e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9e0e-128"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9e0e-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9e0e-129">IDL</span><span class="sxs-lookup"><span data-stu-id="f9e0e-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9e0e-130"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f9e0e-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
