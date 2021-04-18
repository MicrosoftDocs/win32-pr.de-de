---
title: Das TESTFLAG
description: Das TESTFLAG
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- MCI_TEST-Flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36cddaa186a9be260cf87b7a323a6e05ed9fc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311424"
---
# <a name="the-test-flag"></a><span data-ttu-id="716ea-104">Das TESTFLAG</span><span class="sxs-lookup"><span data-stu-id="716ea-104">The Test Flag</span></span>

<span data-ttu-id="716ea-105">Mit dem Flag "Test" (MCI- \_ Test) wird das Gerät abgefragt, um zu bestimmen, ob der Befehl ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="716ea-105">The "test" (MCI\_TEST) flag queries the device to determine if it can execute the command.</span></span> <span data-ttu-id="716ea-106">Das Gerät gibt einen Fehler zurück, wenn der Befehl nicht ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="716ea-106">The device returns an error if it cannot execute the command.</span></span> <span data-ttu-id="716ea-107">Wenn der Befehl behandelt werden kann, wird kein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="716ea-107">It returns no error if it can handle the command.</span></span> <span data-ttu-id="716ea-108">Wenn Sie dieses Flag angeben, gibt MCI die Steuerung an die Anwendung zurück, ohne den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="716ea-108">When you specify this flag, MCI returns control to the application without executing the command.</span></span>

<span data-ttu-id="716ea-109">Dieses Flag wird von Digital-Video-und VCR-Geräten für alle Befehle mit Ausnahme von [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)) und [**Close**](close.md) ([**MCI \_ Close**](mci-close.md)) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="716ea-109">This flag is supported by digital-video and VCR devices for all commands except [**open**](open.md) ([**MCI\_OPEN**](mci-open.md)) and [**close**](close.md) ([**MCI\_CLOSE**](mci-close.md)).</span></span>

 

 




