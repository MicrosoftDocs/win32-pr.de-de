---
description: Das Konzept der Blockierung in einer Windows-Umgebung war in der Vergangenheit ein sehr wichtiges Konzept.
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: Blockierende Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8040865b4c6ededab925279e15d67cb89f7bc6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372819"
---
# <a name="blocking-operations"></a><span data-ttu-id="e587b-103">Blockierende Vorgänge</span><span class="sxs-lookup"><span data-stu-id="e587b-103">Blocking Operations</span></span>

<span data-ttu-id="e587b-104">Das Konzept der Blockierung in einer Windows-Umgebung war in der Vergangenheit ein sehr wichtiges Konzept.</span><span class="sxs-lookup"><span data-stu-id="e587b-104">The notion of blocking in a Windows environment has historically been a very important one.</span></span> <span data-ttu-id="e587b-105">In Windows Sockets 1,1-Umgebungen wurde das Blockieren von Aufrufen davon abgeraten, da Sie die laufende Interaktion mit dem System nicht mehr deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="e587b-105">In Windows Sockets 1.1 environments, blocking calls were discouraged since they tended to disable ongoing interaction with the system.</span></span> <span data-ttu-id="e587b-106">Außerdem verwenden Sie eine Pseudo Blockierungs Methode, die aus verschiedenen Gründen nicht immer wie beabsichtigt funktioniert.</span><span class="sxs-lookup"><span data-stu-id="e587b-106">Additionally, they employ a pseudoblocking technique which, for a variety of reasons, does not always work as intended.</span></span> <span data-ttu-id="e587b-107">In voremptiv geplanten Windows-Umgebungen sind blockierende Aufrufe jedoch viel sinnvoller, können durch systemeigene Betriebssystem Dienste implementiert werden und sind tatsächlich ein allgemein bevorzugter Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="e587b-107">However, in preemptively scheduled Windows environments, blocking calls make much more sense, can be implemented by native operating system services, and are in fact a generally preferred mechanism.</span></span> <span data-ttu-id="e587b-108">Die Winsock 2-API unterstützt psuedoblockierungen nicht mehr, aber da die Windows Sockets 1,1-Kompatibilitäts-Shims weiterhin dieses Verhalten emulieren müssen, müssen die Dienstanbieter dies unterstützen, wie im folgenden beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e587b-108">The Winsock 2 API no longer supports psuedoblocking, but because the Windows Sockets 1.1 compatibility shims must continue to emulate this behavior, service providers must support this as described in the following.</span></span>

 

 



