---
title: Bypassaushandlung
description: Der Registrierungsschlüssel bypassaushandlung bestimmt, ob eine Aushandlung der Funktionen zwischen Server und Client erfolgt oder ob vorkonfigurierte Einstellungen verwendet werden.
ms.assetid: 51e21e9c-d6cb-454b-9584-3f48d76a649a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9fdf883249fc5af7a37be83bb153a670295ba1d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104389654"
---
# <a name="bypassnegotiation"></a><span data-ttu-id="39ad4-103">Bypassaushandlung</span><span class="sxs-lookup"><span data-stu-id="39ad4-103">BypassNegotiation</span></span>

<span data-ttu-id="39ad4-104">Der Registrierungsschlüssel bypassaushandlung bestimmt, ob eine Aushandlung der Funktionen zwischen Server und Client erfolgt oder ob vorkonfigurierte Einstellungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="39ad4-104">The BypassNegotiation registry key determines if capabilities negotiation between the server and client occurs or if pre-configured settings are used.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="39ad4-105">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="39ad4-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   BypassNegotiation = value
```

## <a name="remarks"></a><span data-ttu-id="39ad4-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39ad4-106">Remarks</span></span>

<span data-ttu-id="39ad4-107">Dies ist ein **reg \_ DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="39ad4-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="39ad4-108">Wert</span><span class="sxs-lookup"><span data-stu-id="39ad4-108">Value</span></span>   | <span data-ttu-id="39ad4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39ad4-109">Description</span></span>                                                                                                                                                                                          |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39ad4-110">0</span><span class="sxs-lookup"><span data-stu-id="39ad4-110">0</span></span>       | <span data-ttu-id="39ad4-111">Der Server und der Client aushandeln EAP-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="39ad4-111">Server and client negotiate EAP capabilities.</span></span>                                                                                                                                                        |
| <span data-ttu-id="39ad4-112">ungleich NULL</span><span class="sxs-lookup"><span data-stu-id="39ad4-112">nonzero</span></span> | <span data-ttu-id="39ad4-113">Der Server und der Client aushandeln keine EAP-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="39ad4-113">Server and client do not negotiate EAP capabilities.</span></span> <span data-ttu-id="39ad4-114">Server und Client verwenden den [AssumePhase2Fragmentation](assumephase2fragmentation.md) -Registrierungsschlüssel Wert, um die Funktionen anderer Parteien zu suchen.</span><span class="sxs-lookup"><span data-stu-id="39ad4-114">Server and client use the [AssumePhase2Fragmentation](assumephase2fragmentation.md) registry key value to find the other party's capabilities.</span></span> |



 

<span data-ttu-id="39ad4-115">Wenn dieser Registrierungs Wert nicht vorhanden ist, aushandelt der Server und der Client die EAP-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="39ad4-115">If this registry value is not present, the server and client negotiate EAP capabilities..</span></span>

## <a name="related-topics"></a><span data-ttu-id="39ad4-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39ad4-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39ad4-117">EAPHost-Registrierungs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="39ad4-117">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




