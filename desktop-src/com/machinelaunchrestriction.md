---
title: MachineLaunchRestriction
description: Legt die Computer weite Einschränkungs Richtlinie für das Starten und Aktivieren von Komponenten fest.
ms.assetid: 274e3d08-1f38-4179-b7e7-b218d6e184ee
keywords:
- Machinelauncheinschränkungs-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14dfcfe5535871c6b5b0fe310c94b920c522f05a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207263"
---
# <a name="machinelaunchrestriction"></a><span data-ttu-id="d0845-104">MachineLaunchRestriction</span><span class="sxs-lookup"><span data-stu-id="d0845-104">MachineLaunchRestriction</span></span>

<span data-ttu-id="d0845-105">Legt die Computer weite Einschränkungs Richtlinie für das Starten und Aktivieren von Komponenten fest.</span><span class="sxs-lookup"><span data-stu-id="d0845-105">Sets the computer-wide restriction policy for component launch and activation.</span></span>

> [!Caution]  
> <span data-ttu-id="d0845-106">Wenn Sie diesen Wert ändern, wirkt sich dies auf alle com-Server Anwendungen aus und kann die ordnungsgemäße Ausführung verhindern.</span><span class="sxs-lookup"><span data-stu-id="d0845-106">Changing this value will affect all COM server applications, and might prevent them from working properly.</span></span> <span data-ttu-id="d0845-107">Wenn es com-Server Anwendungen gibt, die Einschränkungen aufweisen, die weniger streng sind als die Computer weiten Einschränkungen, können diese Anwendungen durch eine Reduzierung der Computer weiten Einschränkungen für unerwünschte Zugriffe zugänglich gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="d0845-107">If there are COM server applications that have restrictions that are less stringent than the computer-wide restrictions, reducing the computer-wide restrictions may expose these applications to unwanted access.</span></span> <span data-ttu-id="d0845-108">Wenn Sie dagegen die Computer weiten Einschränkungen erhöhen, können einige com-Server Anwendungen nicht mehr durch das Aufrufen von Anwendungen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d0845-108">Conversely, if you increase the computer-wide restrictions, some COM server applications might no longer be accessible by calling applications.</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="d0845-109">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="d0845-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineLaunchRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a><span data-ttu-id="d0845-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0845-110">Remarks</span></span>

<span data-ttu-id="d0845-111">Dies ist ein **reg- \_ Binärwert** .</span><span class="sxs-lookup"><span data-stu-id="d0845-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="d0845-112">Prinzipale, die hier nicht über Berechtigungen verfügen, können diese auch dann nicht abrufen, wenn die Berechtigungen durch den Registrierungs Wert [DefaultAccessPermission](defaultaccesspermission.md) oder durch die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="d0845-112">Principals not given permissions here cannot obtain them even if the permissions are granted by the [DefaultAccessPermission](defaultaccesspermission.md) registry value or by the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function.</span></span>

<span data-ttu-id="d0845-113">Standardmäßig können Administratoren lokale und Remote Start-und Aktivierungs Berechtigungen erhalten, und Mitglieder der Gruppe Jeder können lokale Aktivierungs-und Start Berechtigungen erhalten.</span><span class="sxs-lookup"><span data-stu-id="d0845-113">By default, administrators may obtain local and remote launch and activation permissions, and members of the Everyone group may obtain local activation and launch permissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0845-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d0845-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0845-115">Festlegen der Sicherheit für COM-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="d0845-115">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




