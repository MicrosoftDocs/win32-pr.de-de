---
title: AuthenticationLevel
description: Legt die Authentifizierungs Ebene für Anwendungen fest, die CoInitializeSecurity nicht aufzurufen, oder für Anwendungen, die CoInitializeSecurity anrufen und eine AppID angeben.
ms.assetid: 137cbffe-6f45-43f4-bf35-b064b3607fcc
keywords:
- Registrierungs Wert "AuthenticationLevel" com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 697b04bcf4992c8a6943bcb515fa0a4eae616fec
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311507"
---
# <a name="authenticationlevel"></a><span data-ttu-id="f2cac-104">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="f2cac-104">AuthenticationLevel</span></span>

<span data-ttu-id="f2cac-105">Legt die Authentifizierungs Ebene für Anwendungen fest, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) nicht aufzurufen, oder für Anwendungen, die **CoInitializeSecurity** anrufen und eine AppID angeben.</span><span class="sxs-lookup"><span data-stu-id="f2cac-105">Sets the authentication level for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) or for applications that call **CoInitializeSecurity** and specify an AppID.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="f2cac-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="f2cac-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AuthenticationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="f2cac-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2cac-107">Remarks</span></span>

<span data-ttu-id="f2cac-108">Dies ist ein **reg \_ DWORD** -Wert, der den Konstanten der RPC- \_ C- \_ authn- \_ Ebene entspricht.</span><span class="sxs-lookup"><span data-stu-id="f2cac-108">This is a **REG\_DWORD** value that is equivalent to the RPC\_C\_AUTHN\_LEVEL constants.</span></span>



| <span data-ttu-id="f2cac-109">Wert</span><span class="sxs-lookup"><span data-stu-id="f2cac-109">Value</span></span> | <span data-ttu-id="f2cac-110">Konstante</span><span class="sxs-lookup"><span data-stu-id="f2cac-110">Constant</span></span>                             |
|-------|--------------------------------------|
| <span data-ttu-id="f2cac-111">1</span><span class="sxs-lookup"><span data-stu-id="f2cac-111">1</span></span>     | <span data-ttu-id="f2cac-112">RPC- \_ C- \_ authn- \_ Ebene \_ None</span><span class="sxs-lookup"><span data-stu-id="f2cac-112">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           |
| <span data-ttu-id="f2cac-113">2</span><span class="sxs-lookup"><span data-stu-id="f2cac-113">2</span></span>     | <span data-ttu-id="f2cac-114">RPC- \_ C \_ authn \_ Level \_ Connect</span><span class="sxs-lookup"><span data-stu-id="f2cac-114">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        |
| <span data-ttu-id="f2cac-115">3</span><span class="sxs-lookup"><span data-stu-id="f2cac-115">3</span></span>     | <span data-ttu-id="f2cac-116">RPC- \_ C \_ authn-Ebene- \_ \_ Aufruf</span><span class="sxs-lookup"><span data-stu-id="f2cac-116">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           |
| <span data-ttu-id="f2cac-117">4</span><span class="sxs-lookup"><span data-stu-id="f2cac-117">4</span></span>     | <span data-ttu-id="f2cac-118">Pkt der RPC- \_ C- \_ authn- \_ Ebene \_</span><span class="sxs-lookup"><span data-stu-id="f2cac-118">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            |
| <span data-ttu-id="f2cac-119">5</span><span class="sxs-lookup"><span data-stu-id="f2cac-119">5</span></span>     | <span data-ttu-id="f2cac-120">\_Pkt-Integrität der RPC C- \_ authn- \_ Ebene \_ \_</span><span class="sxs-lookup"><span data-stu-id="f2cac-120">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> |
| <span data-ttu-id="f2cac-121">6</span><span class="sxs-lookup"><span data-stu-id="f2cac-121">6</span></span>     | <span data-ttu-id="f2cac-122">\_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene</span><span class="sxs-lookup"><span data-stu-id="f2cac-122">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   |



 

