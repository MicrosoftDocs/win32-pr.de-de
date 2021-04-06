---
title: Registrierungs Werte für die System-Wide Sicherheit
description: Registrierungs Werte für die System-Wide Sicherheit
ms.assetid: f1db42b8-4328-4b39-b87f-583382395235
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7addfb59bd8074a5a1392e5f74f9cee73d64f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947577"
---
# <a name="registry-values-for-system-wide-security"></a><span data-ttu-id="e9649-103">Registrierungs Werte für die System-Wide Sicherheit</span><span class="sxs-lookup"><span data-stu-id="e9649-103">Registry Values for System-Wide Security</span></span>

<span data-ttu-id="e9649-104">Es wird nicht empfohlen, die systemweiten Sicherheitseinstellungen zu ändern, da dies Auswirkungen auf alle com-Server Anwendungen hat, die nicht Ihre eigene Prozess weite Sicherheit festlegen, und möglicherweise verhindern, dass Sie ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="e9649-104">It is not recommended that you change the system-wide security settings, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="e9649-105">Wenn Sie die systemweiten Sicherheitseinstellungen ändern, um die Sicherheitseinstellungen für eine bestimmte COM-Anwendung zu beeinflussen, sollten Sie stattdessen die Prozess weiten Sicherheitseinstellungen für die jeweilige COM-Anwendung ändern.</span><span class="sxs-lookup"><span data-stu-id="e9649-105">If you are changing the system-wide security settings to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="e9649-106">Weitere Informationen zum Festlegen der Prozess weiten Sicherheit finden Sie unter [Setting Process-Wide Security](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="e9649-106">For more information about setting process-wide security, see [Setting Process-Wide Security](setting-processwide-security.md).</span></span>

<span data-ttu-id="e9649-107">Bestimmte Werte in der Registrierung werden verwendet, um Sicherheitseinstellungen für Anwendungen zu ermitteln, die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="e9649-107">Certain values in the registry are used to determine security settings for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="e9649-108">Sie können Dcomcnfg.exe verwenden, um diese Standard Sicherheitseinstellungen für einen Computer zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e9649-108">You can use Dcomcnfg.exe to modify these default security settings for a computer.</span></span> <span data-ttu-id="e9649-109">Schritt-für-Schritt-Anleitungen, in denen beschrieben wird, wie Sie Dcomcnfg.exe zu diesem Zweck verwenden, finden [Sie unter Festlegen der System-Wide Sicherheit mithilfe von DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span><span class="sxs-lookup"><span data-stu-id="e9649-109">For step-by-step procedures that describe how to use Dcomcnfg.exe for this purpose, see [Setting System-Wide Security Using DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span></span>

<span data-ttu-id="e9649-110">Eine andere Möglichkeit zum Ändern der systemweiten Standardeinstellungen besteht darin, Registrierungs Werte direkt zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e9649-110">Another way to change default system-wide settings is to manipulate registry values directly.</span></span> <span data-ttu-id="e9649-111">Allerdings verfügen nur Administratoren und das System über Vollzugriff auf den Teil der Registrierung, der die Standardeinstellungen für das systemweite Aufrufen der Sicherheit enthält.</span><span class="sxs-lookup"><span data-stu-id="e9649-111">However, only administrators and the system have full access to the portion of the registry that contains the default system-wide call-security settings.</span></span> <span data-ttu-id="e9649-112">Alle anderen Benutzer verfügen nur über Lesezugriff.</span><span class="sxs-lookup"><span data-stu-id="e9649-112">All other users have read-access only.</span></span>

<span data-ttu-id="e9649-113">Die benannten Werte, die sich auf systemweite Sicherheitsstandards auswirken, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="e9649-113">The named values that affect system-wide security defaults are as follows:</span></span>

-   [<span data-ttu-id="e9649-114">DefaultLaunchPermission</span><span class="sxs-lookup"><span data-stu-id="e9649-114">DefaultLaunchPermission</span></span>](defaultlaunchpermission.md)
-   [<span data-ttu-id="e9649-115">DefaultAccessPermission</span><span class="sxs-lookup"><span data-stu-id="e9649-115">DefaultAccessPermission</span></span>](defaultaccesspermission.md)
-   [<span data-ttu-id="e9649-116">Legacyauthenticationlevel</span><span class="sxs-lookup"><span data-stu-id="e9649-116">LegacyAuthenticationLevel</span></span>](legacyauthenticationlevel.md)
-   [<span data-ttu-id="e9649-117">Legacyidentitäts ationlevel</span><span class="sxs-lookup"><span data-stu-id="e9649-117">LegacyImpersonationLevel</span></span>](legacyimpersonationlevel.md)
-   [<span data-ttu-id="e9649-118">Legacysecurereferences</span><span class="sxs-lookup"><span data-stu-id="e9649-118">LegacySecureReferences</span></span>](legacysecurereferences.md)
-   [<span data-ttu-id="e9649-119">Srprunningobjectchecks</span><span class="sxs-lookup"><span data-stu-id="e9649-119">SRPRunningObjectChecks</span></span>](srprunningobjectchecks.md)
-   [<span data-ttu-id="e9649-120">Srpactivateasactivatorchecks</span><span class="sxs-lookup"><span data-stu-id="e9649-120">SRPActivateAsActivatorChecks</span></span>](srpactivateasactivatorchecks.md)

## <a name="related-topics"></a><span data-ttu-id="e9649-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e9649-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9649-122">Festlegen Process-Wide Sicherheit</span><span class="sxs-lookup"><span data-stu-id="e9649-122">Setting Process-Wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




