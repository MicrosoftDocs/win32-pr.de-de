---
description: Die folgenden Fehlercodes sind spezifisch für die Setup-API.
ms.assetid: C4EB130F-2A83-4A14-BBA8-DB10225D0C0A
title: Fehler Codes (Setup-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ce77fd224abb16c519f4b77fa93f775fe203d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485534"
---
# <a name="error-codes-setup-api"></a><span data-ttu-id="552f6-103">Fehler Codes (Setup-API)</span><span class="sxs-lookup"><span data-stu-id="552f6-103">Error Codes (Setup API)</span></span>

<span data-ttu-id="552f6-104">Die folgenden Fehlercodes sind spezifisch für die Setup-API.</span><span class="sxs-lookup"><span data-stu-id="552f6-104">The following error codes are specific to the Setup API.</span></span>



| <span data-ttu-id="552f6-105">INF-Parsing-Fehler</span><span class="sxs-lookup"><span data-stu-id="552f6-105">INF Parsing Errors</span></span>              | <span data-ttu-id="552f6-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="552f6-106">Description</span></span>                                                                                                         |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="552f6-107">Fehler beim \_ erwarteten \_ Abschnitts \_ Name.</span><span class="sxs-lookup"><span data-stu-id="552f6-107">ERROR\_EXPECTED\_SECTION\_NAME</span></span>  | <span data-ttu-id="552f6-108">Ein Abschnitts Name wurde erwartet und wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="552f6-108">A section name was expected and not found.</span></span>                                                                          |
| <span data-ttu-id="552f6-109">Fehler \_ hafte \_ Abschnitts \_ namens \_ Zeile</span><span class="sxs-lookup"><span data-stu-id="552f6-109">ERROR\_BAD\_SECTION\_NAME\_LINE</span></span> | <span data-ttu-id="552f6-110">Der Abschnitts Name hatte nicht das richtige Format.</span><span class="sxs-lookup"><span data-stu-id="552f6-110">The section name was not of the correct format.</span></span> <span data-ttu-id="552f6-111">(Ein Name wird z. b. nicht durch eine rechte eckige Klammer ( \] ) beendet.</span><span class="sxs-lookup"><span data-stu-id="552f6-111">(For example, a name not terminated by a right-hand bracket ( \] ).</span></span> |
| <span data-ttu-id="552f6-112">der Fehler \_ Abschnitts \_ Name ist \_ zu \_ lang.</span><span class="sxs-lookup"><span data-stu-id="552f6-112">ERROR\_SECTION\_NAME\_TOO\_LONG</span></span> | <span data-ttu-id="552f6-113">Der Abschnitts Name hat die maximale Länge von Max \_ . Sect- \_ Name len überschritten \_ .</span><span class="sxs-lookup"><span data-stu-id="552f6-113">The section name exceeded the maximum length of MAX\_SECT\_NAME\_LEN.</span></span>                                               |
| <span data-ttu-id="552f6-114">\_Allgemeine Fehler \_ Syntax</span><span class="sxs-lookup"><span data-stu-id="552f6-114">ERROR\_GENERAL\_SYNTAX</span></span>          | <span data-ttu-id="552f6-115">Die allgemeine Syntax ist falsch.</span><span class="sxs-lookup"><span data-stu-id="552f6-115">The general syntax is incorrect.</span></span>                                                                                    |



 



| <span data-ttu-id="552f6-116">INF-Laufzeitfehler</span><span class="sxs-lookup"><span data-stu-id="552f6-116">INF Runtime Errors</span></span>         | <span data-ttu-id="552f6-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="552f6-117">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="552f6-118">Fehler \_ beim \_ INF- \_ Stil.</span><span class="sxs-lookup"><span data-stu-id="552f6-118">ERROR\_WRONG\_INF\_STYLE</span></span>   | <span data-ttu-id="552f6-119">Die INF-Datei ist nicht vom Typ, der im Funktions aufrufsbefehl angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="552f6-119">The INF file is not of the type specified in the function call.</span></span> <span data-ttu-id="552f6-120">Dieser Fehler kann z. b. von der [**setupopenappendinffile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) -Funktion zurückgegeben werden, wenn die INF-Datei für eine frühe Version von Windows vorgesehen war.</span><span class="sxs-lookup"><span data-stu-id="552f6-120">For example, this error may be returned by the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function if the INF file was intended for an early version of Windows.</span></span> |
| <span data-ttu-id="552f6-121">der Fehler \_ Abschnitt wurde \_ nicht \_ gefunden.</span><span class="sxs-lookup"><span data-stu-id="552f6-121">ERROR\_SECTION\_NOT\_FOUND</span></span> | <span data-ttu-id="552f6-122">Der Abschnitt wurde in der INF-Datei nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="552f6-122">The section was not found in the INF file.</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="552f6-123">Fehler \_ Zeile \_ nicht \_ gefunden.</span><span class="sxs-lookup"><span data-stu-id="552f6-123">ERROR\_LINE\_NOT\_FOUND</span></span>    | <span data-ttu-id="552f6-124">Die Zeile wurde im INF-Abschnitt nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="552f6-124">The line was not found in the INF section.</span></span>                                                                                                                                                                                                     |



 

 

 



