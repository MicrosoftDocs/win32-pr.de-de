---
title: EnableDCOM
description: Steuert die globalen Aktivierungs-und rufrichtlinien des Computers. Nur Administratoren und das System verfügen über Vollzugriff auf diesen Teil der Registrierung. Alle anderen Benutzer verfügen über schreibgeschützten Zugriff.
ms.assetid: 8533270d-f1b0-42b9-a50d-b05a0dfeee22
keywords:
- Registrierungs Wert für EnableDCOM com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b42cc95b24522e87e4b64f6feefc5c6c56ad5341
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388153"
---
# <a name="enabledcom"></a><span data-ttu-id="a5a2e-106">EnableDCOM</span><span class="sxs-lookup"><span data-stu-id="a5a2e-106">EnableDCOM</span></span>

<span data-ttu-id="a5a2e-107">Steuert die globalen Aktivierungs-und rufrichtlinien des Computers.</span><span class="sxs-lookup"><span data-stu-id="a5a2e-107">Controls the global activation and call policies of the machine.</span></span> <span data-ttu-id="a5a2e-108">Nur Administratoren und das System verfügen über Vollzugriff auf diesen Teil der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="a5a2e-108">Only administrators and the system have full access to this portion of the registry.</span></span> <span data-ttu-id="a5a2e-109">Alle anderen Benutzer verfügen über schreibgeschützten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="a5a2e-109">All other users have read-only access.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="a5a2e-110">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="a5a2e-110">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   EnableDCOM = value
```

## <a name="remarks"></a><span data-ttu-id="a5a2e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5a2e-111">Remarks</span></span>

<span data-ttu-id="a5a2e-112">Dies ist ein **reg \_ SZ** -Wert.</span><span class="sxs-lookup"><span data-stu-id="a5a2e-112">This is a **REG\_SZ** value.</span></span>



| <span data-ttu-id="a5a2e-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a5a2e-113">Value</span></span>    | <span data-ttu-id="a5a2e-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5a2e-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5a2e-115">N (oder n)</span><span class="sxs-lookup"><span data-stu-id="a5a2e-115">N (or n)</span></span> | <span data-ttu-id="a5a2e-116">Keine Remote Clients können Server starten oder eine Verbindung mit Objekten auf diesem Computer herstellen.</span><span class="sxs-lookup"><span data-stu-id="a5a2e-116">No remote clients may launch servers or connect to objects on this computer.</span></span> <span data-ttu-id="a5a2e-117">Lokale Clients können nicht auf Remote-DCOM-Server zugreifen. der gesamte DCOM-Datenverkehr wird blockiert.</span><span class="sxs-lookup"><span data-stu-id="a5a2e-117">Local clients cannot access remote DCOM servers; all DCOM traffic is blocked.</span></span> <span data-ttu-id="a5a2e-118">Das lokale starten von Klassen Code und das Herstellen einer Verbindung mit Objekten ist auf Klassenbasis gemäß den Werten und Zugriffsberechtigungen des Registrierungs Werts " [**launchberechtigungs**](launchpermission.md) " der Klasse und des globalen [**defaultlaunchberechtigung**](defaultlaunchpermission.md) -Registrierungs Werts zulässig.</span><span class="sxs-lookup"><span data-stu-id="a5a2e-118">Local launching of class code and connecting to objects are allowed on a per-class basis according to the value and access permissions of the class's [**LaunchPermission**](launchpermission.md) registry value and the global [**DefaultLaunchPermission**](defaultlaunchpermission.md) registry value.</span></span> |
| <span data-ttu-id="a5a2e-119">Y (oder y)</span><span class="sxs-lookup"><span data-stu-id="a5a2e-119">Y (or y)</span></span> | <span data-ttu-id="a5a2e-120">Das Starten von Servern und das Herstellen einer Verbindung mit Objekten durch Remote Clients ist auf Klassenbasis gemäß den Werten und Zugriffsberechtigungen des Registrierungs Werts " [**launchberechtigungs**](launchpermission.md) " der Klasse und des globalen [**defaultlaunchberechtigung**](defaultlaunchpermission.md) -Registrierungs Werts zulässig.</span><span class="sxs-lookup"><span data-stu-id="a5a2e-120">Launching of servers and connecting to objects by remote clients is allowed on a per-class basis according to the value and access permissions of the class's [**LaunchPermission**](launchpermission.md) registry value and the global [**DefaultLaunchPermission**](defaultlaunchpermission.md) registry value.</span></span>                                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="a5a2e-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a5a2e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5a2e-122">**DefaultLaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="a5a2e-122">**DefaultLaunchPermission**</span></span>](defaultlaunchpermission.md)
</dt> <dt>

[<span data-ttu-id="a5a2e-123">**Launchberechtigung**</span><span class="sxs-lookup"><span data-stu-id="a5a2e-123">**LaunchPermission**</span></span>](launchpermission.md)
</dt> <dt>

[<span data-ttu-id="a5a2e-124">Sicherheit in com</span><span class="sxs-lookup"><span data-stu-id="a5a2e-124">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




