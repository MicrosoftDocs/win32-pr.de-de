---
title: Preferredserverbitness
description: Legt die bevorzugte Architektur (32-Bit oder 64-Bit) für diesen com-Server fest.
ms.assetid: ef770039-1624-4256-aa09-1443695c1a1f
keywords:
- "' Preferredserverbitness '-Registrierungs Wert com"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a8c5b1504c5a59ca2ab178cd46236335d44ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316545"
---
# <a name="preferredserverbitness"></a><span data-ttu-id="3dcee-104">Preferredserverbitness</span><span class="sxs-lookup"><span data-stu-id="3dcee-104">PreferredServerBitness</span></span>

<span data-ttu-id="3dcee-105">Legt die bevorzugte Architektur (32-Bit oder 64-Bit) für diesen com-Server fest.</span><span class="sxs-lookup"><span data-stu-id="3dcee-105">Sets the preferred architecture, 32-bit or 64-bit, for this COM server.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3dcee-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="3dcee-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      PreferredServerBitness = value
```

## <a name="remarks"></a><span data-ttu-id="3dcee-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3dcee-107">Remarks</span></span>

<span data-ttu-id="3dcee-108">Dies ist ein **reg \_ DWORD** -Wert, der nur in 64-Bit-Versionen von Windows verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3dcee-108">This is a **REG\_DWORD** value that is available only on 64-bit versions of Windows.</span></span>



| <span data-ttu-id="3dcee-109">Wert</span><span class="sxs-lookup"><span data-stu-id="3dcee-109">Value</span></span> | <span data-ttu-id="3dcee-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3dcee-110">Description</span></span>                                                                                                                                                                                                |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3dcee-111">1</span><span class="sxs-lookup"><span data-stu-id="3dcee-111">1</span></span>     | <span data-ttu-id="3dcee-112">Vergleichen Sie die Serverarchitektur mit der Client Architektur.</span><span class="sxs-lookup"><span data-stu-id="3dcee-112">Match the server architecture to the client architecture.</span></span> <span data-ttu-id="3dcee-113">Wenn der Client z. b. 32-Bit ist, verwenden Sie eine 32-Bit-Version des Servers, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3dcee-113">For example, if the client is 32-bit, use a 32-bit version of the server, if it is available.</span></span> <span data-ttu-id="3dcee-114">Wenn dies nicht der Fall ist, schlägt die Aktivierungs Anforderung des Clients fehl.</span><span class="sxs-lookup"><span data-stu-id="3dcee-114">If not, the client's activation request will fail.</span></span> |
| <span data-ttu-id="3dcee-115">2</span><span class="sxs-lookup"><span data-stu-id="3dcee-115">2</span></span>     | <span data-ttu-id="3dcee-116">Verwenden Sie eine 32-Bit-Version des Servers.</span><span class="sxs-lookup"><span data-stu-id="3dcee-116">Use a 32-bit version of the server.</span></span> <span data-ttu-id="3dcee-117">Wenn keine vorhanden ist, tritt bei der Aktivierungs Anforderung des Clients ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="3dcee-117">If one does not exist, the client's activation request will fail.</span></span>                                                                                                      |
| <span data-ttu-id="3dcee-118">3</span><span class="sxs-lookup"><span data-stu-id="3dcee-118">3</span></span>     | <span data-ttu-id="3dcee-119">Verwenden Sie eine 64-Bit-Version des Servers.</span><span class="sxs-lookup"><span data-stu-id="3dcee-119">Use a 64-bit version of the server.</span></span> <span data-ttu-id="3dcee-120">Wenn keine vorhanden ist, tritt bei der Aktivierungs Anforderung des Clients ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="3dcee-120">If one does not exist, the client's activation request will fail.</span></span>                                                                                                      |



 

<span data-ttu-id="3dcee-121">Wenn dieser Wert nicht vorhanden ist, gilt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3dcee-121">If this value is not present, then:</span></span>

-   <span data-ttu-id="3dcee-122">Wenn auf dem Computer, auf dem der Server gehostet wird, Windows XP oder Windows Server 2003 ohne SP1 oder höher ausgeführt wird, wird com eine 64-Bit-Version des Servers bevorzugen, sofern verfügbar. Andernfalls wird eine 32-Bit-Version des Servers aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3dcee-122">If the computer that hosts the server is running Windows XP or Windows Server 2003 without SP1 or later installed, then COM will prefer a 64-bit version of the server if available; otherwise it will activate a 32-bit version of the server.</span></span>
-   <span data-ttu-id="3dcee-123">Wenn auf dem Computer, auf dem der Server gehostet wird, Windows Server 2003 mit SP1 oder höher ausgeführt wird, versucht com, die Serverarchitektur mit der Client Architektur zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="3dcee-123">If the computer that hosts the server is running Windows Server 2003 with SP1 or later installed, then COM will try to match the server architecture to the client architecture.</span></span> <span data-ttu-id="3dcee-124">Anders ausgedrückt: bei einem 32-Bit-Client aktiviert com einen 32-Bit-Server, falls verfügbar. Andernfalls wird eine 64-Bit-Version des Servers aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3dcee-124">In other words, for a 32-bit client, COM will activate a 32-bit server if available; otherwise it will activate a 64-bit version of the server.</span></span> <span data-ttu-id="3dcee-125">Bei einem 64-Bit-Client aktiviert com einen 64-Bit-Server, falls verfügbar. Andernfalls wird ein 32-Bit-Server aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3dcee-125">For a 64-bit client, COM will activate a 64-bit server if available; otherwise it will activate a 32-bit server.</span></span>

<span data-ttu-id="3dcee-126">Der Client kann auch seine eigene Architektur Einstellung über den CLSCTX \_ \_ \_ -32-Bit \_ -Server und CLSCTX aktivieren \_ \_ 64 Bit- \_ \_ Serverflags angeben. diese überschreiben die bevorzugte Servereinstellung.</span><span class="sxs-lookup"><span data-stu-id="3dcee-126">The client can also specify its own architecture preference via the CLSCTX\_ACTIVATE\_32\_BIT\_SERVER and CLSCTX\_ACTIVATE\_64\_BIT\_SERVER flags, and these will override the server's preference.</span></span> <span data-ttu-id="3dcee-127">Weitere Informationen und ein Diagramm möglicher Interaktionen zwischen Client-und Serverarchitektur Einstellungen finden Sie unter [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).</span><span class="sxs-lookup"><span data-stu-id="3dcee-127">For more information, and a chart of possible interactions between client and server architecture preferences, see [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3dcee-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3dcee-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3dcee-129">**CLSCTX**</span><span class="sxs-lookup"><span data-stu-id="3dcee-129">**CLSCTX**</span></span>](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> </dl>

 

 