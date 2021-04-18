---
title: AssumePhase2Fragmentation
description: Der Registrierungsschlüssel AssumePhase2Fragmentation bestimmt, ob der Server und der Client die Fragmentierung der Phase 2 annehmen.
ms.assetid: 3d6ececf-8871-4038-9706-4da57857d25a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b0fa35692ec3ac741e2bd2fdb43607dfe1cb948
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104389636"
---
# <a name="assumephase2fragmentation"></a><span data-ttu-id="e0244-103">AssumePhase2Fragmentation</span><span class="sxs-lookup"><span data-stu-id="e0244-103">AssumePhase2Fragmentation</span></span>

<span data-ttu-id="e0244-104">Der Registrierungsschlüssel AssumePhase2Fragmentation bestimmt, ob der Server und der Client die Fragmentierung der Phase 2 annehmen.</span><span class="sxs-lookup"><span data-stu-id="e0244-104">The AssumePhase2Fragmentation registry key determines if the server and client assume phase 2 fragmentation.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="e0244-105">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="e0244-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   AssumePhase2Fragmentation = value
```

## <a name="remarks"></a><span data-ttu-id="e0244-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0244-106">Remarks</span></span>

<span data-ttu-id="e0244-107">Dies ist ein **reg \_ DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="e0244-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="e0244-108">Wert</span><span class="sxs-lookup"><span data-stu-id="e0244-108">Value</span></span>   | <span data-ttu-id="e0244-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0244-109">Description</span></span>                                                                                                  |
|---------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0244-110">0</span><span class="sxs-lookup"><span data-stu-id="e0244-110">0</span></span>       | <span data-ttu-id="e0244-111">Server und Client gehen davon aus, dass die andere Partei während der Peer-Authentifizierung keine Fragmentierung in Phase 2 durchsetzen kann.</span><span class="sxs-lookup"><span data-stu-id="e0244-111">Server and client assume the other party is not capable of phase 2 fragmentation during PEAP authentication.</span></span> |
| <span data-ttu-id="e0244-112">ungleich NULL</span><span class="sxs-lookup"><span data-stu-id="e0244-112">nonzero</span></span> | <span data-ttu-id="e0244-113">Server und Client gehen davon aus, dass die andere Partei während der Peer-Authentifizierung die Fragmentierung der Phase 2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e0244-113">Server and client assume the other party is capable of phase 2 fragmentation during PEAP authentication.</span></span>     |



 

<span data-ttu-id="e0244-114">Wenn dieser Registrierungs Wert nicht vorhanden ist, gehen Server und Client davon aus, dass die andere Partei während der Peer-Authentifizierung die Fragmentierung der Phase 2 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e0244-114">If this registry value is not present, the server and client assume the other party is capable of phase 2 fragmentation during PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0244-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0244-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0244-116">EAPHost-Registrierungs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="e0244-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




