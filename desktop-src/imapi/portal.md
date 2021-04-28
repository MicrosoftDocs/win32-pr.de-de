---
title: ImageMastering-API
description: ImageMastering-API
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 641d9357496eb82a7e30f25a711928b16eeee2bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117578"
---
# <a name="image-mastering-api"></a><span data-ttu-id="2fe95-103">ImageMastering-API</span><span class="sxs-lookup"><span data-stu-id="2fe95-103">Image Mastering API</span></span>

## <a name="purpose"></a><span data-ttu-id="2fe95-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="2fe95-104">Purpose</span></span>

<span data-ttu-id="2fe95-105">Mit der Microsoft Windows-Imagemastering-API können Anwendungen Bilder auf optischen CD-, DVD- und Blu-Ray-Speichermedien bereitstellen und auf diese speichern.</span><span class="sxs-lookup"><span data-stu-id="2fe95-105">The Microsoft Windows image mastering API enables applications to stage and burn images to CD, DVD, and Blu-ray optical storage media.</span></span> <span data-ttu-id="2fe95-106">Andere datenträgerähnliche Medien, die Bilder auf die gleiche Weise ablegen, können diese API ebenfalls verwenden.</span><span class="sxs-lookup"><span data-stu-id="2fe95-106">Other disc-like media that lay images in the same manner can also use this API.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="2fe95-107">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="2fe95-107">Developer audience</span></span>

<span data-ttu-id="2fe95-108">IMAPI ist für C/C++- und Visual Basic-Entwickler sowie für Entwickler konzipiert, die Skripts mit VBScript schreiben.</span><span class="sxs-lookup"><span data-stu-id="2fe95-108">IMAPI is designed for C/C++ and Visual Basic developers and those writing scripts using VBScript.</span></span>

