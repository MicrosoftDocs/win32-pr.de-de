---
description: 'SMC_GETSFOBJECT Meldung: Fordert einen Zeiger auf ein angegebenes Objekt an.'
title: SMC_GETSFOBJECT Nachricht (Shobjidl.h)
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
ms.openlocfilehash: 612b43c193cd1919db4a5cf9dba3a8fdba1c81c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086608"
---
# <a name="smc_getsfobject-message"></a><span data-ttu-id="a7b1e-103">SMC \_ GETSFOBJECT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a7b1e-103">SMC\_GETSFOBJECT message</span></span>

<span data-ttu-id="a7b1e-104">Fordert einen Zeiger auf ein angegebenes Objekt an.</span><span class="sxs-lookup"><span data-stu-id="a7b1e-104">Requests a pointer to a specified object.</span></span>


```C++
SMC_GETSFOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="a7b1e-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7b1e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7b1e-106">*Iid*</span><span class="sxs-lookup"><span data-stu-id="a7b1e-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="a7b1e-107">Die IID, die dem angeforderten Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a7b1e-107">The IID associated with the requested object.</span></span>

</dd> <dt>

<span data-ttu-id="a7b1e-108">*Pv*</span><span class="sxs-lookup"><span data-stu-id="a7b1e-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="a7b1e-109">Ein void-Zeiger, der einen Zeiger auf die angeforderte Schnittstelle empfängt.</span><span class="sxs-lookup"><span data-stu-id="a7b1e-109">A void pointer that receives a pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7b1e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7b1e-110">Return value</span></span>

<span data-ttu-id="a7b1e-111">Geben Sie S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="a7b1e-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7b1e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7b1e-112">Remarks</span></span>

<span data-ttu-id="a7b1e-113">Diese Benachrichtigung wird von der [**IShellMenuCallback::CallbackSM-Methode**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) empfangen.</span><span class="sxs-lookup"><span data-stu-id="a7b1e-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span> <span data-ttu-id="a7b1e-114">Es ähnelt [**SMC \_ GETOBJECT,**](smc-getobject.md) wird aber für Shell-Ordnerelemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7b1e-114">It is similar to [**SMC\_GETOBJECT**](smc-getobject.md) but used for Shell folder items.</span></span> <span data-ttu-id="a7b1e-115">Erstellen Sie das angeforderte Objekt, und weisen Sie pv einen Zeiger *auf* die angeforderte Schnittstelle zu.</span><span class="sxs-lookup"><span data-stu-id="a7b1e-115">Create the requested object and assign a pointer to the requested interface to *pv*.</span></span>

<span data-ttu-id="a7b1e-116">Die folgenden Schnittstellen können angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="a7b1e-116">The following interfaces may be requested.</span></span>

-   [<span data-ttu-id="a7b1e-117">**Istream**</span><span class="sxs-lookup"><span data-stu-id="a7b1e-117">**IStream**</span></span>](/windows/win32/api/objidl/nn-objidl-istream)
-   [<span data-ttu-id="a7b1e-118">**IShellMenu**</span><span class="sxs-lookup"><span data-stu-id="a7b1e-118">**IShellMenu**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [<span data-ttu-id="a7b1e-119">**IShellMenuCallback**</span><span class="sxs-lookup"><span data-stu-id="a7b1e-119">**IShellMenuCallback**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)

## <a name="requirements"></a><span data-ttu-id="a7b1e-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7b1e-120">Requirements</span></span>



| <span data-ttu-id="a7b1e-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7b1e-121">Requirement</span></span> | <span data-ttu-id="a7b1e-122">Wert</span><span class="sxs-lookup"><span data-stu-id="a7b1e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7b1e-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7b1e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a7b1e-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7b1e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a7b1e-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7b1e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a7b1e-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7b1e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a7b1e-127">Header</span><span class="sxs-lookup"><span data-stu-id="a7b1e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7b1e-128"><dt>Shobjidl.h</dt></span><span class="sxs-lookup"><span data-stu-id="a7b1e-128"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7b1e-129">Idl</span><span class="sxs-lookup"><span data-stu-id="a7b1e-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7b1e-130"><dt>Shobjidl.idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7b1e-130"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
