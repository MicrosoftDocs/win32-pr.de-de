---
description: Wird aufgerufen, wenn ein Fenster als Shellfenster registriert wird.
title: Dshellwindowsvents. windowregistered-Methode
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
ms.openlocfilehash: b12ed98c6b2a11e5886ed9e76d324a1a6842cda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983068"
---
# <a name="dshellwindowseventswindowregistered-method"></a><span data-ttu-id="943ee-103">Dshellwindowsvents. windowregistered-Methode</span><span class="sxs-lookup"><span data-stu-id="943ee-103">DShellWindowsEvents.WindowRegistered method</span></span>

<span data-ttu-id="943ee-104">Wird aufgerufen, wenn ein Fenster als Shellfenster registriert wird.</span><span class="sxs-lookup"><span data-stu-id="943ee-104">Called when a window is registered as a Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="943ee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="943ee-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="943ee-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="943ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="943ee-107">*lcookie* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="943ee-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="943ee-108">Type: **Integer**</span><span class="sxs-lookup"><span data-stu-id="943ee-108">Type: **Integer**</span></span>

<span data-ttu-id="943ee-109">Das Cookie, das das registrierte Fenster identifiziert.</span><span class="sxs-lookup"><span data-stu-id="943ee-109">The cookie that identifies the window that was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="943ee-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="943ee-110">Return value</span></span>

<span data-ttu-id="943ee-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="943ee-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="943ee-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="943ee-112">Remarks</span></span>

<span data-ttu-id="943ee-113">Einem Fenster wird ein Cookie erteilt, wenn es als Shellfenster registriert wird.</span><span class="sxs-lookup"><span data-stu-id="943ee-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="943ee-114">Weitere Informationen finden Sie unter [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="943ee-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="943ee-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="943ee-115">Requirements</span></span>



| <span data-ttu-id="943ee-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="943ee-116">Requirement</span></span> | <span data-ttu-id="943ee-117">Wert</span><span class="sxs-lookup"><span data-stu-id="943ee-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="943ee-118">Produkt</span><span class="sxs-lookup"><span data-stu-id="943ee-118">Product</span></span><br/> | <span data-ttu-id="943ee-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="943ee-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="943ee-120">DLL</span><span class="sxs-lookup"><span data-stu-id="943ee-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="943ee-121"><dt>Shdocvw.dll (Version 5.00.2014.0216 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="943ee-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="943ee-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="943ee-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="943ee-123">**Dshellwindowgvents**</span><span class="sxs-lookup"><span data-stu-id="943ee-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="943ee-124">**Windows-gesperrt**</span><span class="sxs-lookup"><span data-stu-id="943ee-124">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[<span data-ttu-id="943ee-125">**Register**</span><span class="sxs-lookup"><span data-stu-id="943ee-125">**Register**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[<span data-ttu-id="943ee-126">**Register ausstehend**</span><span class="sxs-lookup"><span data-stu-id="943ee-126">**RegisterPending**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




