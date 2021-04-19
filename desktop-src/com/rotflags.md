---
title: Rotflags
description: Steuert die Registrierung eines COM-Servers in der laufenden Objekttabelle (rot).
ms.assetid: a27c04e5-b1d3-4cb5-9b2c-9ae45663cf56
keywords:
- Rotflags-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d52bc0c07ee6c86015ad1b997f2f21e33dda9a1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342254"
---
# <a name="rotflags"></a><span data-ttu-id="4d4e5-104">Rotflags</span><span class="sxs-lookup"><span data-stu-id="4d4e5-104">ROTFlags</span></span>

<span data-ttu-id="4d4e5-105">Steuert die Registrierung eines COM-Servers in der laufenden Objekttabelle (rot).</span><span class="sxs-lookup"><span data-stu-id="4d4e5-105">Controls the registration of a COM server in the running object table (ROT).</span></span>

## <a name="registry-entry"></a><span data-ttu-id="4d4e5-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="4d4e5-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ROTFlags = flags
```

## <a name="remarks"></a><span data-ttu-id="4d4e5-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d4e5-107">Remarks</span></span>

<span data-ttu-id="4d4e5-108">Dies ist ein **reg \_ DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="4d4e5-109">Flagwert</span><span class="sxs-lookup"><span data-stu-id="4d4e5-109">Flag Value</span></span> | <span data-ttu-id="4d4e5-110">Konstante</span><span class="sxs-lookup"><span data-stu-id="4d4e5-110">Constant</span></span>                        |
|------------|---------------------------------|
| <span data-ttu-id="4d4e5-111">0x1</span><span class="sxs-lookup"><span data-stu-id="4d4e5-111">0x1</span></span>        | <span data-ttu-id="4d4e5-112">**rotregflags- \_ zustandsclient**</span><span class="sxs-lookup"><span data-stu-id="4d4e5-112">**ROTREGFLAGS\_ALLOWANYCLIENT**</span></span> |



 

### <a name="rotregflags_allowanyclient-description"></a><span data-ttu-id="4d4e5-113">Rotregflags- \_ zustandsclientbeschreibung</span><span class="sxs-lookup"><span data-stu-id="4d4e5-113">ROTREGFLAGS\_ALLOWANYCLIENT Description</span></span>

<span data-ttu-id="4d4e5-114">Wenn ein com-Server in der rot registriert werden soll und jedem Client der Zugriff auf die Registrierung gestattet werden soll, muss das Flag " **rotflags \_ zugsclient** " verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-114">If a COM server wants to register in the ROT and allow any client to access the registration, it must use the **ROTFLAGS\_ALLOWANYCLIENT** flag.</span></span> <span data-ttu-id="4d4e5-115">Der com-Server "aktivieren als Aktivator" kann " **rotflags \_ Zuordnungs Client** " nicht angeben, da der DCOM-Dienststeuerungs-Manager (dcomscm) eine spodüberprüfung für dieses Flag erzwingt.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-115">An "Activate As Activator" COM server cannot specify **ROTFLAGS\_ALLOWANYCLIENT** because the DCOM service control manager (DCOMSCM) enforces a spoof check against this flag.</span></span> <span data-ttu-id="4d4e5-116">Daher fügt com in Windows Vista und höher Unterstützung für den **rotflags** -Registrierungs Eintrag hinzu, der es dem Server ermöglicht, festzulegen, dass seine rot-Registrierungen für jeden Client verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-116">Therefore, in Windows Vista and later, COM adds support for the **ROTFlags** registry entry that allows the server to stipulate that its ROT registrations be made available to any client.</span></span>

<span data-ttu-id="4d4e5-117">Der Eintrag muss in der Hive des **\_ lokalen \_ HKEY** -Computers vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-117">The entry must exist in the **HKEY\_LOCAL\_MACHINE** hive.</span></span> <span data-ttu-id="4d4e5-118">Dieser Eintrag bietet den Server "aktivieren als Aktivator" mit derselben Funktionalität, die von " **rotflags \_** " für einen runas-Server bereitstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4d4e5-118">This entry provides an "Activate As Activator" server with the same functionality that **ROTFLAGS\_ALLOWANYCLIENT** provides for a RunAs server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d4e5-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4d4e5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d4e5-120">AppID-Schlüssel</span><span class="sxs-lookup"><span data-stu-id="4d4e5-120">AppID Key</span></span>](appid-key.md)
</dt> <dt>

[<span data-ttu-id="4d4e5-121">Registrieren von com-Servern</span><span class="sxs-lookup"><span data-stu-id="4d4e5-121">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="4d4e5-122">Sicherheit in com</span><span class="sxs-lookup"><span data-stu-id="4d4e5-122">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




