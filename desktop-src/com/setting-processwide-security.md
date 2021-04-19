---
title: Festlegen Process-Wide Sicherheit
description: Es gibt mehrere Möglichkeiten, die Prozess weite Sicherheit festzulegen.
ms.assetid: 596ba257-cbde-4243-aa29-78749304867a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc483bc6f52963eadc12891e657db1cbe51fb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338625"
---
# <a name="setting-process-wide-security"></a><span data-ttu-id="0d97f-103">Festlegen Process-Wide Sicherheit</span><span class="sxs-lookup"><span data-stu-id="0d97f-103">Setting Process-Wide Security</span></span>

<span data-ttu-id="0d97f-104">Es gibt mehrere Möglichkeiten, die Prozess weite Sicherheit festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0d97f-104">There are several ways to set process-wide security.</span></span> <span data-ttu-id="0d97f-105">Die erste Möglichkeit, das Dcomcnfg.exe Tool zu verwenden, ist die einfachste Methode, da Sie keine Programmierung erfordert.</span><span class="sxs-lookup"><span data-stu-id="0d97f-105">The first way, using the Dcomcnfg.exe tool, is easiest because it requires no programming.</span></span> <span data-ttu-id="0d97f-106">Das zweite Verfahren bietet dem Programmierer mehr Kontrolle und erfordert einen [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)-Rückruf.</span><span class="sxs-lookup"><span data-stu-id="0d97f-106">The second technique offers the programmer more control, and it requires a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="0d97f-107">Eine andere Möglichkeit besteht darin, die Prozess weite Sicherheit in der Registrierung mithilfe des [AppID](appid-key.md) -Schlüssels festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0d97f-107">Another technique is to set process-wide security in the registry by using the [AppID](appid-key.md) key.</span></span>

<span data-ttu-id="0d97f-108">Weitere Informationen zu diesen Techniken finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="0d97f-108">For more information about these techniques, see the following topics:</span></span>

-   [<span data-ttu-id="0d97f-109">Festlegen der Process-Wide Sicherheit mithilfe von DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="0d97f-109">Setting Process-Wide Security Using DCOMCNFG</span></span>](setting-processwide-security-using-dcomcnfg.md)
-   [<span data-ttu-id="0d97f-110">Festlegen der Process-Wide Sicherheit mit CoInitializeSecurity</span><span class="sxs-lookup"><span data-stu-id="0d97f-110">Setting Process-Wide Security with CoInitializeSecurity</span></span>](setting-processwide-security-with-coinitializesecurity.md)
-   [<span data-ttu-id="0d97f-111">Festlegen der Process-Wide Sicherheit über die Registrierung</span><span class="sxs-lookup"><span data-stu-id="0d97f-111">Setting Process-Wide Security Through the Registry</span></span>](setting-processwide-security-through-the-registry.md)

## <a name="related-topics"></a><span data-ttu-id="0d97f-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d97f-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d97f-113">Festlegen der Sicherheit auf der Ebene des Schnittstellen Proxys</span><span class="sxs-lookup"><span data-stu-id="0d97f-113">Setting Security at the Interface Proxy Level</span></span>](setting-security-at-the-interface-proxy-level.md)
</dt> <dt>

[<span data-ttu-id="0d97f-114">Festlegen der Sicherheit für COM-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="0d97f-114">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




