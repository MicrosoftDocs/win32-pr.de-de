---
title: Legacyidentitäts ationlevel
description: Legt die Standard Ebene des Identitäts Wechsels für Anwendungen fest, die CoInitializeSecurity nicht aufzurufen.
ms.assetid: 3f42c6d7-729d-4406-9391-4bfe28f7a59d
keywords:
- Registrierungs Wert "legacyidentitäts ationlevel" com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fa00494eb71e49c35bfa37b434afc5c999e73e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337791"
---
# <a name="legacyimpersonationlevel"></a><span data-ttu-id="411d8-104">Legacyidentitäts ationlevel</span><span class="sxs-lookup"><span data-stu-id="411d8-104">LegacyImpersonationLevel</span></span>

<span data-ttu-id="411d8-105">Legt die Standard Ebene des Identitäts Wechsels für Anwendungen fest, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="411d8-105">Sets the default level of impersonation for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

> [!Caution]  
> <span data-ttu-id="411d8-106">Es wird nicht empfohlen, diesen Wert zu ändern, da dies Auswirkungen auf alle com-Server Anwendungen hat, die nicht Ihre eigene Prozess weite Sicherheit festlegen, und möglicherweise verhindern, dass Sie ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="411d8-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="411d8-107">Wenn Sie diesen Wert ändern, um die Sicherheitseinstellungen für eine bestimmte COM-Anwendung zu beeinflussen, sollten Sie stattdessen die Prozess weiten Sicherheitseinstellungen für die jeweilige COM-Anwendung ändern.</span><span class="sxs-lookup"><span data-stu-id="411d8-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="411d8-108">Weitere Informationen zum Festlegen der Prozess weiten Sicherheit finden Sie unter [Festlegen der Prozess weiten Sicherheit](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="411d8-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="411d8-109">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="411d8-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacyImpersonationLevel = value
```

## <a name="remarks"></a><span data-ttu-id="411d8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="411d8-110">Remarks</span></span>

<span data-ttu-id="411d8-111">Dies ist ein **reg \_ Word** -Wert, der den Konstanten der RPC- \_ C- \_ IMP- \_ Ebene entspricht.</span><span class="sxs-lookup"><span data-stu-id="411d8-111">This is a **REG\_WORD** value that is equivalent to the RPC\_C\_IMP\_LEVEL constants.</span></span>



| <span data-ttu-id="411d8-112">Wert</span><span class="sxs-lookup"><span data-stu-id="411d8-112">Value</span></span> | <span data-ttu-id="411d8-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="411d8-113">Constant</span></span>                        |
|-------|---------------------------------|
| <span data-ttu-id="411d8-114">1</span><span class="sxs-lookup"><span data-stu-id="411d8-114">1</span></span>     | <span data-ttu-id="411d8-115">RPC- \_ C- \_ IMP- \_ Ebene \_ Anonym</span><span class="sxs-lookup"><span data-stu-id="411d8-115">RPC\_C\_IMP\_LEVEL\_ANONYMOUS</span></span>   |
| <span data-ttu-id="411d8-116">2</span><span class="sxs-lookup"><span data-stu-id="411d8-116">2</span></span>     | <span data-ttu-id="411d8-117">RPC- \_ C- \_ IMP- \_ Stufe \_ identifizieren</span><span class="sxs-lookup"><span data-stu-id="411d8-117">RPC\_C\_IMP\_LEVEL\_IDENTIFY</span></span>    |
| <span data-ttu-id="411d8-118">3</span><span class="sxs-lookup"><span data-stu-id="411d8-118">3</span></span>     | <span data-ttu-id="411d8-119">Identitätswechsel auf RPC- \_ C- \_ \_ Ebene \_</span><span class="sxs-lookup"><span data-stu-id="411d8-119">RPC\_C\_IMP\_LEVEL\_IMPERSONATE</span></span> |
| <span data-ttu-id="411d8-120">4</span><span class="sxs-lookup"><span data-stu-id="411d8-120">4</span></span>     | <span data-ttu-id="411d8-121">RPC- \_ C- \_ IMP- \_ Stufen \_ Delegat</span><span class="sxs-lookup"><span data-stu-id="411d8-121">RPC\_C\_IMP\_LEVEL\_DELEGATE</span></span>    |



 

<span data-ttu-id="411d8-122">Wenn dieser Registrierungs Wert nicht vorhanden ist, ist die Standard Ebene des Identitäts Wechsels, die vom System festgelegt wird, 2 (RPC- \_ C- \_ Ebene- \_ Ebene \_ identifizieren).</span><span class="sxs-lookup"><span data-stu-id="411d8-122">If this registry value is not present, the default impersonation level established by the system is 2 (RPC\_C\_IMP\_LEVEL\_IDENTIFY).</span></span>

## <a name="related-topics"></a><span data-ttu-id="411d8-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="411d8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="411d8-124">Registrieren von com-Servern</span><span class="sxs-lookup"><span data-stu-id="411d8-124">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="411d8-125">Festlegen der Prozess weiten Sicherheit</span><span class="sxs-lookup"><span data-stu-id="411d8-125">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




