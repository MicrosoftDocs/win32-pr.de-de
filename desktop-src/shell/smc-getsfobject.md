---
description: Fordert einen Zeiger auf ein angegebenes Objekt an.
title: SMC_GETSFOBJECT Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a8478f10-77ce-4e71-a5dc-89d8a90cf513
api_name:
- SMC_GETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c7fb57ea8e3f02ce4e773e187310530c14d65515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216826"
---
# <a name="smc_getsfobject-message"></a><span data-ttu-id="3935a-103">SMC \_ gezfobject-Nachricht</span><span class="sxs-lookup"><span data-stu-id="3935a-103">SMC\_GETSFOBJECT message</span></span>

<span data-ttu-id="3935a-104">Fordert einen Zeiger auf ein angegebenes Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3935a-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETSFOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="3935a-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="3935a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3935a-106">*IID*</span><span class="sxs-lookup"><span data-stu-id="3935a-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="3935a-107">Die dem angeforderten Objekt zugeordnete IID.</span><span class="sxs-lookup"><span data-stu-id="3935a-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="3935a-108">*teuren*</span><span class="sxs-lookup"><span data-stu-id="3935a-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="3935a-109">Ein void-Zeiger, der einen Zeiger auf die angeforderte Schnittstelle empfängt.</span><span class="sxs-lookup"><span data-stu-id="3935a-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3935a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3935a-110">Return value</span></span>

<span data-ttu-id="3935a-111">Gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="3935a-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3935a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3935a-112">Remarks</span></span>

<span data-ttu-id="3935a-113">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="3935a-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="3935a-114">Sie ähnelt der Verwendung von [**SMC \_ GetObject**](smc-getobject.md) , wird jedoch für shellordnerelemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="3935a-114">It is similar to [**SMC\_GETOBJECT**](smc-getobject.md) but used for Shell folder items.</span></span> <span data-ttu-id="3935a-115">Erstellen Sie das angeforderte Objekt, und weisen Sie der angeforderten Schnittstelle einen Zeiger auf *PV* zu.</span><span class="sxs-lookup"><span data-stu-id="3935a-115">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="3935a-116">Die folgenden Schnittstellen können angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="3935a-116">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="3935a-117">**IStream**</span><span class="sxs-lookup"><span data-stu-id="3935a-117">**IStream**</span></span>](/windows/win32/api/objidl/nn-objidl-istream)
-   [<span data-ttu-id="3935a-118">**Ishellmenu**</span><span class="sxs-lookup"><span data-stu-id="3935a-118">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="3935a-119">**Ishellmenucallback**</span><span class="sxs-lookup"><span data-stu-id="3935a-119">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)

## <a name="requirements"></a><span data-ttu-id="3935a-120">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3935a-120">Requirements</span></span>



| <span data-ttu-id="3935a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3935a-121">Requirement</span></span> | <span data-ttu-id="3935a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="3935a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3935a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3935a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3935a-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3935a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3935a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3935a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3935a-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3935a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3935a-127">Header</span><span class="sxs-lookup"><span data-stu-id="3935a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3935a-128"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3935a-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="3935a-129">IDL</span><span class="sxs-lookup"><span data-stu-id="3935a-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3935a-130"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3935a-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
