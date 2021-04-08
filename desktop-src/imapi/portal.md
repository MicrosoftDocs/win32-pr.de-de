---
title: Bild-Mastering-API
description: .
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc23c972cf111dee5edf3cb014a52351eda3605e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "103949194"
---
# <a name="image-mastering-api"></a><span data-ttu-id="95ef9-103">Bild-Mastering-API</span><span class="sxs-lookup"><span data-stu-id="95ef9-103">Image Mastering API</span></span>

## <a name="purpose"></a><span data-ttu-id="95ef9-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="95ef9-104">Purpose</span></span>

<span data-ttu-id="95ef9-105">Die Microsoft Windows-Abbild-Mastering-API ermöglicht Anwendungen das Staging und Brennen von Bildern auf optischen CD-, DVD-und Blu-Ray-Speichermedien.</span><span class="sxs-lookup"><span data-stu-id="95ef9-105">The Microsoft Windows image mastering API enables applications to stage and burn images to CD, DVD, and Blu-ray optical storage media.</span></span> <span data-ttu-id="95ef9-106">Andere auf dem Bild Platten ähnliche Medien, die Bilder auf die gleiche Weise aufstellen, können diese API ebenfalls verwenden.</span><span class="sxs-lookup"><span data-stu-id="95ef9-106">Other disc-like media that lay images in the same manner can also use this API.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="95ef9-107">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="95ef9-107">Developer audience</span></span>

<span data-ttu-id="95ef9-108">IMAPI ist für C/C++-und Visual Basic-Entwickler und solche konzipiert, die Skripts mithilfe von VBScript schreiben.</span><span class="sxs-lookup"><span data-stu-id="95ef9-108">IMAPI is designed for C/C++ and Visual Basic developers and those writing scripts using VBScript.</span></span>