<span data-ttu-id="f2cac-123">Der Wert **AuthenticationLevel** ähnelt dem Wert von [**legacyauthenticationlevel**](legacyauthenticationlevel.md) .</span><span class="sxs-lookup"><span data-stu-id="f2cac-123">The **AuthenticationLevel** value is similar to the [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) value.</span></span> <span data-ttu-id="f2cac-124">Wenn der **AuthenticationLevel** -Wert vorhanden ist, wird er anstelle des **legacyauthenticationlevel** -Werts für diese AppID verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2cac-124">If the **AuthenticationLevel** value is present, it is used instead of the **LegacyAuthenticationLevel** value for that AppID.</span></span>

<span data-ttu-id="f2cac-125">Wenn der **AuthenticationLevel** -Wert vom falschen Typ oder außerhalb des gültigen Bereichs ist, schlägt [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) fehl, wodurch das Marshalling der Schnittstelle fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="f2cac-125">If the **AuthenticationLevel** value is of the wrong type or out of range, [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) fails, causing interface marshaling to fail.</span></span> <span data-ttu-id="f2cac-126">Dadurch wird verhindert, dass die Anwendung überhaupt Aufrufe durchführen kann (Apartment übergreifend, Thread übergreifend, Prozess übergreifend oder Computer übergreifend).</span><span class="sxs-lookup"><span data-stu-id="f2cac-126">This prevents the application from making any calls at all (cross-apartment, cross-thread, cross-process, or cross-computer).</span></span>

<span data-ttu-id="f2cac-127">Die Werte " **AuthenticationLevel** " und " [**AccessPermission**](accesspermission.md) " sind unabhängig voneinander.</span><span class="sxs-lookup"><span data-stu-id="f2cac-127">The **AuthenticationLevel** and [**AccessPermission**](accesspermission.md) values are independent.</span></span> <span data-ttu-id="f2cac-128">Wenn kein Wert vorhanden ist, wird der Standardwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2cac-128">If one is not present, the default is used.</span></span> <span data-ttu-id="f2cac-129">In den folgenden Regeln wird die Interaktion zwischen dem Wert **AuthenticationLevel** und dem **AccessPermission** -Wert aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="f2cac-129">The following rules list the interaction between the **AuthenticationLevel** value and the **AccessPermission** value:</span></span>

-   <span data-ttu-id="f2cac-130">Wenn **AuthenticationLevel** den Wert None hat, werden die Werte [**AccessPermission**](accesspermission.md) und [**DefaultAccessPermission**](defaultaccesspermission.md) ignoriert (für diese Anwendung).</span><span class="sxs-lookup"><span data-stu-id="f2cac-130">If the **AuthenticationLevel** is NONE, the [**AccessPermission**](accesspermission.md) and [**DefaultAccessPermission**](defaultaccesspermission.md) values are ignored (for that application).</span></span>
-   <span data-ttu-id="f2cac-131">Wenn " **AuthenticationLevel** " nicht vorhanden ist und " [**legacyauthenticationlevel**](legacyauthenticationlevel.md) " auf "None" festgelegt ist, werden die Werte [**AccessPermission**](accesspermission.md) und [**DefaultAccessPermission**](defaultaccesspermission.md) ignoriert (für diese Anwendung).</span><span class="sxs-lookup"><span data-stu-id="f2cac-131">If the **AuthenticationLevel** is not present and the [**LegacyAuthenticationLevel**](legacyauthenticationlevel.md) is NONE, the [**AccessPermission**](accesspermission.md) and [**DefaultAccessPermission**](defaultaccesspermission.md) values are ignored (for that application).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2cac-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2cac-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2cac-133">Konstanten auf Authentifizierungs Ebene</span><span class="sxs-lookup"><span data-stu-id="f2cac-133">Authentication Level Constants</span></span>](com-authentication-level-constants.md)
</dt> <dt>

[<span data-ttu-id="f2cac-134">**Legacyauthenticationlevel**</span><span class="sxs-lookup"><span data-stu-id="f2cac-134">**LegacyAuthenticationLevel**</span></span>](legacyauthenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="f2cac-135">Registrieren von com-Servern</span><span class="sxs-lookup"><span data-stu-id="f2cac-135">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="f2cac-136">Sicherheit in com</span><span class="sxs-lookup"><span data-stu-id="f2cac-136">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




