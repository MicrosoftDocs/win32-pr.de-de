---
title: Legacysecurereferences
description: Bestimmt, ob adressf/releaseaufrufe für Anwendungen gesichert werden, die CoInitializeSecurity nicht aufrufen.
ms.assetid: 955b599b-1858-475a-95c4-a55038a28e69
keywords:
- Legacysecurereferences-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2776bf3661013f1e622bbc2e1c553f2551c62808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341863"
---
# <a name="legacysecurereferences"></a><span data-ttu-id="9ab14-104">Legacysecurereferences</span><span class="sxs-lookup"><span data-stu-id="9ab14-104">LegacySecureReferences</span></span>

<span data-ttu-id="9ab14-105">Bestimmt, ob **adressf**- / **releaseaufrufe** für Anwendungen gesichert werden, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9ab14-105">Determines whether **AddRef**/**Release** invocations are secured for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="9ab14-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="9ab14-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   LegacySecureReferences = value
```

## <a name="remarks"></a><span data-ttu-id="9ab14-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ab14-107">Remarks</span></span>

<span data-ttu-id="9ab14-108">Dies ist ein **reg \_ SZ** -Wert.</span><span class="sxs-lookup"><span data-stu-id="9ab14-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="9ab14-109">Der Wert "y" oder "y" zeigt an, dass **adressf** und **Release** gesichert sind.</span><span class="sxs-lookup"><span data-stu-id="9ab14-109">A value of 'Y' or 'y' indicate that **AddRef** and **Release** are secured.</span></span> <span data-ttu-id="9ab14-110">Wenn dieser Registrierungs Wert nicht vorhanden ist oder auf einen anderen Wert als ' y ' oder ' y ' festgelegt ist, werden **adressf** und **Release** nicht gesichert.</span><span class="sxs-lookup"><span data-stu-id="9ab14-110">If this registry value is not present or is set to a value other than 'Y' or 'y', **AddRef** and **Release** are not secured.</span></span> <span data-ttu-id="9ab14-111">Durch das Aktivieren sicherer Verweise werden Remote Aufrufe verlangsamt.</span><span class="sxs-lookup"><span data-stu-id="9ab14-111">Enabling secure references slows remote calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ab14-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9ab14-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ab14-113">Registrieren von com-Servern</span><span class="sxs-lookup"><span data-stu-id="9ab14-113">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="9ab14-114">Festlegen der Prozess weiten Sicherheit</span><span class="sxs-lookup"><span data-stu-id="9ab14-114">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




