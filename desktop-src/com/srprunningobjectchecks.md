---
title: Srprunningobjectchecks
description: Bestimmt, ob Verbindungsversuche mit ausgelaufenden Objekten auf kompatible Richtlinien für Software Einschränkungs Richtlinien (SRP) überprüft werden.
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- Srprunningobjectchecks-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad307856bcfdd30cfaa6c731551ac6570d2bec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709431"
---
# <a name="srprunningobjectchecks"></a><span data-ttu-id="2311c-104">Srprunningobjectchecks</span><span class="sxs-lookup"><span data-stu-id="2311c-104">SRPRunningObjectChecks</span></span>

<span data-ttu-id="2311c-105">Bestimmt, ob Verbindungsversuche mit ausgelaufenden Objekten auf kompatible Richtlinien für Software Einschränkungs Richtlinien (SRP) überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="2311c-105">Determines whether attempts to connect to running objects are screened for compatible software restriction policy (SRP) trust levels.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="2311c-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="2311c-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a><span data-ttu-id="2311c-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2311c-107">Remarks</span></span>

<span data-ttu-id="2311c-108">Dies ist ein **reg \_ SZ** -Wert.</span><span class="sxs-lookup"><span data-stu-id="2311c-108">This is a **REG\_SZ** value.</span></span>

<span data-ttu-id="2311c-109">Zeichen folgen Werte ({N, n, Nein, Nein, Nein}) geben an, dass Verbindungsversuche mit ausgelaufenden Objekten nicht auf kompatible SRP-Vertrauens Ebenen überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="2311c-109">String values of {N, n, NO, No, no} indicate that attempts to connect to running objects are not screened for compatible SRP trust levels.</span></span> <span data-ttu-id="2311c-110">Wenn dieser Registrierungs Wert auf einen anderen Wert festgelegt ist oder nicht vorhanden ist, kann das laufende Objekt nicht über eine weniger strenge SRP-Vertrauens Ebene verfügen als das Client Objekt.</span><span class="sxs-lookup"><span data-stu-id="2311c-110">If this registry value is set to any other value or does not exist, the running object cannot have a less stringent SRP trust level than the client object.</span></span> <span data-ttu-id="2311c-111">Beispielsweise kann das laufende Objekt nicht über eine unzulässige Vertrauens Ebene verfügen, wenn das Client Objekt eine uneingeschränkte Vertrauens Ebene aufweist.</span><span class="sxs-lookup"><span data-stu-id="2311c-111">For example, the running object cannot have a Disallowed trust level if the client object has an Unrestricted trust level.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2311c-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2311c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2311c-113">SRPTrustLevel</span><span class="sxs-lookup"><span data-stu-id="2311c-113">SRPTrustLevel</span></span>](srptrustlevel.md)
</dt> </dl>

 

 




