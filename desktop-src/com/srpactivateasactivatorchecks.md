---
title: Srpactivateasactivatorchecks
description: Bestimmt, ob die Richtlinien für die Software Einschränkungs Richtlinie (SRP) während der Aktivierungen von activateasactivator verwendet werden.
ms.assetid: b0d616c3-1cb0-4854-a4f9-6635d61b0698
keywords:
- Srpactivateasactivatorchecks-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b66ae6b1c7f267f48f24441c04e95eea75e4345
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709432"
---
# <a name="srpactivateasactivatorchecks"></a><span data-ttu-id="6a8f0-104">Srpactivateasactivatorchecks</span><span class="sxs-lookup"><span data-stu-id="6a8f0-104">SRPActivateAsActivatorChecks</span></span>

<span data-ttu-id="6a8f0-105">Bestimmt, ob die Richtlinien für die Software Einschränkungs Richtlinie (SRP) während der Aktivierungen von activateasactivator verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a8f0-105">Determines whether software restriction policy (SRP) trust levels are used during ActivateAsActivator activations.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="6a8f0-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="6a8f0-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPActivateAsActivatorChecks = value
```

## <a name="remarks"></a><span data-ttu-id="6a8f0-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a8f0-107">Remarks</span></span>

<span data-ttu-id="6a8f0-108">Dies ist ein **reg \_ SZ** -Wert.</span><span class="sxs-lookup"><span data-stu-id="6a8f0-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="6a8f0-109">Zeichen folgen Werte ({N, n, Nein, Nein, Nein}) geben an, dass das Server Objekt mit der SRP-Vertrauens Ebene des Client Objekts ausgeführt wird, unabhängig von der SRP-Vertrauens Ebene, mit der es konfiguriert wurde.</span><span class="sxs-lookup"><span data-stu-id="6a8f0-109">String values of {N, n, NO, No, no} indicate that the server object runs with the SRP trust level of the client object, regardless of the SRP trust level with which it was configured.</span></span> <span data-ttu-id="6a8f0-110">Wenn dieser Registrierungs Wert auf einen anderen Wert festgelegt ist oder nicht vorhanden ist, wird die für das Server Objekt konfigurierte SRP-Vertrauens Ebene mit der SRP-Vertrauens Ebene des Client Objekts verglichen, und es wird die strengere Vertrauens Ebene zum Ausführen des Server Objekts verwendet.</span><span class="sxs-lookup"><span data-stu-id="6a8f0-110">If this registry value is set to any other value or does not exist, the SRP trust level that is configured for the server object is compared with the SRP trust level of the client object and that the more stringent trust level is used to run the server object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a8f0-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6a8f0-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a8f0-112">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="6a8f0-112">SRPTrustLevel</span></span>](srptrustlevel.md)
</dt> </dl>

 

 




