---
title: Bluetooth und getsockopt
description: Bluetooth verwendet die getsockopt-Funktion, um verschiedene Parameter abzufragen, die dem Serverchannel oder der Verbindung zugeordnet sind.
ms.assetid: 9593fd6c-b55d-45d8-a9d9-87ebcd09d1bd
keywords:
- Bluetooth
- getsockopt
- Bluetooth und getsockopt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dede19b27eea39b7d1e778b3e92312a5e148c0ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728361"
---
# <a name="bluetooth-and-getsockopt"></a><span data-ttu-id="09c90-106">Bluetooth und getsockopt</span><span class="sxs-lookup"><span data-stu-id="09c90-106">Bluetooth and getsockopt</span></span>

<span data-ttu-id="09c90-107">Bluetooth verwendet die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion, um verschiedene Parameter abzufragen, die dem Serverchannel oder der Verbindung zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="09c90-107">Bluetooth uses the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function to query various parameters associated with the server channel or the connection.</span></span> <span data-ttu-id="09c90-108">Für die Verwendung von **getsockopt** mit Bluetooth gelten die folgenden Anforderungen:</span><span class="sxs-lookup"><span data-stu-id="09c90-108">Use of **getsockopt** with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="09c90-109">Der *s* -Parameter von [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) muss ein gültiger Bluetooth-Socket sein.</span><span class="sxs-lookup"><span data-stu-id="09c90-109">The *s* parameter of [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) must be a valid Bluetooth socket.</span></span>
-   <span data-ttu-id="09c90-110">Der *Level* -Parameter von [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) muss "Sol \_ RFCOMM" lauten.</span><span class="sxs-lookup"><span data-stu-id="09c90-110">The *level* parameter of [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) must be SOL\_RFCOMM.</span></span>

<span data-ttu-id="09c90-111">Eine Liste der verfügbaren Bluetooth-Socketoptionen finden Sie unter [Optionen für Bluetooth und Socket](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="09c90-111">For a listing of available Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="09c90-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="09c90-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09c90-113">Windows-Sockets</span><span class="sxs-lookup"><span data-stu-id="09c90-113">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="09c90-114">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="09c90-114">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> </dl>

 

 