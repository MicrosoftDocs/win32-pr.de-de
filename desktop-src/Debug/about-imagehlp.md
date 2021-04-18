---
description: Die imagehlp-Funktionen werden hauptsächlich von Programmier Tools, Anwendungssetup-Hilfsprogramme und anderen Programmen verwendet, die Zugriff auf die in einem PE-Image enthaltenen Daten benötigen.
ms.assetid: 831d7bb2-bf01-4422-a940-173f9856a513
title: Informationen zu imagehlp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76da517a396536640df0e9bfcfa05368e4d0b76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344593"
---
# <a name="about-imagehlp"></a><span data-ttu-id="e387e-103">Informationen zu imagehlp</span><span class="sxs-lookup"><span data-stu-id="e387e-103">About ImageHlp</span></span>

<span data-ttu-id="e387e-104">Die imagehlp-Funktionen werden hauptsächlich von Programmier Tools, Anwendungssetup-Hilfsprogramme und anderen Programmen verwendet, die Zugriff auf die in einem PE-Image enthaltenen Daten benötigen.</span><span class="sxs-lookup"><span data-stu-id="e387e-104">The ImageHlp functions are used mostly by programming tools, application setup utilities, and other programs that need access to the data contained in a PE image.</span></span> <span data-ttu-id="e387e-105">Alle imagehlp-Funktionen sind Single Thread.</span><span class="sxs-lookup"><span data-stu-id="e387e-105">All ImageHlp functions are single threaded.</span></span> <span data-ttu-id="e387e-106">Daher führen Aufrufe von mehr als einem Thread zu dieser Funktion wahrscheinlich zu unerwartetem Verhalten oder einer Beschädigung des Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="e387e-106">Therefore, calls from more than one thread to this function will likely result in unexpected behavior or memory corruption.</span></span> <span data-ttu-id="e387e-107">Um dies zu vermeiden, müssen Sie alle gleichzeitigen Aufrufe von mehr als einem Thread an diese Funktion synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="e387e-107">To avoid this, you must synchronize all concurrent calls from more than one thread to this function.</span></span>

<span data-ttu-id="e387e-108">In den folgenden Themen werden PE-Images und die von den imagehlp-Funktionen bereitgestellten Funktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e387e-108">The following topics describe PE images and the functionality provided by the ImageHlp functions.</span></span>

-   [<span data-ttu-id="e387e-109">PE-Format</span><span class="sxs-lookup"><span data-stu-id="e387e-109">PE Format</span></span>](pe-format.md)
-   [<span data-ttu-id="e387e-110">Bild Zugriffs Funktionen</span><span class="sxs-lookup"><span data-stu-id="e387e-110">Image Access Functions</span></span>](image-access-functions.md)
-   [<span data-ttu-id="e387e-111">Bild Integritäts Funktionen</span><span class="sxs-lookup"><span data-stu-id="e387e-111">Image Integrity Functions</span></span>](image-integrity-functions.md)
-   [<span data-ttu-id="e387e-112">Funktionen zum Ändern von Bildern</span><span class="sxs-lookup"><span data-stu-id="e387e-112">Image Modification Functions</span></span>](image-modification-functions.md)

 

 



