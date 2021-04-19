---
title: DefaultLaunchPermission
description: Definiert die Access Control Liste (ACL) der Prinzipale, die Klassen starten können, die nicht Ihre eigene ACL über den Registrierungs Wert launchberechtigungstyp angeben.
ms.assetid: 23ca87fc-7829-46a9-9fc3-2cd7f677bbff
keywords:
- Defaultlaunchberechtigungs-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599a0993a4a1238e57e357f428f7046331412cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342090"
---
# <a name="defaultlaunchpermission"></a><span data-ttu-id="af3c7-104">DefaultLaunchPermission</span><span class="sxs-lookup"><span data-stu-id="af3c7-104">DefaultLaunchPermission</span></span>

<span data-ttu-id="af3c7-105">Definiert die Access Control Liste (ACL) der Prinzipale, die Klassen starten können, die nicht Ihre eigene ACL über den Registrierungs Wert [**launchberechtigungstyp**](launchpermission.md) angeben.</span><span class="sxs-lookup"><span data-stu-id="af3c7-105">Defines the Access Control List (ACL) of the principals that can launch classes that do not specify their own ACL through the [**LaunchPermission**](launchpermission.md) registry value.</span></span>

> [!Caution]  
> <span data-ttu-id="af3c7-106">Es wird nicht empfohlen, diesen Wert zu ändern, da dies Auswirkungen auf alle com-Server Anwendungen hat, die nicht Ihre eigene Prozess weite Sicherheit festlegen, und möglicherweise verhindern, dass Sie ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="af3c7-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="af3c7-107">Wenn Sie diesen Wert ändern, um die Sicherheitseinstellungen für eine bestimmte COM-Anwendung zu beeinflussen, sollten Sie stattdessen die Prozess weiten Sicherheitseinstellungen für die jeweilige COM-Anwendung ändern.</span><span class="sxs-lookup"><span data-stu-id="af3c7-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="af3c7-108">Weitere Informationen zum Festlegen der Prozess weiten Sicherheit finden Sie unter [Festlegen der Prozess weiten Sicherheit](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="af3c7-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="af3c7-109">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="af3c7-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultLaunchPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="af3c7-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="af3c7-110">Remarks</span></span>

<span data-ttu-id="af3c7-111">Dies ist ein **reg- \_ Binärwert** .</span><span class="sxs-lookup"><span data-stu-id="af3c7-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="af3c7-112">Die Standard Zugriffsberechtigungen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="af3c7-112">The default access permissions are as follows:</span></span>

-   <span data-ttu-id="af3c7-113">Administratoren: Start zulassen</span><span class="sxs-lookup"><span data-stu-id="af3c7-113">Administrators: allow launch</span></span>
-   <span data-ttu-id="af3c7-114">System: Start zulassen</span><span class="sxs-lookup"><span data-stu-id="af3c7-114">SYSTEM: allow launch</span></span>
-   <span data-ttu-id="af3c7-115">Interaktiv: Start zulassen</span><span class="sxs-lookup"><span data-stu-id="af3c7-115">INTERACTIVE: allow launch</span></span>

<span data-ttu-id="af3c7-116">Wenn der [**launchberechtigungswert**](launchpermission.md) für einen Server festgelegt ist, hat er Vorrang vor dem **defaultlaunchberechtigungswert** .</span><span class="sxs-lookup"><span data-stu-id="af3c7-116">If the [**LaunchPermission**](launchpermission.md) value is set for a server, it takes precedence over the **DefaultLaunchPermission** value.</span></span> <span data-ttu-id="af3c7-117">Wenn eine lokale oder eine Remote Anforderung zum Starten eines Servers empfangen wird, dessen [**AppID**](appid-key.md) -Schlüssel keinen eigenen **launchberechtigungswert** hat, wird die durch diesen Wert beschriebene ACL während der Identität des Clients aktiviert, und Ihr Erfolg ermöglicht das Starten des Klassen Codes entweder oder nicht.</span><span class="sxs-lookup"><span data-stu-id="af3c7-117">Upon receiving a local or remote request to launch a server whose [**AppID**](appid-key.md) key has no **LaunchPermission** value of its own, the ACL described by this value is checked while impersonating the client and its success either allows or disallows the launching of the class code.</span></span>

<span data-ttu-id="af3c7-118">Dieser Wert stellt eine einfache Ebene der zentralisierten Verwaltung des standardmäßigen Zugriffs Zugriffs auf ansonsten nicht verwaltete Klassen auf einem Computer bereit.</span><span class="sxs-lookup"><span data-stu-id="af3c7-118">This value provides a simple level of centralized administration of the default launching access to otherwise unadministered classes on a computer.</span></span> <span data-ttu-id="af3c7-119">Ein Administrator kann z. b. das DCOMCNFG-Tool verwenden, um das System so zu konfigurieren, dass es den schreibgeschützten Zugriff für Poweruser zulässt.</span><span class="sxs-lookup"><span data-stu-id="af3c7-119">For example, an administrator might use the DCOMCNFG tool to configure the system to allow read-only access for Power Users.</span></span> <span data-ttu-id="af3c7-120">OLE schränkt daher Anforderungen zum Starten von Klassen Code für Mitglieder der Hauptbenutzer Gruppe ein.</span><span class="sxs-lookup"><span data-stu-id="af3c7-120">OLE would therefore restrict requests to launch class code to members of the Power Users group.</span></span> <span data-ttu-id="af3c7-121">Ein Administrator kann anschließend Start Berechtigungen für einzelne Klassen konfigurieren, um die Möglichkeit zu erteilen, bei Bedarf Klassen Code für andere Gruppen oder einzelne Benutzer zu starten.</span><span class="sxs-lookup"><span data-stu-id="af3c7-121">An administrator could subsequently configure launch permissions for individual classes to grant the ability to launch class code to other groups or individual users as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af3c7-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af3c7-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af3c7-123">**Launchberechtigung**</span><span class="sxs-lookup"><span data-stu-id="af3c7-123">**LaunchPermission**</span></span>](launchpermission.md)
</dt> <dt>

[<span data-ttu-id="af3c7-124">Registrieren von com-Servern</span><span class="sxs-lookup"><span data-stu-id="af3c7-124">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="af3c7-125">Festlegen der Prozess weiten Sicherheit</span><span class="sxs-lookup"><span data-stu-id="af3c7-125">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




