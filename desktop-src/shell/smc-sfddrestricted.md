---
description: Fragt ab, ob es zulässig ist, ein Datenobjekt für das von der zugehörigen smdata-Struktur angegebene Element zu löschen.
ms.assetid: 777bbc7e-6b0f-4627-9d92-4aa8209082ca
title: SMC_SFDDRESTRICTED Meldung (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ae6a852fd342e67edf42429f31eb7e1ba3b566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980145"
---
# <a name="smc_sfddrestricted-message"></a><span data-ttu-id="9a628-103">SMC \_ sfddrestrihierte Nachricht</span><span class="sxs-lookup"><span data-stu-id="9a628-103">SMC\_SFDDRESTRICTED message</span></span>

<span data-ttu-id="9a628-104">Fragt ab, ob es zulässig ist, ein Datenobjekt für das von der zugehörigen [**smdata**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) -Struktur angegebene Element zu löschen.</span><span class="sxs-lookup"><span data-stu-id="9a628-104">Requests whether it is acceptable to drop a data object on the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFDDRESTRICTED 
    wParam = (WPARAM) (void **) pDropTarget
            
```



## <a name="parameters"></a><span data-ttu-id="9a628-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a628-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a628-106">*pdroptarget*</span><span class="sxs-lookup"><span data-stu-id="9a628-106">*pDropTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="9a628-107">Die Adresse eines void-Zeigers, der einen Zeiger auf Ihre [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) -Schnittstelle empfängt.</span><span class="sxs-lookup"><span data-stu-id="9a628-107">The address of a void pointer that receives a pointer to your [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span> <span data-ttu-id="9a628-108">Legen Sie diesen Wert auf **null** fest, wenn Sie das Datenobjekt nicht akzeptieren möchten.</span><span class="sxs-lookup"><span data-stu-id="9a628-108">Set this value to **NULL** if you do not want to accept the data object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a628-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a628-109">Return value</span></span>

<span data-ttu-id="9a628-110">Gibt "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="9a628-110">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a628-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a628-111">Remarks</span></span>

<span data-ttu-id="9a628-112">Diese Benachrichtigung wird von der [**ishellmenucallback:: callbacksm**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) -Methode empfangen.</span><span class="sxs-lookup"><span data-stu-id="9a628-112">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a628-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="9a628-113">Requirements</span></span>



| <span data-ttu-id="9a628-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a628-114">Requirement</span></span> | <span data-ttu-id="9a628-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9a628-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a628-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a628-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9a628-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a628-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9a628-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a628-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9a628-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a628-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9a628-120">Header</span><span class="sxs-lookup"><span data-stu-id="9a628-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a628-121"><dt>Shobjidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a628-121"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a628-122">IDL</span><span class="sxs-lookup"><span data-stu-id="9a628-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9a628-123"><dt>Shobjidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a628-123"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 
