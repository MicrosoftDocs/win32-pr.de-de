---
title: Sicherheit und erweiterte Fehlerinformationen
description: Erweiterte Fehlerinformationen bieten sehr nützliche Daten, wenn Sie ein RPC-Problem beheben. solche Daten werden jedoch von sicherheitsbewussten Organisationen als vertraulich eingestuft.
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b2029b40937dcef0622f6163e5e8f95b7006ade
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713553"
---
# <a name="security-and-extended-error-information"></a><span data-ttu-id="b686f-103">Sicherheit und erweiterte Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="b686f-103">Security and Extended Error Information</span></span>

<span data-ttu-id="b686f-104">Erweiterte Fehlerinformationen bieten sehr nützliche Daten, wenn Sie ein RPC-Problem beheben. solche Daten werden jedoch von sicherheitsbewussten Organisationen als vertraulich eingestuft.</span><span class="sxs-lookup"><span data-stu-id="b686f-104">Extended error information offers very useful data when troubleshooting an RPC problem, but such data many be considered confidential by security-conscious organizations.</span></span> <span data-ttu-id="b686f-105">Wenn solche Sicherheitsprobleme berücksichtigt werden, sind erweiterte Fehlerinformationen standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b686f-105">In consideration of such security issues, extended error information is turned off by default.</span></span>

<span data-ttu-id="b686f-106">Erweiterte Fehlerinformationen werden immer noch generiert, wenn erweiterte Fehlerinformationen deaktiviert sind, aber die Informationen niemals über Prozess-oder Computer Grenzen hinweg übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="b686f-106">Extended error information is still generated when extended error information is disabled, but the information is never transmitted across process or computer boundaries.</span></span> <span data-ttu-id="b686f-107">Diese Vorgehensweise ermöglicht es, dass Fehlerinformationen von Tools verwendet werden, die Zugriff auf den Prozess Adressraum haben, z. b. Debugger.</span><span class="sxs-lookup"><span data-stu-id="b686f-107">This approach enables error information to be used by tools that have access to the process address space, such as debuggers.</span></span> <span data-ttu-id="b686f-108">Wenn diese aktiviert ist, werden erweiterte Fehlerinformationen generiert und können über Prozess-und Computer Grenzen hinweg gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="b686f-108">When turned on, extended error information is generated and can be sent across process and computer boundaries.</span></span> <span data-ttu-id="b686f-109">Zurzeit werden erweiterte Fehlerinformationen für Verbindungs orientierte Protokoll Sequenzen und lokales RPC (LRPC) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b686f-109">Currently, extended error information is used for connection oriented protocol sequences and local RPC (LRPC).</span></span> <span data-ttu-id="b686f-110">Es ist teilweise für Datagramme implementiert.</span><span class="sxs-lookup"><span data-stu-id="b686f-110">It is partially implemented for datagrams.</span></span>

 

 




