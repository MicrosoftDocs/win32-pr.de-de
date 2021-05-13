---
description: Wird aufgerufen, wenn ein Fenster als Shellfenster registriert wird.
title: DShellWindowsEvents.WindowRegistered-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRegistered
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 7faf758a-daa0-47f5-9f95-61fe3d8286ea
ms.openlocfilehash: 64bf83a88584c5d97994726696d4fb3a1e971bdf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841451"
---
# <a name="dshellwindowseventswindowregistered-method"></a><span data-ttu-id="11781-103">DShellWindowsEvents.WindowRegistered-Methode</span><span class="sxs-lookup"><span data-stu-id="11781-103">DShellWindowsEvents.WindowRegistered method</span></span>

<span data-ttu-id="11781-104">Wird aufgerufen, wenn ein Fenster als Shellfenster registriert wird.</span><span class="sxs-lookup"><span data-stu-id="11781-104">Called when a window is registered as a Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="11781-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="11781-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="11781-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="11781-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11781-107">*lCookie* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="11781-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11781-108">Typ: **Integer**</span><span class="sxs-lookup"><span data-stu-id="11781-108">Type: **Integer**</span></span>

<span data-ttu-id="11781-109">Das Cookie, das das registrierte Fenster identifiziert.</span><span class="sxs-lookup"><span data-stu-id="11781-109">The cookie that identifies the window that was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11781-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11781-110">Return value</span></span>

<span data-ttu-id="11781-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="11781-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="11781-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="11781-112">Remarks</span></span>

<span data-ttu-id="11781-113">Einem Fenster wird ein Cookie erteilt, wenn es als Shellfenster registriert wird.</span><span class="sxs-lookup"><span data-stu-id="11781-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="11781-114">Weitere Informationen finden Sie unter [**Registrieren von**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="11781-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="11781-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11781-115">Requirements</span></span>



| <span data-ttu-id="11781-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11781-116">Requirement</span></span> | <span data-ttu-id="11781-117">Wert</span><span class="sxs-lookup"><span data-stu-id="11781-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11781-118">Produkt</span><span class="sxs-lookup"><span data-stu-id="11781-118">Product</span></span><br/> | <span data-ttu-id="11781-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="11781-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="11781-120">DLL</span><span class="sxs-lookup"><span data-stu-id="11781-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="11781-121"><dt>Shdocvw.dll (Version 5.00.2014.0216 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="11781-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11781-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11781-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11781-123">**DShellWindowsEvents**</span><span class="sxs-lookup"><span data-stu-id="11781-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="11781-124">**WindowRevoked**</span><span class="sxs-lookup"><span data-stu-id="11781-124">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[<span data-ttu-id="11781-125">**Registrieren**</span><span class="sxs-lookup"><span data-stu-id="11781-125">**Register**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[<span data-ttu-id="11781-126">**RegisterPending**</span><span class="sxs-lookup"><span data-stu-id="11781-126">**RegisterPending**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




