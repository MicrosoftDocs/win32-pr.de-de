---
description: 'Damit eine Tablet PC-Anwendung effizient mit Ink arbeitet, sollte diese Anwendung folgende Aktionen ausführen können:'
ms.assetid: 64a7b773-35c9-42f7-aec4-7fed34fa84d9
title: Wichtige Interoperabilitäts Szenarien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6dca3bcbf52d673131122615fa5a08317dbf10c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341184"
---
# <a name="important-interoperability-scenarios"></a><span data-ttu-id="f7430-103">Wichtige Interoperabilitäts Szenarien</span><span class="sxs-lookup"><span data-stu-id="f7430-103">Important Interoperability Scenarios</span></span>

<span data-ttu-id="f7430-104">Damit eine Tablet PC-Anwendung effizient mit Ink arbeitet, sollte diese Anwendung folgende Aktionen ausführen können:</span><span class="sxs-lookup"><span data-stu-id="f7430-104">For a Tablet PC application to operate with ink effectively, that application should be able to:</span></span>

-   <span data-ttu-id="f7430-105">Speichern eines Dokuments im systemeigenen Binärformat der Anwendung, ohne den frei Hand Text des Dokuments zu verlieren.</span><span class="sxs-lookup"><span data-stu-id="f7430-105">Save a document in the application's native binary format without losing the document's ink.</span></span>
-   <span data-ttu-id="f7430-106">Speichern eines Dokuments in einem beliebigen Format, das von der Anwendung normalerweise unterstützt wird (z. b. html-oder Rich-Text-Format (RTF))</span><span class="sxs-lookup"><span data-stu-id="f7430-106">Save a document in any format the application normally supports (for example, HTML or Rich Text Format (RTF)) without losing the document's ink.</span></span>
-   <span data-ttu-id="f7430-107">Kopieren von frei Hand Eingaben aus einer Anwendung in eine andere mithilfe der Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="f7430-107">Copy ink from one application to another by using the Clipboard.</span></span> <span data-ttu-id="f7430-108">Dies funktioniert, wenn die andere Anwendung nur ein bestimmtes Format erkennt, z. b. html, RTF oder Bitmap (BMP).</span><span class="sxs-lookup"><span data-stu-id="f7430-108">This works if the other application only recognizes a specific format, such as HTML, RTF, or bitmap (BMP).</span></span> <span data-ttu-id="f7430-109">Es funktioniert auch, ob die Zielanwendung frei Hand Eingaben erkennt.</span><span class="sxs-lookup"><span data-stu-id="f7430-109">It also works whether the destination application recognizes ink.</span></span> <span data-ttu-id="f7430-110">Wenn frei Hand Eingaben erkannt werden, kann die Zielanwendung die frei Hand Eingaben interpretieren, die als frei Hand Eingaben und nicht nur als Bild kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="f7430-110">If it does recognize ink, the destination application is able to interpret the ink that has been copied as ink and not just as an image.</span></span>
-   <span data-ttu-id="f7430-111">Kopieren Sie frei Hand Eingaben zusammen mit Text zwischen zwei Anwendungen, die frei Hand Eingaben erkennen, von denen jeder über mehr als ein [**Ink**](inkdisp-class.md) -Objekt verfügt.</span><span class="sxs-lookup"><span data-stu-id="f7430-111">Copy ink, along with text, between two applications that recognize ink, each of which has more than one [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="f7430-112">Hierfür ist HTML, RTF oder ein ähnliches Format erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f7430-112">This requires HTML, RTF, or a similar format.</span></span>
-   <span data-ttu-id="f7430-113">Kopieren von frei Hand Eingaben zwischen zwei Anwendungen, von denen jedes über ein [**Ink**](inkdisp-class.md) -Objekt verfügt.</span><span class="sxs-lookup"><span data-stu-id="f7430-113">Copy ink between two applications, each of which has one [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="f7430-114">Das frei Hand Format (Ink Serialized Format, ISF) ist hierfür ausreichend.</span><span class="sxs-lookup"><span data-stu-id="f7430-114">Ink Serialized Format (ISF) is sufficient for this.</span></span>
-   <span data-ttu-id="f7430-115">Kopieren Sie Freihand aus einer Anwendung, die über mehr als ein [**Ink**](inkdisp-class.md) -Objekt verfügt, in eine Anwendung, die **nur ein frei** Hand Objekt aufweist.</span><span class="sxs-lookup"><span data-stu-id="f7430-115">Copy ink from an application that has more than one [**Ink**](inkdisp-class.md) object to an application that has only one **Ink** object.</span></span> <span data-ttu-id="f7430-116">In diesem Fall muss die Anwendung mit mehr als einem **Ink** -Objekt in der Lage sein, das frei Hand Format (Ink Serialized Format, ISF) zu liefern.</span><span class="sxs-lookup"><span data-stu-id="f7430-116">In this case, the application that has more than one **Ink** object must be able to produce Ink Serialized Format (ISF).</span></span>
-   <span data-ttu-id="f7430-117">Kopieren von frei Hand Eingaben aus einer Anwendung [**mit einem frei**](inkdisp-class.md) Hand Objekt in eine Anwendung, die über mehr **als ein frei** Hand Objekt verfügt.</span><span class="sxs-lookup"><span data-stu-id="f7430-117">Copy ink from an application that has one [**Ink**](inkdisp-class.md) object to an application that has more than one **Ink** object.</span></span> <span data-ttu-id="f7430-118">In diesem Fall muss die Anwendung, die über mehr als ein **Ink** -Objekt verfügt, ISF erkennen können.</span><span class="sxs-lookup"><span data-stu-id="f7430-118">In this case, the application that has more than one **Ink** object must be able to recognize ISF.</span></span>

 

 