<span data-ttu-id="2fe95-109">Kenntnisse über CD-, DVD- und Blu-ray-Technologien und Dateisysteme werden empfohlen.</span><span class="sxs-lookup"><span data-stu-id="2fe95-109">Knowledge of CD, DVD, and Blu-ray technologies and file systems is recommended.</span></span> <span data-ttu-id="2fe95-110">Entwickler können von einer Vertrautheit mit der neuesten Revision von Multimedia command (MMC) unter [ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go)profitieren.</span><span class="sxs-lookup"><span data-stu-id="2fe95-110">Developers may benefit from a familiarity with the latest revision of Multimedia Command (MMC) at [ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="2fe95-111">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="2fe95-111">Run-time requirements</span></span>

<span data-ttu-id="2fe95-112">IMAPI 2.0 wird ab Windows Vista und Windows Server 2008 nativ unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2fe95-112">IMAPI 2.0 is supported natively starting with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="2fe95-113">Zum Aktivieren der IMAPI 2.0-Funktionalität für Windows XP und Windows Server 2003 muss das Updatepaket [KB932716](https://support.microsoft.com/kb/932716) installiert werden.</span><span class="sxs-lookup"><span data-stu-id="2fe95-113">Enabling IMAPI 2.0 functionality for Windows XP and Windows Server 2003 requires the installation of the [KB932716](https://support.microsoft.com/kb/932716) update package.</span></span> <span data-ttu-id="2fe95-114">Wenn dieses Paket nicht installiert ist, unterstützt Windows XP [IMAPI 1.0](imapiv1.md)weiterhin nativ.</span><span class="sxs-lookup"><span data-stu-id="2fe95-114">If this package is not installed, Windows XP still natively supports [IMAPI 1.0](imapiv1.md).</span></span>

> [!Note]  
> <span data-ttu-id="2fe95-115">Das Windows Feature Pack für Storage ist für die Öffentlichkeit über das [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2fe95-115">The Windows Feature Pack for Storage is available to the public via the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05).</span></span> <span data-ttu-id="2fe95-116">Weitere Informationen zu bestimmten API-Änderungen finden Sie im Abschnitt [Neuerungen.](what-s-new.md)</span><span class="sxs-lookup"><span data-stu-id="2fe95-116">Additional information regarding specific API changes can be found in the [What's New](what-s-new.md) section.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="2fe95-117">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="2fe95-117">In this section</span></span>



| <span data-ttu-id="2fe95-118">Thema</span><span class="sxs-lookup"><span data-stu-id="2fe95-118">Topic</span></span>                                             | <span data-ttu-id="2fe95-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fe95-119">Description</span></span>                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fe95-120">Neuerungen</span><span class="sxs-lookup"><span data-stu-id="2fe95-120">What's New</span></span>](what-s-new.md)<br/>           | <span data-ttu-id="2fe95-121">Informationen zu den einzelnen wichtigen Freigaben der ImageMastering-API.</span><span class="sxs-lookup"><span data-stu-id="2fe95-121">Information detailing each significant release of the Image Mastering API.</span></span><br/> |
| [<span data-ttu-id="2fe95-122">Informationen zu IMAPI</span><span class="sxs-lookup"><span data-stu-id="2fe95-122">About IMAPI</span></span>](about-imapi.md)<br/>         | <span data-ttu-id="2fe95-123">Allgemeine Informationen zur Imagemastering-API.</span><span class="sxs-lookup"><span data-stu-id="2fe95-123">General information about the Image Mastering API.</span></span><br/>                         |
| [<span data-ttu-id="2fe95-124">Verwenden von IMAPI</span><span class="sxs-lookup"><span data-stu-id="2fe95-124">Using IMAPI</span></span>](using-imapi.md)<br/>         | <span data-ttu-id="2fe95-125">Aufgabenbezogene Themen, die die Verwendung der Imagemastering-API veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="2fe95-125">Task-related topics that demonstrate how to use the Image Mastering API.</span></span><br/>   |
| [<span data-ttu-id="2fe95-126">IMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="2fe95-126">IMAPI Reference</span></span>](imapi-reference.md)<br/> | <span data-ttu-id="2fe95-127">Ausführliche Beschreibungen von IMAPI-Schnittstellen und anderen Programmierelementen.</span><span class="sxs-lookup"><span data-stu-id="2fe95-127">Detailed descriptions of IMAPI interfaces and other programming elements.</span></span><br/>  |



 

## <a name="additional-resources"></a><span data-ttu-id="2fe95-128">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2fe95-128">Additional resources</span></span>

<span data-ttu-id="2fe95-129">Weitere Informationen zu IMAPI und anderen verwandten Themen finden Sie an den folgenden Stellen:</span><span class="sxs-lookup"><span data-stu-id="2fe95-129">Further information regarding IMAPI and other related subjects can be found at the following locations:</span></span>



|                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2fe95-130">Microsoft Optical Storage Blog</span><span class="sxs-lookup"><span data-stu-id="2fe95-130">Microsoft Optical Storage Blog</span></span>](/archive/blogs/opticalstorage/)                | <span data-ttu-id="2fe95-131">Hebt Themen hervor, die sich auf die Implementierung der Bildmaster-API in realen Entwicklungsszenarien konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="2fe95-131">Highlights topics that focus on the implementation of the Image Mastering API in real world development scenarios.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="2fe95-132">Diskussionsforum zur optischen Plattform</span><span class="sxs-lookup"><span data-stu-id="2fe95-132">Optical Platform Discussion Forum</span></span>](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | <span data-ttu-id="2fe95-133">Erläutern CDROM.SYS, IMAPIv2- und Live File System-Problemen.</span><span class="sxs-lookup"><span data-stu-id="2fe95-133">Discuss CDROM.SYS, IMAPIv2 and Live File System issues.</span></span> <span data-ttu-id="2fe95-134">Dieses Forum konzentriert sich auf Themen auf Systemebene und ist für Anwendungsentwickler und nicht für Endbenutzer vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="2fe95-134">This forum focuses on system-level topics and is intended for application developers rather than endusers.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="2fe95-135">T10 Technical Committee</span><span class="sxs-lookup"><span data-stu-id="2fe95-135">T10 Technical Committee</span></span>](https://www.t10.org/)                       | <span data-ttu-id="2fe95-136">Ein technischer Ausschuss des InterNational-Ausschuss für Informationstechnologiestandards (INCITS, ausgesprochen als "Erkenntnisse").</span><span class="sxs-lookup"><span data-stu-id="2fe95-136">A Technical Committee of the InterNational Committee on Information Technology Standards (INCITS, pronounced "insights").</span></span> <span data-ttu-id="2fe95-137">INCITS wird von der Ansi (American National Standards Institute) zugelassen und arbeitet gemäß diesen Regeln.</span><span class="sxs-lookup"><span data-stu-id="2fe95-137">INCITS is accredited by, and operates under rules that are approved by, the American National Standards Institute (ANSI).</span></span> <span data-ttu-id="2fe95-138">Diese Regeln sollen sicherstellen, dass freiwillige Standards durch den Konsens von Branchengruppen entwickelt werden.</span><span class="sxs-lookup"><span data-stu-id="2fe95-138">These rules are designed to ensure that voluntary standards are developed by the consensus of industry groups.</span></span> |
| [<span data-ttu-id="2fe95-139">Optical Storage Technology Association (LAGERUNG)</span><span class="sxs-lookup"><span data-stu-id="2fe95-139">Optical Storage Technology Association (OSTA)</span></span>](http://www.osta.org/) | <span data-ttu-id="2fe95-140">Arbeitet an der Gestaltung der Zukunft der Branche durch regelmäßige Besprechungen von kommerziellen optischen Speicheranwendungen (Commercial Optical Storage Applications, COSA), DVD-Kompatibilität, Marketing, MPV (MusicPhotoVideo), UDF-Sprechungen und einem neuen Ad-hoc-BlueScan-Ausschuss.</span><span class="sxs-lookup"><span data-stu-id="2fe95-140">Works to shape the future of the industry through regular meetings of Commercial Optical Storage Applications (COSA), DVD Compatibility, Marketing, MPV (MusicPhotoVideo), UDF committees, and a new adhoc Blue Laser committee.</span></span> <span data-ttu-id="2fe95-141">Interessierten Unternehmen auf der ganzen Welt werden eingeladen, der Organisation beizunehmen und an deren Programmen und Programmen teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="2fe95-141">Interested companies worldwide are invited to join the organization and participate in its committees and programs.</span></span>               |



 

 

