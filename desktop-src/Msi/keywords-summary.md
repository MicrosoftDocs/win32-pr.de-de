---
description: Die Schlüsselwort Zusammenfassungs Eigenschaft in den Installations Datenbanken oder Transformationen enthält eine Liste von Schlüsselwörtern.
ms.assetid: e19dc495-e4d4-465f-8464-c60af8985334
title: Schlüsselwort Zusammenfassungs Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3828146fef861cd993331045d6a1380d84c2bbc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362017"
---
# <a name="keywords-summary-property"></a><span data-ttu-id="bbc77-103">Schlüsselwort Zusammenfassungs Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bbc77-103">Keywords Summary property</span></span>

<span data-ttu-id="bbc77-104">Die **Schlüsselwort Zusammenfassungs** Eigenschaft in den Installations Datenbanken oder Transformationen enthält eine Liste von Schlüsselwörtern.</span><span class="sxs-lookup"><span data-stu-id="bbc77-104">The **Keywords Summary** property in installation databases or transforms contains a list of keywords.</span></span> <span data-ttu-id="bbc77-105">Die Schlüsselwörter können von Datei Browsern verwendet werden, um Schlüsselwörter nach einer Datei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="bbc77-105">The keywords may be used by file browsers to do keyword searches for a file.</span></span> <span data-ttu-id="bbc77-106">Diese Eigenschaft enthält eine Liste der Quellen des Patches in einem Patchpaket.</span><span class="sxs-lookup"><span data-stu-id="bbc77-106">This property contains a list of sources of the patch in a patch package.</span></span>

<span data-ttu-id="bbc77-107">Es liegt an der Erstellung einer Installations Datenbank, einer Transformation oder eines Patchpakets, um den Wert dieser Eigenschaft in den Zusammenfassungs Informationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="bbc77-107">It is up to the author of an installation database, transform, or patch package to provide the value of this property in the summary information.</span></span> <span data-ttu-id="bbc77-108">Autoren sollten die folgenden Schritte ausführen, um den richtigen Wert zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="bbc77-108">Authors should do the following to determine the correct value.</span></span>

-   <span data-ttu-id="bbc77-109">Legen Sie in einem Installationspaket den Wert dieser Eigenschaft auf eine Liste von Schlüsselwörtern fest.</span><span class="sxs-lookup"><span data-stu-id="bbc77-109">In an installation package, set the value of this property to a list of keywords.</span></span> <span data-ttu-id="bbc77-110">Das Schlüsselwort sollte "Installer" und produktspezifische Schlüsselwörter enthalten und möglicherweise lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="bbc77-110">The keyword should include "Installer" as well as product-specific keywords, and may be localized.</span></span>
-   <span data-ttu-id="bbc77-111">Legen Sie in einer Transformation den Wert dieser Eigenschaft auf eine Liste von Schlüsselwörtern fest.</span><span class="sxs-lookup"><span data-stu-id="bbc77-111">In a transform, set the value of this property to a list of keywords.</span></span> <span data-ttu-id="bbc77-112">Das Schlüsselwort sollte "Installer" und produktspezifische Schlüsselwörter enthalten und möglicherweise lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="bbc77-112">The keyword should include "Installer" as well as product-specific keywords, and may be localized.</span></span>
-   <span data-ttu-id="bbc77-113">Legen Sie in einem Patchpaket den Wert dieser Eigenschaft auf eine durch Semikolons getrennte Liste von Netzwerk-oder URL-Speicherorten für die Quellen des Patches fest.</span><span class="sxs-lookup"><span data-stu-id="bbc77-113">In a patch package, set the value of this property to a semicolon-delimited list of network or URL locations for the sources of the patch.</span></span> <span data-ttu-id="bbc77-114">Wenn der Patch installiert ist, fügt das Installationsprogramm diese der Quell Liste für das Patchpaket hinzu.</span><span class="sxs-lookup"><span data-stu-id="bbc77-114">When the patch is installed, the installer adds these to the source list for the patch package.</span></span> <span data-ttu-id="bbc77-115">Wenn der zwischengespeicherte Patch fehlt, kann das Installationsprogramm eine Quelle am ursprünglichen Speicherort, einen Speicherort, der der Quell Liste von der **Schlüsselwort Zusammenfassungs** Eigenschaft hinzugefügt wurde, oder einen Speicherort, der der Quell Liste mithilfe der [**msisourcelistaddsource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) -Funktion oder der [**msisourcelistaddsourceex**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) -Funktion hinzugefügt wird, suchen.</span><span class="sxs-lookup"><span data-stu-id="bbc77-115">If the cached patch becomes missing, the installer can search for a source in the original location, a location added to the source list by the **Keywords Summary** property, or a location added to the source list using the [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) or [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbc77-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bbc77-116">Requirements</span></span>



| <span data-ttu-id="bbc77-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bbc77-117">Requirement</span></span> | <span data-ttu-id="bbc77-118">Wert</span><span class="sxs-lookup"><span data-stu-id="bbc77-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbc77-119">Version</span><span class="sxs-lookup"><span data-stu-id="bbc77-119">Version</span></span><br/> | <span data-ttu-id="bbc77-120">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bbc77-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bbc77-121">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bbc77-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bbc77-122">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="bbc77-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bbc77-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbc77-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbc77-124">Beschreibungen der Zusammenfassungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bbc77-124">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




