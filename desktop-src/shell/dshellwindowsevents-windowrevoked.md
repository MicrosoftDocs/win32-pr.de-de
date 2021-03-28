---
description: Wird aufgerufen, wenn die Registrierung eines shellfensters widerrufen wird.
title: Dshellwindowsvents. windowwiderruf-Methode
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
ms.openlocfilehash: b036bdde2916c2fa037d1b6e286a2096d9e1d8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983084"
---
# <a name="dshellwindowseventswindowrevoked-method"></a><span data-ttu-id="ac67a-103">Dshellwindowsvents. windowwiderruf-Methode</span><span class="sxs-lookup"><span data-stu-id="ac67a-103">DShellWindowsEvents.WindowRevoked method</span></span>

<span data-ttu-id="ac67a-104">Wird aufgerufen, wenn die Registrierung eines shellfensters widerrufen wird.</span><span class="sxs-lookup"><span data-stu-id="ac67a-104">Called when a Shell window's registration is revoked.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac67a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac67a-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="ac67a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac67a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac67a-107">*lcookie* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ac67a-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac67a-108">Type: **Integer**</span><span class="sxs-lookup"><span data-stu-id="ac67a-108">Type: **Integer**</span></span>

<span data-ttu-id="ac67a-109">Das Cookie, das das Fenster identifiziert, das widerrufen wurde.</span><span class="sxs-lookup"><span data-stu-id="ac67a-109">The cookie that identifies the window that was revoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac67a-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ac67a-110">Return value</span></span>

<span data-ttu-id="ac67a-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ac67a-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac67a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ac67a-112">Remarks</span></span>

<span data-ttu-id="ac67a-113">Einem Fenster wird ein Cookie erteilt, wenn es als Shellfenster registriert wird.</span><span class="sxs-lookup"><span data-stu-id="ac67a-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="ac67a-114">Weitere Informationen finden Sie unter [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="ac67a-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac67a-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ac67a-115">Requirements</span></span>



| <span data-ttu-id="ac67a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ac67a-116">Requirement</span></span> | <span data-ttu-id="ac67a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="ac67a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac67a-118">Produkt</span><span class="sxs-lookup"><span data-stu-id="ac67a-118">Product</span></span><br/> | <span data-ttu-id="ac67a-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="ac67a-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="ac67a-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ac67a-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="ac67a-121"><dt>Shdocvw.dll (Version 5.00.2014.0216 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="ac67a-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac67a-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ac67a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac67a-123">**Dshellwindowgvents**</span><span class="sxs-lookup"><span data-stu-id="ac67a-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="ac67a-124">**Windowregistered**</span><span class="sxs-lookup"><span data-stu-id="ac67a-124">**WindowRegistered**</span></span>](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[<span data-ttu-id="ac67a-125">**Revoke**</span><span class="sxs-lookup"><span data-stu-id="ac67a-125">**Revoke**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




