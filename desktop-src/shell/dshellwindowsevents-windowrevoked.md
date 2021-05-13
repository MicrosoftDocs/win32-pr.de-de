---
description: Wird aufgerufen, wenn die Registrierung eines Shellfensters widerrufen wird.
title: DShellWindowsEvents.WindowRevoked-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRevoked
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 92e8653f-7f41-4e0b-97e5-429fddc51951
ms.openlocfilehash: 7ed78dcaa545b2321b04aff9ff2f4e711f93c992
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843181"
---
# <a name="dshellwindowseventswindowrevoked-method"></a><span data-ttu-id="a5b57-103">DShellWindowsEvents.WindowRevoked-Methode</span><span class="sxs-lookup"><span data-stu-id="a5b57-103">DShellWindowsEvents.WindowRevoked method</span></span>

<span data-ttu-id="a5b57-104">Wird aufgerufen, wenn die Registrierung eines Shellfensters widerrufen wird.</span><span class="sxs-lookup"><span data-stu-id="a5b57-104">Called when a Shell window's registration is revoked.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b57-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5b57-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="a5b57-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5b57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5b57-107">*lCookie* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="a5b57-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5b57-108">Typ: **Ganze Zahl**</span><span class="sxs-lookup"><span data-stu-id="a5b57-108">Type: **Integer**</span></span>

<span data-ttu-id="a5b57-109">Das Cookie, das das gesperrte Fenster identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a5b57-109">The cookie that identifies the window that was revoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5b57-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5b57-110">Return value</span></span>

<span data-ttu-id="a5b57-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a5b57-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5b57-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a5b57-112">Remarks</span></span>

<span data-ttu-id="a5b57-113">Einem Fenster wird ein Cookie gewährt, wenn es als Shellfenster registriert ist.</span><span class="sxs-lookup"><span data-stu-id="a5b57-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="a5b57-114">Weitere Informationen finden Sie unter [**Registrieren von**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="a5b57-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5b57-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5b57-115">Requirements</span></span>



| <span data-ttu-id="a5b57-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5b57-116">Requirement</span></span> | <span data-ttu-id="a5b57-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a5b57-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b57-118">Produkt</span><span class="sxs-lookup"><span data-stu-id="a5b57-118">Product</span></span><br/> | <span data-ttu-id="a5b57-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="a5b57-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="a5b57-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a5b57-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="a5b57-121"><dt>Shdocvw.dll (Version 5.00.2014.0216 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="a5b57-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5b57-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5b57-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5b57-123">**DShellWindowsEvents**</span><span class="sxs-lookup"><span data-stu-id="a5b57-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="a5b57-124">**WindowRegistered**</span><span class="sxs-lookup"><span data-stu-id="a5b57-124">**WindowRegistered**</span></span>](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[<span data-ttu-id="a5b57-125">**Revoke**</span><span class="sxs-lookup"><span data-stu-id="a5b57-125">**Revoke**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




