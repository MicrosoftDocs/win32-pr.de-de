---
description: .
ms.assetid: f575109e-e9c4-4db5-945c-7c96b6b5d613
title: XPS-druckapi-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 828e999417354678d77ad1de8c29beb5956f7762
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755216"
---
# <a name="xps-print-api-interfaces"></a><span data-ttu-id="b1304-103">XPS-druckapi-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="b1304-103">XPS Print API Interfaces</span></span>

<span data-ttu-id="b1304-104">\[Die in diesem Abschnitt beschriebenen Schnittstellen sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="b1304-104">\[The interfaces described in this section are deprecated.</span></span> <span data-ttu-id="b1304-105">Client Anwendungen sollten stattdessen die [API zum Drucken von Dokument Paketen](./tailored-app-printing-api.md) verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="b1304-105">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="b1304-106">\[Ixpsprintjob wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="b1304-106">\[IXpsPrintJob is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="b1304-107">\]</span><span class="sxs-lookup"><span data-stu-id="b1304-107">\]</span></span>

<span data-ttu-id="b1304-108">\[Ixpsprintjobstream wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="b1304-108">\[IXpsPrintJobStream is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="b1304-109">\]</span><span class="sxs-lookup"><span data-stu-id="b1304-109">\]</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b1304-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="b1304-110">In this section</span></span>



| <span data-ttu-id="b1304-111">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b1304-111">Interface</span></span>                                                   | <span data-ttu-id="b1304-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b1304-112">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1304-113">**Ixpsprintjob**</span><span class="sxs-lookup"><span data-stu-id="b1304-113">**IXpsPrintJob**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjob)<br/>             | <span data-ttu-id="b1304-114">Ermöglicht den Zugriff auf einen Druckauftrag, der gerade ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1304-114">Provides access to a print job that is currently in progress.</span></span><br/>                  |
| [<span data-ttu-id="b1304-115">**Ixpsprintjobstream**</span><span class="sxs-lookup"><span data-stu-id="b1304-115">**IXpsPrintJobStream**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjobstream)<br/> | <span data-ttu-id="b1304-116">Eine schreibgeschützte Datenstrom Schnittstelle, in die eine Anwendung Druckauftrags Daten schreibt.</span><span class="sxs-lookup"><span data-stu-id="b1304-116">A write-only stream interface into which an application writes print job data.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="b1304-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b1304-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1304-118">Dokumente</span><span class="sxs-lookup"><span data-stu-id="b1304-118">Documents</span></span>](./jobbindalldocuments.md)
</dt> <dt>

[<span data-ttu-id="b1304-119">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="b1304-119">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

