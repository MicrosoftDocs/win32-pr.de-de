---
title: Ändern der Sicherheits Standardwerte für einen Computer
description: Ändern der Sicherheits Standardwerte für einen Computer
ms.assetid: c6d84375-59ea-42d5-87f9-af514b6f7d7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e7a17e7db1f8852dff42e62384c730090bbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387950"
---
# <a name="modifying-the-security-defaults-for-a-computer"></a><span data-ttu-id="77b86-103">Ändern der Sicherheits Standardwerte für einen Computer</span><span class="sxs-lookup"><span data-stu-id="77b86-103">Modifying the Security Defaults for a Computer</span></span>

<span data-ttu-id="77b86-104">Es wird nicht empfohlen, die systemweiten Sicherheitseinstellungen zu ändern, da dies Auswirkungen auf alle com-Server Anwendungen hat, die nicht Ihre eigene Prozess weite Sicherheit festlegen, und möglicherweise verhindern, dass Sie ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="77b86-104">It is not recommended that you change the system-wide security settings, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="77b86-105">Wenn Sie die systemweiten Sicherheitseinstellungen ändern, um die Sicherheitseinstellungen für eine bestimmte COM-Anwendung zu beeinflussen, sollten Sie stattdessen die Prozess weiten Sicherheitseinstellungen für die jeweilige COM-Anwendung ändern.</span><span class="sxs-lookup"><span data-stu-id="77b86-105">If you are changing the system-wide security settings to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="77b86-106">Weitere Informationen zum Festlegen der Prozess weiten Sicherheit finden Sie unter [Setting Process-Wide Security](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="77b86-106">For more information about setting process-wide security, see [Setting Process-Wide Security](setting-processwide-security.md).</span></span>

<span data-ttu-id="77b86-107">Bestimmte Werte in der Registrierung bestimmen die Sicherheitseinstellungen für Anwendungen, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="77b86-107">Certain values in the registry determine security settings for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="77b86-108">Sie können diese Einstellungen mit Dcomcnfg.exe ändern.</span><span class="sxs-lookup"><span data-stu-id="77b86-108">You can modify these settings using Dcomcnfg.exe.</span></span>

<span data-ttu-id="77b86-109">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="77b86-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="77b86-110">Registrierungs Werte für die System-Wide Sicherheit</span><span class="sxs-lookup"><span data-stu-id="77b86-110">Registry Values for System-Wide Security</span></span>](registry-values-for-machine-wide-security.md)
-   [<span data-ttu-id="77b86-111">Festlegen der System-Wide Sicherheit mithilfe von DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="77b86-111">Setting System-Wide Security Using DCOMCNFG</span></span>](setting-machine-wide-security-using-dcomcnfg.md)

## <a name="related-topics"></a><span data-ttu-id="77b86-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="77b86-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77b86-113">Festlegen der Prozess weiten Sicherheit</span><span class="sxs-lookup"><span data-stu-id="77b86-113">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> <dt>

[<span data-ttu-id="77b86-114">Festlegen der Sicherheit für COM-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="77b86-114">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




