---
title: Bluetooth und setsockopt
description: Bluetooth verwendet die Setsockopt-Funktion, um verschiedene Parameter festzulegen, die dem Serverchannel oder der Verbindung zugeordnet sind.
ms.assetid: ab78baed-5556-4d7b-88a6-e3ceb93afa8c
keywords:
- Bluetooth
- setsockopt
- Bluetooth und setsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 943839a49788b76e597596aee9cba65fa4b8d30d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315344"
---
# <a name="bluetooth-and-setsockopt"></a><span data-ttu-id="e0c18-106">Bluetooth und setsockopt</span><span class="sxs-lookup"><span data-stu-id="e0c18-106">Bluetooth and setsockopt</span></span>

<span data-ttu-id="e0c18-107">Bluetooth verwendet die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion, um verschiedene Parameter festzulegen, die dem Serverchannel oder der Verbindung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e0c18-107">Bluetooth uses the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to set various parameters associated with the server channel or the connection.</span></span> <span data-ttu-id="e0c18-108">Für die Verwendung von **setsockopt** mit Bluetooth gelten die folgenden Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="e0c18-108">Use of **setsockopt** with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="e0c18-109">Der *s* -Parameter von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) muss ein gültiger Bluetooth-Socket sein.</span><span class="sxs-lookup"><span data-stu-id="e0c18-109">The *s* parameter of [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) must be a valid Bluetooth socket.</span></span>
-   <span data-ttu-id="e0c18-110">Der *Level* -Parameter von [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) muss "Sol \_ RFCOMM" lauten.</span><span class="sxs-lookup"><span data-stu-id="e0c18-110">The *level* parameter of [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) must be SOL\_RFCOMM.</span></span>

<span data-ttu-id="e0c18-111">Eine Liste der verfügbaren Bluetooth-Socketoptionen finden Sie unter [Optionen für Bluetooth und Socket](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="e0c18-111">For a listing of available Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0c18-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0c18-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0c18-113">Windows-Sockets</span><span class="sxs-lookup"><span data-stu-id="e0c18-113">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="e0c18-114">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="e0c18-114">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> </dl>

 

 