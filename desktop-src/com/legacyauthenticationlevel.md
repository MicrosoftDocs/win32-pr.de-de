---
title: Legacyauthenticationlevel
description: Legt die Standard Authentifizierungs Ebene für Anwendungen fest, die CoInitializeSecurity nicht aufzurufen.
ms.assetid: e14d2203-c84e-46af-befd-d82ef1936c9d
keywords:
- Legacyauthenticationlevel-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d87d808287418f635629e15324f2f517619be6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037612"
---
# <a name="legacyauthenticationlevel"></a><span data-ttu-id="95a93-104">Legacyauthenticationlevel</span><span class="sxs-lookup"><span data-stu-id="95a93-104">LegacyAuthenticationLevel</span></span>

<span data-ttu-id="95a93-105">Legt die Standard Authentifizierungs Ebene für Anwendungen fest, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="95a93-105">Sets the default authentication level for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

> [!Caution]  
> <span data-ttu-id="95a93-106">Es wird nicht empfohlen, diesen Wert zu ändern, da dies Auswirkungen auf alle com-Server Anwendungen hat, die nicht Ihre eigene Prozess weite Sicherheit festlegen, und möglicherweise verhindern, dass Sie ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="95a93-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="95a93-107">Wenn Sie diesen Wert ändern, um die Sicherheitseinstellungen für eine bestimmte COM-Anwendung zu beeinflussen, sollten Sie stattdessen die Prozess weiten Sicherheitseinstellungen für die jeweilige COM-Anwendung ändern.</span><span class="sxs-lookup"><span data-stu-id="95a93-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="95a93-108">Weitere Informationen zum Festlegen der Prozess weiten Sicherheit finden Sie unter [Festlegen der Prozess weiten Sicherheit](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="95a93-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="95a93-109">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="95a93-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyAuthenticationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="95a93-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95a93-110">Remarks</span></span>

<span data-ttu-id="95a93-111">Dies ist ein **reg \_ Word** -Wert, der den Konstanten der RPC- \_ C- \_ authn- \_ Ebene entspricht.</span><span class="sxs-lookup"><span data-stu-id="95a93-111">This is a **REG\_WORD** value that is equivalent to the RPC\_C\_AUTHN\_LEVEL constants.</span></span>



| <span data-ttu-id="95a93-112">Wert</span><span class="sxs-lookup"><span data-stu-id="95a93-112">Value</span></span> | <span data-ttu-id="95a93-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="95a93-113">Constant</span></span>                             |
|-------|--------------------------------------|
| <span data-ttu-id="95a93-114">1</span><span class="sxs-lookup"><span data-stu-id="95a93-114">1</span></span>     | <span data-ttu-id="95a93-115">RPC- \_ C- \_ authn- \_ Ebene \_ None</span><span class="sxs-lookup"><span data-stu-id="95a93-115">RPC\_C\_AUTHN\_LEVEL\_NONE</span></span>           |
| <span data-ttu-id="95a93-116">2</span><span class="sxs-lookup"><span data-stu-id="95a93-116">2</span></span>     | <span data-ttu-id="95a93-117">RPC- \_ C \_ authn \_ Level \_ Connect</span><span class="sxs-lookup"><span data-stu-id="95a93-117">RPC\_C\_AUTHN\_LEVEL\_CONNECT</span></span>        |
| <span data-ttu-id="95a93-118">3</span><span class="sxs-lookup"><span data-stu-id="95a93-118">3</span></span>     | <span data-ttu-id="95a93-119">RPC- \_ C \_ authn-Ebene- \_ \_ Aufruf</span><span class="sxs-lookup"><span data-stu-id="95a93-119">RPC\_C\_AUTHN\_LEVEL\_CALL</span></span>           |
| <span data-ttu-id="95a93-120">4</span><span class="sxs-lookup"><span data-stu-id="95a93-120">4</span></span>     | <span data-ttu-id="95a93-121">Pkt der RPC- \_ C- \_ authn- \_ Ebene \_</span><span class="sxs-lookup"><span data-stu-id="95a93-121">RPC\_C\_AUTHN\_LEVEL\_PKT</span></span>            |
| <span data-ttu-id="95a93-122">5</span><span class="sxs-lookup"><span data-stu-id="95a93-122">5</span></span>     | <span data-ttu-id="95a93-123">\_Pkt-Integrität der RPC C- \_ authn- \_ Ebene \_ \_</span><span class="sxs-lookup"><span data-stu-id="95a93-123">RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY</span></span> |
| <span data-ttu-id="95a93-124">6</span><span class="sxs-lookup"><span data-stu-id="95a93-124">6</span></span>     | <span data-ttu-id="95a93-125">\_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene</span><span class="sxs-lookup"><span data-stu-id="95a93-125">RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY</span></span>   |



 

<span data-ttu-id="95a93-126">Wenn dieser Registrierungs Wert nicht vorhanden ist, ist die vom System festgelegte Standard Authentifizierungs Ebene 2 (RPC \_ C \_ authn \_ Connect).</span><span class="sxs-lookup"><span data-stu-id="95a93-126">If this registry value is not present, the default authentication level established by the system is 2 (RPC\_C\_AUTHN\_CONNECT).</span></span>

## <a name="related-topics"></a><span data-ttu-id="95a93-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="95a93-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95a93-128">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="95a93-128">**AuthenticationLevel**</span></span>](authenticationlevel.md)
</dt> <dt>

[<span data-ttu-id="95a93-129">Registrieren von com-Servern</span><span class="sxs-lookup"><span data-stu-id="95a93-129">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="95a93-130">Festlegen der Prozess weiten Sicherheit</span><span class="sxs-lookup"><span data-stu-id="95a93-130">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




