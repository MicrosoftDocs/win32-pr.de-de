---
description: Die SourceList-Eigenschaft ist eine durch Semikolons getrennte Liste der Netzwerk-oder URL-Quell Pfade zum Installationspaket der Anwendung.
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: SourceList-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5384504c337aeb9f1848f59efb2c6abaee5887b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359228"
---
# <a name="sourcelist-property"></a><span data-ttu-id="fbce5-103">SourceList-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fbce5-103">SOURCELIST property</span></span>

<span data-ttu-id="fbce5-104">Die **SourceList** -Eigenschaft ist eine durch Semikolons getrennte Liste der Netzwerk-oder URL-Quell Pfade zum Installationspaket der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="fbce5-104">The **SOURCELIST** property is a semicolon-delimited list of network or URL source paths to the application's installation package.</span></span> <span data-ttu-id="fbce5-105">Diese Liste wird an das Ende der vorhandenen Quell Liste der einzelnen Benutzer für die Anwendung angehängt.</span><span class="sxs-lookup"><span data-stu-id="fbce5-105">This list is appended to the end of each user's existing source list for the application.</span></span> <span data-ttu-id="fbce5-106">Der Installer sucht eine Quelle, indem er die Liste der Quell Pfade auflistet und den ersten zugänglichen Speicherort verwendet, den er findet.</span><span class="sxs-lookup"><span data-stu-id="fbce5-106">The installer locates a source by enumerating the list of source paths and uses the first accessible location it finds.</span></span> <span data-ttu-id="fbce5-107">Nur diese Quelle kann für den Rest der Installation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbce5-107">Only this source can be used for the remainder of the installation.</span></span> <span data-ttu-id="fbce5-108">Jeder in der Quell Liste angegebene Pfad muss sich daher an einem Speicherort befinden, der über eine komplette Quelle für die Anwendung verfügt.</span><span class="sxs-lookup"><span data-stu-id="fbce5-108">Each path specified in the source list must therefore be to a location having a complete source for the application.</span></span> <span data-ttu-id="fbce5-109">Die gesamte Verzeichnisstruktur an jedem Quell Speicherort muss identisch sein, und Sie muss alle erforderlichen Quelldateien einschließlich aller Schränke enthalten.</span><span class="sxs-lookup"><span data-stu-id="fbce5-109">The entire directory tree at each source location must be the same and must include all of the required source files, including any cabinets.</span></span> <span data-ttu-id="fbce5-110">Jeder Speicherort muss über eine MSI-Datei mit demselben Dateinamen und Produktcode verfügen.</span><span class="sxs-lookup"><span data-stu-id="fbce5-110">Each location must have an .msi file with the same file name and product code.</span></span>

## <a name="default-value"></a><span data-ttu-id="fbce5-111">Standardwert</span><span class="sxs-lookup"><span data-stu-id="fbce5-111">Default Value</span></span>

<span data-ttu-id="fbce5-112">Das Installationsprogramm überprüft nur die **SourceList** -Eigenschaft, wenn das Produkt nicht bereits angekündigt oder installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="fbce5-112">The installer only checks the **SOURCELIST** property if the product has not already been advertised or installed.</span></span> <span data-ttu-id="fbce5-113">In allen anderen Fällen verwendet das Installationsprogramm die vorhandene Quell Liste in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="fbce5-113">In all other cases the installer uses the existing source list that is in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbce5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbce5-114">Remarks</span></span>

<span data-ttu-id="fbce5-115">Quellen, die mithilfe der **SourceList** -Eigenschaft hinzugefügt werden, werden für jeden Quelltyp direkt am Ende der Liste hinzugefügt und sind immer nach der Standard Quelle, die von der [**SourceDir**](sourcedir.md) -Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fbce5-115">Sources added using the **SOURCELIST** property are added directly to the end of the list for each type of source and always come after the default source specified by the [**SourceDir**](sourcedir.md) property.</span></span>

<span data-ttu-id="fbce5-116">Bei Windows Installer die Anzahl der Quellen in der **SourceList** -Eigenschaft unbegrenzt sein.</span><span class="sxs-lookup"><span data-stu-id="fbce5-116">For Windows Installer the number of sources in the **SOURCELIST** property is unlimited.</span></span> <span data-ttu-id="fbce5-117">[**Msisourcelistaddsource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) kann zum Hinzufügen von Netzwerk Quellen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbce5-117">[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) can be used to add network sources.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbce5-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbce5-118">Requirements</span></span>



| <span data-ttu-id="fbce5-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbce5-119">Requirement</span></span> | <span data-ttu-id="fbce5-120">Wert</span><span class="sxs-lookup"><span data-stu-id="fbce5-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbce5-121">Version</span><span class="sxs-lookup"><span data-stu-id="fbce5-121">Version</span></span><br/> | <span data-ttu-id="fbce5-122">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fbce5-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fbce5-123">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fbce5-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fbce5-124">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fbce5-124">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="fbce5-125">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="fbce5-125">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fbce5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbce5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbce5-127">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fbce5-127">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="fbce5-128">Quellen Resilienz</span><span class="sxs-lookup"><span data-stu-id="fbce5-128">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




