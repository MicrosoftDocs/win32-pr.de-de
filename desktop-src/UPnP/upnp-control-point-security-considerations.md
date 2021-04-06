---
title: Überlegungen zur Steuerungspunkt Sicherheit
description: Wenn Sie einen Steuerungspunkt erstellen, müssen Sie die folgenden Sicherheitsprobleme berücksichtigen.
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0165ad0c8a721b10d5cc34c49947a98f2c15d1de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947930"
---
# <a name="control-point-security-considerations"></a><span data-ttu-id="76082-103">Überlegungen zur Steuerungspunkt Sicherheit</span><span class="sxs-lookup"><span data-stu-id="76082-103">Control Point Security Considerations</span></span>

<span data-ttu-id="76082-104">Wenn Sie einen Steuerungspunkt erstellen, müssen Sie die folgenden Sicherheitsprobleme berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="76082-104">When you are creating a control point, you need to take into consideration the following security issues.</span></span>

-   <span data-ttu-id="76082-105">Alle Kontrollpunkt suchen werden standardmäßig mit einer Gültigkeitsdauer von 1 gesendet.</span><span class="sxs-lookup"><span data-stu-id="76082-105">All control point searches are by default sent with a TTL of 1.</span></span> <span data-ttu-id="76082-106">Dies bedeutet, dass nur Geräte innerhalb desselben Subnetzes erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="76082-106">This means that only devices within the same subnet are discovered.</span></span> <span data-ttu-id="76082-107">Sie können eine höhere Gültigkeitsdauer in der Registrierung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="76082-107">You can configure a higher TTL in the registry.</span></span>
-   <span data-ttu-id="76082-108">Das Gerät und die Dienst Beschreibung eines Geräts werden nur heruntergeladen, wenn es auf dem gleichen Gerät vorhanden ist, von dem die Geräte Ankündigung gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="76082-108">A device's device and service description is only downloaded if it is present on the same device which sent the device announcement.</span></span>
-   <span data-ttu-id="76082-109">Einem Gerät werden nur Steuerungs-und Abonnement Anforderungen gesendet, wenn sich seine Steuerungs-und Abonnement-URLs auf demselben Gerät befinden, von dem die Geräte Ankündigungen gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="76082-109">A device is only sent control and subscription requests if its control and subscription URLs are on the same device that sent the device announcements.</span></span>

 

 




