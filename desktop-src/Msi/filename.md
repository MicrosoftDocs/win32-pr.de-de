---
description: Der Datentyp Dateiname ist eine Text Zeichenfolge, die einen Dateinamen oder einen Ordner enthält.
ms.assetid: af59e1b8-0699-4031-895f-415752611e21
title: Dateiname
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fc049fa0808efc180afbd715e311a124bfdada9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528190"
---
# <a name="filename"></a><span data-ttu-id="62845-103">Dateiname</span><span class="sxs-lookup"><span data-stu-id="62845-103">Filename</span></span>

<span data-ttu-id="62845-104">Der Datentyp Dateiname ist eine Text Zeichenfolge, die einen Dateinamen oder einen Ordner enthält.</span><span class="sxs-lookup"><span data-stu-id="62845-104">The Filename data type is a text string containing a file name or folder.</span></span> <span data-ttu-id="62845-105">Standardmäßig wird davon ausgegangen, dass der Dateiname eine kurze Dateiname-Syntax verwendet. Dabei handelt es sich um einen achtstelligen Namen, einen Zeitraum (.) und eine Erweiterung mit drei Zeichen.</span><span class="sxs-lookup"><span data-stu-id="62845-105">By default, the file name is assumed to use short file name syntax; that is, eight-character name, period (.), and 3-character extension.</span></span> <span data-ttu-id="62845-106">Ein kurzer Dateiname muss immer angegeben werden, da die Eigenschaft [**shortfileames**](shortfilenames.md) festgelegt werden kann oder das Zielvolume für die Installation nur kurze Dateinamen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="62845-106">A short file name must always be provided because the [**SHORTFILENAMES**](shortfilenames.md) property may be set or the target volume for the installation may only support short file names.</span></span>

<span data-ttu-id="62845-107">Wenn Sie einen langen Dateinamen mit dem kurzen Dateinamen einschließen möchten, trennen Sie ihn vom kurzen Dateinamen mit einem senkrechten Strich ( \| ).</span><span class="sxs-lookup"><span data-stu-id="62845-107">To include a long file name with the short file name, separate it from the short file name with a vertical bar (\|).</span></span>

<span data-ttu-id="62845-108">Die folgenden beiden Zeichen folgen sind z. b. gültig:</span><span class="sxs-lookup"><span data-stu-id="62845-108">For example, the following two strings are valid:</span></span>

-   <span data-ttu-id="62845-109">status.txt</span><span class="sxs-lookup"><span data-stu-id="62845-109">status.txt</span></span>
-   <span data-ttu-id="62845-110">PROJEC ~1.txt\| Projekt Status.txt</span><span class="sxs-lookup"><span data-stu-id="62845-110">projec~1.txt\|Project Status.txt</span></span>

<span data-ttu-id="62845-111">Kurze und lange Dateinamen dürfen die folgenden Zeichen nicht enthalten:</span><span class="sxs-lookup"><span data-stu-id="62845-111">Short and long file names must not contain the following characters:</span></span>

-   <span data-ttu-id="62845-112">Schrägstrich (/) oder ( \\ )</span><span class="sxs-lookup"><span data-stu-id="62845-112">slash (/) or (\\)</span></span>
-   <span data-ttu-id="62845-113">Fragezeichen (?)</span><span class="sxs-lookup"><span data-stu-id="62845-113">question mark (?)</span></span>
-   <span data-ttu-id="62845-114">senkrechter Strich ( \| )</span><span class="sxs-lookup"><span data-stu-id="62845-114">vertical bar (\|)</span></span>
-   <span data-ttu-id="62845-115">Rechte Spitze Klammer (>)</span><span class="sxs-lookup"><span data-stu-id="62845-115">right angle bracket (>)</span></span>
-   <span data-ttu-id="62845-116">öffnende spitze Klammer (<)</span><span class="sxs-lookup"><span data-stu-id="62845-116">left angle bracket (<)</span></span>
-   <span data-ttu-id="62845-117">Doppelpunkt (:)</span><span class="sxs-lookup"><span data-stu-id="62845-117">colon (:)</span></span>
-   <span data-ttu-id="62845-118">Sternchen ( \* )</span><span class="sxs-lookup"><span data-stu-id="62845-118">asterisk (\*)</span></span>
-   <span data-ttu-id="62845-119">Anführungszeichen (")</span><span class="sxs-lookup"><span data-stu-id="62845-119">quotation mark (")</span></span>

<span data-ttu-id="62845-120">Außerdem dürfen kurze Dateinamen die folgenden Zeichen nicht enthalten:</span><span class="sxs-lookup"><span data-stu-id="62845-120">In addition, short file names must not contain the following characters:</span></span>

-   <span data-ttu-id="62845-121">Pluszeichen (+)</span><span class="sxs-lookup"><span data-stu-id="62845-121">plus sign (+)</span></span>
-   <span data-ttu-id="62845-122">Komma (,)</span><span class="sxs-lookup"><span data-stu-id="62845-122">comma (,)</span></span>
-   <span data-ttu-id="62845-123">Semikolon (;)</span><span class="sxs-lookup"><span data-stu-id="62845-123">semicolon (;)</span></span>
-   <span data-ttu-id="62845-124">Gleichheitszeichen (=)</span><span class="sxs-lookup"><span data-stu-id="62845-124">equals sign (=)</span></span>
-   <span data-ttu-id="62845-125">linke eckige Klammer ( \[ )</span><span class="sxs-lookup"><span data-stu-id="62845-125">left square bracket (\[)</span></span>
-   <span data-ttu-id="62845-126">rechte eckige Klammer ( \] )</span><span class="sxs-lookup"><span data-stu-id="62845-126">right square bracket (\])</span></span>

<span data-ttu-id="62845-127">Es ist kein Leerzeichen vor dem senkrechten Strich ( \| ) für die Syntax der kurzen Dateinamen/langen Dateinamen zulässig.</span><span class="sxs-lookup"><span data-stu-id="62845-127">No space is allowed preceding the vertical bar (\|) separator for the short file name/long file name syntax.</span></span> <span data-ttu-id="62845-128">Kurze Dateinamen dürfen keine Leerzeichen enthalten, obwohl ein langer Dateiname möglicherweise ist.</span><span class="sxs-lookup"><span data-stu-id="62845-128">Short file names may not include a space, although a long file name may.</span></span> <span data-ttu-id="62845-129">Ein Leerzeichen kann nach dem Trennzeichen nur vorhanden sein, wenn der lange Dateiname mit dem Leerzeichen beginnt.</span><span class="sxs-lookup"><span data-stu-id="62845-129">A space can exist after the separator only if the long file name of the file name begins with the space.</span></span> <span data-ttu-id="62845-130">Es ist keine vollständige Pfad Syntax zulässig.</span><span class="sxs-lookup"><span data-stu-id="62845-130">No full-path syntax is allowed.</span></span>

> [!Note]  
> <span data-ttu-id="62845-131">Das Format der Dateiname-Spalte der [msiembeddedui](msiembeddedui-table.md) -Tabelle entspricht dem Datentyp Datentyp Datentyp, mit dem Unterschied, dass das vertikale Balken \| Trennzeichen () für die Syntax kurzer Dateiname/langer Dateiname nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="62845-131">The format of the FileName column of the [MsiEmbeddedUI](msiembeddedui-table.md) table is like the format Filename data type except that the vertical bar (\|) separator for the short file name/long file name syntax is not available.</span></span>

 

 

 



