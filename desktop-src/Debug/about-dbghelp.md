---
description: In den folgenden Themen werden Symbol Dateien und die von den dbghelp-Funktionen bereitgestellten Funktionen beschrieben.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: Informationen zu dbghelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634633d44d0c9e8202d99fd16140dd0a506453ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126247"
---
# <a name="about-dbghelp"></a><span data-ttu-id="abbab-103">Informationen zu dbghelp</span><span class="sxs-lookup"><span data-stu-id="abbab-103">About DbgHelp</span></span>

<span data-ttu-id="abbab-104">In den folgenden Themen werden Symbol Dateien und die von den [dbghelp-Funktionen](dbghelp-functions.md)bereitgestellten Funktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="abbab-104">The following topics describe symbol files and the functionality provided by the [DbgHelp functions](dbghelp-functions.md).</span></span>

-   [<span data-ttu-id="abbab-105">Dbghelp-Versionen</span><span class="sxs-lookup"><span data-stu-id="abbab-105">DbgHelp Versions</span></span>](dbghelp-versions.md)
-   [<span data-ttu-id="abbab-106">Symbol Dateien</span><span class="sxs-lookup"><span data-stu-id="abbab-106">Symbol Files</span></span>](symbol-files.md)
-   [<span data-ttu-id="abbab-107">Symbol Behandlung</span><span class="sxs-lookup"><span data-stu-id="abbab-107">Symbol Handling</span></span>](symbol-handling.md)
-   [<span data-ttu-id="abbab-108">Symbol Server und Symbol Speicher</span><span class="sxs-lookup"><span data-stu-id="abbab-108">Symbol Servers and Symbol Stores</span></span>](symbol-servers-and-symbol-stores.md)
-   [<span data-ttu-id="abbab-109">Minidumpdateien</span><span class="sxs-lookup"><span data-stu-id="abbab-109">Minidump Files</span></span>](minidump-files.md)
-   [<span data-ttu-id="abbab-110">Quellserver</span><span class="sxs-lookup"><span data-stu-id="abbab-110">Source Server</span></span>](source-server-and-source-indexing.md)
-   [<span data-ttu-id="abbab-111">Aktualisierte Plattformunterstützung</span><span class="sxs-lookup"><span data-stu-id="abbab-111">Updated Platform Support</span></span>](updated-platform-support.md)

<span data-ttu-id="abbab-112">Beachten Sie, dass alle [dbghelp-Funktionen](dbghelp-functions.md) Single Thread sind.</span><span class="sxs-lookup"><span data-stu-id="abbab-112">Note that all [DbgHelp functions](dbghelp-functions.md) are single threaded.</span></span> <span data-ttu-id="abbab-113">Daher führen Aufrufe von mehr als einem Thread zu dieser Funktion wahrscheinlich zu unerwartetem Verhalten oder einer Beschädigung des Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="abbab-113">Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption.</span></span> <span data-ttu-id="abbab-114">Um dies zu vermeiden, müssen Sie alle gleichzeitigen Aufrufe von mehr als einem Thread an diese Funktion synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="abbab-114">To avoid this, you must synchronize all concurrent calls from more than one thread to this function.</span></span>

 

 



