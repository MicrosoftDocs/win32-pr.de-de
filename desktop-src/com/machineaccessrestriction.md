---
title: MachineAccessRestriction
description: Legt die Computer weite Einschränkungs Richtlinie für den Komponenten Zugriff fest.
ms.assetid: aeb37e49-6425-4058-968e-f9d00acf4fc2
keywords:
- Machineaccesseinschränkung-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d99e747b8a38dbb41cb8a6a8adc0935d3f9fa8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342289"
---
# <a name="machineaccessrestriction"></a><span data-ttu-id="db7fb-104">MachineAccessRestriction</span><span class="sxs-lookup"><span data-stu-id="db7fb-104">MachineAccessRestriction</span></span>

<span data-ttu-id="db7fb-105">Legt die Computer weite Einschränkungs Richtlinie für den Komponenten Zugriff fest.</span><span class="sxs-lookup"><span data-stu-id="db7fb-105">Sets the computer-wide restriction policy for component access.</span></span>

> [!Caution]  
> <span data-ttu-id="db7fb-106">Wenn Sie diesen Wert ändern, wirkt sich dies auf alle com-Server Anwendungen aus und kann die ordnungsgemäße Ausführung verhindern.</span><span class="sxs-lookup"><span data-stu-id="db7fb-106">Changing this value will affect all COM server applications, and might prevent them from working properly.</span></span> <span data-ttu-id="db7fb-107">Wenn es com-Server Anwendungen gibt, die Einschränkungen aufweisen, die weniger streng sind als die Computer weiten Einschränkungen, können diese Anwendungen durch eine Reduzierung der Computer weiten Einschränkungen für unerwünschte Zugriffe zugänglich gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="db7fb-107">If there are COM server applications that have restrictions that are less stringent than the computer-wide restrictions, reducing the computer-wide restrictions may expose these applications to unwanted access.</span></span> <span data-ttu-id="db7fb-108">Wenn Sie dagegen die Computer weiten Einschränkungen erhöhen, können einige com-Server Anwendungen nicht mehr durch das Aufrufen von Anwendungen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="db7fb-108">Conversely, if you increase the computer-wide restrictions, some COM server applications might no longer be accessible by calling applications.</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="db7fb-109">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="db7fb-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineAccessRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a><span data-ttu-id="db7fb-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db7fb-110">Remarks</span></span>

<span data-ttu-id="db7fb-111">Dies ist ein **reg- \_ Binärwert** .</span><span class="sxs-lookup"><span data-stu-id="db7fb-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="db7fb-112">Prinzipale, die hier nicht über Berechtigungen verfügen, können diese auch dann nicht abrufen, wenn die Berechtigungen durch den Registrierungs Wert [DefaultAccessPermission](defaultaccesspermission.md) oder durch die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="db7fb-112">Principals not given permissions here cannot obtain them even if the permissions are granted by the [DefaultAccessPermission](defaultaccesspermission.md) registry value or by the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function.</span></span>

<span data-ttu-id="db7fb-113">Standardmäßig können Mitglieder der Gruppe "jeder" Berechtigungen für den lokalen Zugriff und den Remote Zugriff erhalten, und anonyme Benutzer können lokale Zugriffsberechtigungen erhalten.</span><span class="sxs-lookup"><span data-stu-id="db7fb-113">By default, members of the Everyone group can obtain local and remote access permissions, and anonymous users can obtain local access permissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db7fb-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="db7fb-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db7fb-115">Festlegen der Sicherheit für COM-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="db7fb-115">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