<span data-ttu-id="95ef9-109">Es wird empfohlen, auf CD-, DVD-und Blu-Ray-Technologien und Dateisysteme zu wissen.</span><span class="sxs-lookup"><span data-stu-id="95ef9-109">Knowledge of CD, DVD, and Blu-ray technologies and file systems is recommended.</span></span> <span data-ttu-id="95ef9-110">Entwickler können von einer Vertrautheit mit der neuesten Revision von Multimedia Command (MMC) unter [FTP://FTP.T10.org/T10/Drafts/mmc6](https://www.microsoft.com/?ref=go)profitieren.</span><span class="sxs-lookup"><span data-stu-id="95ef9-110">Developers may benefit from a familiarity with the latest revision of Multimedia Command (MMC) at [ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="95ef9-111">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="95ef9-111">Run-time requirements</span></span>

<span data-ttu-id="95ef9-112">IMAPI 2,0 wird nativ unterstützt, beginnend mit Windows Vista und Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="95ef9-112">IMAPI 2.0 is supported natively starting with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="95ef9-113">Um die IMAPI 2,0-Funktionalität für Windows XP und Windows Server 2003 zu aktivieren, muss das [KB932716](https://support.microsoft.com/kb/932716) -Update Paket installiert werden.</span><span class="sxs-lookup"><span data-stu-id="95ef9-113">Enabling IMAPI 2.0 functionality for Windows XP and Windows Server 2003 requires the installation of the [KB932716](https://support.microsoft.com/kb/932716) update package.</span></span> <span data-ttu-id="95ef9-114">Wenn dieses Paket nicht installiert ist, unterstützt Windows XP weiterhin nativ [IMAPI 1,0](imapiv1.md).</span><span class="sxs-lookup"><span data-stu-id="95ef9-114">If this package is not installed, Windows XP still natively supports [IMAPI 1.0](imapiv1.md).</span></span>

> [!Note]  
> <span data-ttu-id="95ef9-115">Das Windows Feature Pack für Storage steht dem öffentlichen über das [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05)zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="95ef9-115">The Windows Feature Pack for Storage is available to the public via the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05).</span></span> <span data-ttu-id="95ef9-116">Weitere Informationen zu bestimmten API-Änderungen finden Sie im Abschnitt [Neuerungen](what-s-new.md) .</span><span class="sxs-lookup"><span data-stu-id="95ef9-116">Additional information regarding specific API changes can be found in the [What's New](what-s-new.md) section.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="95ef9-117">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="95ef9-117">In this section</span></span>



| <span data-ttu-id="95ef9-118">Thema</span><span class="sxs-lookup"><span data-stu-id="95ef9-118">Topic</span></span>                                             | <span data-ttu-id="95ef9-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95ef9-119">Description</span></span>                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="95ef9-120">Neuerungen</span><span class="sxs-lookup"><span data-stu-id="95ef9-120">What's New</span></span>](what-s-new.md)<br/>           | <span data-ttu-id="95ef9-121">Informationen, die jede bedeutende Version der Image-Mastering-API beschreiben.</span><span class="sxs-lookup"><span data-stu-id="95ef9-121">Information detailing each significant release of the Image Mastering API.</span></span><br/> |
| [<span data-ttu-id="95ef9-122">Informationen zu IMAPI</span><span class="sxs-lookup"><span data-stu-id="95ef9-122">About IMAPI</span></span>](about-imapi.md)<br/>         | <span data-ttu-id="95ef9-123">Allgemeine Informationen zur Image-Mastering-API.</span><span class="sxs-lookup"><span data-stu-id="95ef9-123">General information about the Image Mastering API.</span></span><br/>                         |
| [<span data-ttu-id="95ef9-124">Verwenden von IMAPI</span><span class="sxs-lookup"><span data-stu-id="95ef9-124">Using IMAPI</span></span>](using-imapi.md)<br/>         | <span data-ttu-id="95ef9-125">Aufgabenbezogene Themen, die veranschaulichen, wie die Image-Mastering-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="95ef9-125">Task-related topics that demonstrate how to use the Image Mastering API.</span></span><br/>   |
| [<span data-ttu-id="95ef9-126">IMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="95ef9-126">IMAPI Reference</span></span>](imapi-reference.md)<br/> | <span data-ttu-id="95ef9-127">Ausführliche Beschreibungen von IMAPI-Schnittstellen und anderen Programmier Elementen.</span><span class="sxs-lookup"><span data-stu-id="95ef9-127">Detailed descriptions of IMAPI interfaces and other programming elements.</span></span><br/>  |



 

## <a name="additional-resources"></a><span data-ttu-id="95ef9-128">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="95ef9-128">Additional resources</span></span>

<span data-ttu-id="95ef9-129">Weitere Informationen zu IMAPI und anderen verwandten Themen finden Sie unter den folgenden Speicherorten:</span><span class="sxs-lookup"><span data-stu-id="95ef9-129">Further information regarding IMAPI and other related subjects can be found at the following locations:</span></span>



|                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95ef9-130">Blog zu optischen Microsoft-Speicher</span><span class="sxs-lookup"><span data-stu-id="95ef9-130">Microsoft Optical Storage Blog</span></span>](/archive/blogs/opticalstorage/)                | <span data-ttu-id="95ef9-131">Hebt Themen hervor, die sich auf die Implementierung der Image-Mastering-API in realen Entwicklungsszenarien konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="95ef9-131">Highlights topics that focus on the implementation of the Image Mastering API in real world development scenarios.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="95ef9-132">Forum zur optischen Platt Form Diskussion</span><span class="sxs-lookup"><span data-stu-id="95ef9-132">Optical Platform Discussion Forum</span></span>](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | <span data-ttu-id="95ef9-133">Erörtern Sie Probleme mit CDROM.SYS, IMAPIv2 und Live File System.</span><span class="sxs-lookup"><span data-stu-id="95ef9-133">Discuss CDROM.SYS, IMAPIv2 and Live File System issues.</span></span> <span data-ttu-id="95ef9-134">Dieses Forum konzentriert sich auf Themen auf Systemebene und ist eher für Anwendungsentwickler als auch für ender vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="95ef9-134">This forum focuses on system-level topics and is intended for application developers rather than endusers.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="95ef9-135">T10 Technical Committee</span><span class="sxs-lookup"><span data-stu-id="95ef9-135">T10 Technical Committee</span></span>](https://www.t10.org/)                       | <span data-ttu-id="95ef9-136">Ein technisches Committee des internationalen Komitees zu Informationstechnologie Standards ("Einblicke").</span><span class="sxs-lookup"><span data-stu-id="95ef9-136">A Technical Committee of the InterNational Committee on Information Technology Standards (INCITS, pronounced "insights").</span></span> <span data-ttu-id="95ef9-137">Die aufhetzen werden von der-American National Standards Institute (ANSI) genehmigt und unter Regeln angewendet, die von genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="95ef9-137">INCITS is accredited by, and operates under rules that are approved by, the American National Standards Institute (ANSI).</span></span> <span data-ttu-id="95ef9-138">Diese Regeln stellen sicher, dass die freiwillig geltenden Standards durch den Konsens von Branchengruppen entwickelt werden.</span><span class="sxs-lookup"><span data-stu-id="95ef9-138">These rules are designed to ensure that voluntary standards are developed by the consensus of industry groups.</span></span> |
| [<span data-ttu-id="95ef9-139">Optical Storage Technology Association (OSTA)</span><span class="sxs-lookup"><span data-stu-id="95ef9-139">Optical Storage Technology Association (OSTA)</span></span>](http://www.osta.org/) | <span data-ttu-id="95ef9-140">Funktioniert, um die Zukunft der Branche durch reguläre Besprechungen von kommerziellen optischen Speicheranwendungen (Cosa), DVD-Kompatibilität, Marketing, MPV (musicphotovideo), UDF-Komitees und ein neues Adhoc Blue Laser Committee zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="95ef9-140">Works to shape the future of the industry through regular meetings of Commercial Optical Storage Applications (COSA), DVD Compatibility, Marketing, MPV (MusicPhotoVideo), UDF committees, and a new adhoc Blue Laser committee.</span></span> <span data-ttu-id="95ef9-141">Interessierte Unternehmen in der ganzen Welt sind eingeladen, der Organisation beizutreten und an Ihren Ausschüssen und Programmen teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="95ef9-141">Interested companies worldwide are invited to join the organization and participate in its committees and programs.</span></span>               |



 

 

