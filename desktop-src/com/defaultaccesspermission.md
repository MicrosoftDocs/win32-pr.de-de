---
title: DefaultAccessPermission
description: Legt die Access Control Liste (ACL) der Prinzipale fest, die auf Klassen zugreifen können, für die keine AccessPermission-Einstellung vorhanden ist.
ms.assetid: 02675d0e-a96c-476e-820e-e6ff3c2d1be1
keywords:
- DefaultAccessPermission-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c132096807b8c234259071758ebd361421f8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339184"
---
# <a name="defaultaccesspermission"></a><span data-ttu-id="0d9db-104">DefaultAccessPermission</span><span class="sxs-lookup"><span data-stu-id="0d9db-104">DefaultAccessPermission</span></span>

<span data-ttu-id="0d9db-105">Legt die Access Control Liste (ACL) der Prinzipale fest, die auf Klassen zugreifen können, für die keine [**AccessPermission**](accesspermission.md) -Einstellung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0d9db-105">Sets the Access Control List (ACL) of the principals that can access classes for which there is no [**AccessPermission**](accesspermission.md) setting.</span></span> <span data-ttu-id="0d9db-106">Diese ACL wird nur von Anwendungen verwendet, die nicht [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) und keinen **AccessPermission** -Wert unter Ihrem [**AppID**](appid-key.md) -Schlüssel haben.</span><span class="sxs-lookup"><span data-stu-id="0d9db-106">This ACL is used only by applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) and do not have an **AccessPermission** value under their [**AppID**](appid-key.md) key.</span></span>

> [!Caution]  
> <span data-ttu-id="0d9db-107">Es wird nicht empfohlen, diesen Wert zu ändern, da dies Auswirkungen auf alle com-Server Anwendungen hat, die nicht Ihre eigene Prozess weite Sicherheit festlegen, und möglicherweise verhindern, dass Sie ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="0d9db-107">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="0d9db-108">Wenn Sie diesen Wert ändern, um die Sicherheitseinstellungen für eine bestimmte COM-Anwendung zu beeinflussen, sollten Sie stattdessen die Prozess weiten Sicherheitseinstellungen für die jeweilige COM-Anwendung ändern.</span><span class="sxs-lookup"><span data-stu-id="0d9db-108">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="0d9db-109">Weitere Informationen zum Festlegen der Prozess weiten Sicherheit finden Sie unter [Festlegen der Prozess weiten Sicherheit](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="0d9db-109">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="0d9db-110">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="0d9db-110">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultAccessPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="0d9db-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d9db-111">Remarks</span></span>

<span data-ttu-id="0d9db-112">Dies ist ein **reg- \_ Binärwert** .</span><span class="sxs-lookup"><span data-stu-id="0d9db-112">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="0d9db-113">Die com-Laufzeit im Server überprüft die durch diesen Wert beschriebene ACL während der Identität des Aufrufers, der versucht, eine Verbindung mit dem Objekt herzustellen, und der Erfolg bestimmt, ob der Zugriff zugelassen oder nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="0d9db-113">The COM runtime in the server checks the ACL described by this value while impersonating the caller that is attempting to connect to the object, and its success determines whether the access is allowed or disallowed.</span></span> <span data-ttu-id="0d9db-114">Wenn die Zugriffs Überprüfung fehlschlägt, ist die Verbindung mit dem Objekt nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="0d9db-114">If the access-check fails, the connection to the object is disallowed.</span></span> <span data-ttu-id="0d9db-115">Wenn dieser benannte Wert nicht vorhanden ist, dürfen nur der Server Prinzipal und das lokale System den Server anrufen.</span><span class="sxs-lookup"><span data-stu-id="0d9db-115">If this named value does not exist, only the server principal and local system are allowed to call the server.</span></span>

<span data-ttu-id="0d9db-116">Standardmäßig enthält dieser Wert keine Einträge.</span><span class="sxs-lookup"><span data-stu-id="0d9db-116">By default, this value has no entries in it.</span></span> <span data-ttu-id="0d9db-117">Nur der Server Prinzipal und das System dürfen den Server anrufen.</span><span class="sxs-lookup"><span data-stu-id="0d9db-117">Only the server principal and system are allowed to call the server.</span></span>

<span data-ttu-id="0d9db-118">Dieser Wert bietet eine einfache Ebene der zentralisierten Verwaltung des Standard Verbindungs Zugriffs auf die Ausführung von Objekten auf einem Computer.</span><span class="sxs-lookup"><span data-stu-id="0d9db-118">This value provides a simple level of centralized administration of the default connection access to running objects on a computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d9db-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0d9db-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d9db-120">**Access spermission**</span><span class="sxs-lookup"><span data-stu-id="0d9db-120">**AccessPermission**</span></span>](accesspermission.md)
</dt> <dt>

[<span data-ttu-id="0d9db-121">Registrieren von com-Servern</span><span class="sxs-lookup"><span data-stu-id="0d9db-121">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="0d9db-122">Festlegen der Prozess weiten Sicherheit</span><span class="sxs-lookup"><span data-stu-id="0d9db-122">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




