---
description: XPS-Druck-API-Schnittstellen
ms.assetid: f575109e-e9c4-4db5-945c-7c96b6b5d613
title: XPS-Druck-API-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47cd01c169c82a9e3210f281ec6c44fa206c40b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105188"
---
# <a name="xps-print-api-interfaces"></a><span data-ttu-id="2aeef-103">XPS-Druck-API-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="2aeef-103">XPS Print API Interfaces</span></span>

<span data-ttu-id="2aeef-104">\[Die in diesem Abschnitt beschriebenen Schnittstellen sind veraltet.</span><span class="sxs-lookup"><span data-stu-id="2aeef-104">\[The interfaces described in this section are deprecated.</span></span> <span data-ttu-id="2aeef-105">Clientanwendungen sollten stattdessen die [Druckdokumentpaket-API](./tailored-app-printing-api.md) verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="2aeef-105">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="2aeef-106">\[IXpsPrintJob wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="2aeef-106">\[IXpsPrintJob is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="2aeef-107">\]</span><span class="sxs-lookup"><span data-stu-id="2aeef-107">\]</span></span>

<span data-ttu-id="2aeef-108">\[IXpsPrintJobStream wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="2aeef-108">\[IXpsPrintJobStream is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="2aeef-109">\]</span><span class="sxs-lookup"><span data-stu-id="2aeef-109">\]</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2aeef-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="2aeef-110">In this section</span></span>



| <span data-ttu-id="2aeef-111">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2aeef-111">Interface</span></span>                                                   | <span data-ttu-id="2aeef-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2aeef-112">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2aeef-113">**IXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="2aeef-113">**IXpsPrintJob**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjob)<br/>             | <span data-ttu-id="2aeef-114">Ermöglicht den Zugriff auf einen Druckauftrag, der gerade in Bearbeitung ist.</span><span class="sxs-lookup"><span data-stu-id="2aeef-114">Provides access to a print job that is currently in progress.</span></span><br/>                  |
| [<span data-ttu-id="2aeef-115">**IXpsPrintJobStream**</span><span class="sxs-lookup"><span data-stu-id="2aeef-115">**IXpsPrintJobStream**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjobstream)<br/> | <span data-ttu-id="2aeef-116">Eine datenübertragungsbasierte Schnittstelle, in die eine Anwendung Druckauftragsdaten schreibt.</span><span class="sxs-lookup"><span data-stu-id="2aeef-116">A write-only stream interface into which an application writes print job data.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="2aeef-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2aeef-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2aeef-118">Dokumente</span><span class="sxs-lookup"><span data-stu-id="2aeef-118">Documents</span></span>](./jobbindalldocuments.md)
</dt> <dt>

[<span data-ttu-id="2aeef-119">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="2aeef-119">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

