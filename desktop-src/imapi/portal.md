---
title: Bildmaster-API
description: Bildmaster-API
ms.assetid: 4902d3fb-3195-4909-ab64-28f8a77ba14c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fabf41d1c82420709b39bb5db03c2ac3e851d2
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119676"
---
# <a name="image-mastering-api"></a><span data-ttu-id="9f0b6-103">Bildmaster-API</span><span class="sxs-lookup"><span data-stu-id="9f0b6-103">Image Mastering API</span></span>

## <a name="purpose"></a><span data-ttu-id="9f0b6-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="9f0b6-104">Purpose</span></span>

<span data-ttu-id="9f0b6-105">Mit der Microsoft Windows-Imagemastering-API können Anwendungen Bilder auf cd-, DVD- und Blu-ray-Optische Speichermedien stagen und darauf speichern.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-105">The Microsoft Windows image mastering API enables applications to stage and burn images to CD, DVD, and Blu-ray optical storage media.</span></span> <span data-ttu-id="9f0b6-106">Andere datenträgerbasierte Medien, die Bilder auf die gleiche Weise erstellen, können diese API ebenfalls verwenden.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-106">Other disc-like media that lay images in the same manner can also use this API.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9f0b6-107">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="9f0b6-107">Developer audience</span></span>

<span data-ttu-id="9f0b6-108">IMAPI ist für C/C++- und Visual Basic entwickler sowie für Entwickler konzipiert, die Skripts mit VBScript schreiben.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-108">IMAPI is designed for C/C++ and Visual Basic developers and those writing scripts using VBScript.</span></span>

<span data-ttu-id="9f0b6-109">Kenntnisse über CD-, DVD- und Blu-ray-Technologien und Dateisysteme werden empfohlen.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-109">Knowledge of CD, DVD, and Blu-ray technologies and file systems is recommended.</span></span> <span data-ttu-id="9f0b6-110">Entwickler können von einer vertrauten Version des Multimedia-Befehls (MMC) bei [ftp://ftp.t10.org/t10/drafts/mmc6.](https://www.microsoft.com/?ref=go)</span><span class="sxs-lookup"><span data-stu-id="9f0b6-110">Developers may benefit from a familiarity with the latest revision of Multimedia Command (MMC) at [ftp://ftp.t10.org/t10/drafts/mmc6](https://www.microsoft.com/?ref=go).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9f0b6-111">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="9f0b6-111">Run-time requirements</span></span>

<span data-ttu-id="9f0b6-112">IMAPI 2.0 wird ab Windows Vista und Windows Server 2008 nativ unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-112">IMAPI 2.0 is supported natively starting with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="9f0b6-113">Zum Aktivieren der IMAPI 2.0-Funktionalität für Windows XP und Windows Server 2003 muss das [Updatepaket KB932716](https://support.microsoft.com/kb/932716) installiert werden.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-113">Enabling IMAPI 2.0 functionality for Windows XP and Windows Server 2003 requires the installation of the [KB932716](https://support.microsoft.com/kb/932716) update package.</span></span> <span data-ttu-id="9f0b6-114">Wenn dieses Paket nicht installiert ist, unterstützt Windows XP weiterhin [nativ IMAPI 1.0.](imapiv1.md)</span><span class="sxs-lookup"><span data-stu-id="9f0b6-114">If this package is not installed, Windows XP still natively supports [IMAPI 1.0](imapiv1.md).</span></span>

> [!Note]  
> <span data-ttu-id="9f0b6-115">Das Windows Feature Pack für Storage ist für die Öffentlichkeit über das [Microsoft Download Center verfügbar.](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05)</span><span class="sxs-lookup"><span data-stu-id="9f0b6-115">The Windows Feature Pack for Storage is available to the public via the [Microsoft Download Center](https://www.microsoft.com/downloads/details.aspx?FamilyID=63ab51ea-99c9-45c0-980a-c556746fcf05).</span></span> <span data-ttu-id="9f0b6-116">Weitere Informationen zu bestimmten API-Änderungen finden Sie im Abschnitt [Neuerungen.](what-s-new.md)</span><span class="sxs-lookup"><span data-stu-id="9f0b6-116">Additional information regarding specific API changes can be found in the [What's New](what-s-new.md) section.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="9f0b6-117">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9f0b6-117">In this section</span></span>



| <span data-ttu-id="9f0b6-118">Thema</span><span class="sxs-lookup"><span data-stu-id="9f0b6-118">Topic</span></span>                                             | <span data-ttu-id="9f0b6-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f0b6-119">Description</span></span>                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f0b6-120">Neuerungen</span><span class="sxs-lookup"><span data-stu-id="9f0b6-120">What's New</span></span>](what-s-new.md)<br/>           | <span data-ttu-id="9f0b6-121">Informationen zu jedem wichtigen Release der Imagemaster-API.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-121">Information detailing each significant release of the Image Mastering API.</span></span><br/> |
| [<span data-ttu-id="9f0b6-122">Informationen zu IMAPI</span><span class="sxs-lookup"><span data-stu-id="9f0b6-122">About IMAPI</span></span>](about-imapi.md)<br/>         | <span data-ttu-id="9f0b6-123">Allgemeine Informationen zur Imagemastering-API.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-123">General information about the Image Mastering API.</span></span><br/>                         |
| [<span data-ttu-id="9f0b6-124">Verwenden von IMAPI</span><span class="sxs-lookup"><span data-stu-id="9f0b6-124">Using IMAPI</span></span>](using-imapi.md)<br/>         | <span data-ttu-id="9f0b6-125">Aufgabenbezogene Themen, die die Verwendung der Bildmaster-API veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-125">Task-related topics that demonstrate how to use the Image Mastering API.</span></span><br/>   |
| [<span data-ttu-id="9f0b6-126">IMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="9f0b6-126">IMAPI Reference</span></span>](imapi-reference.md)<br/> | <span data-ttu-id="9f0b6-127">Ausführliche Beschreibungen von IMAPI-Schnittstellen und anderen Programmierelementen.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-127">Detailed descriptions of IMAPI interfaces and other programming elements.</span></span><br/>  |



 

## <a name="additional-resources"></a><span data-ttu-id="9f0b6-128">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9f0b6-128">Additional resources</span></span>

<span data-ttu-id="9f0b6-129">Weitere Informationen zu IMAPI und anderen verwandten Themen finden Sie an den folgenden Stellen:</span><span class="sxs-lookup"><span data-stu-id="9f0b6-129">Further information regarding IMAPI and other related subjects can be found at the following locations:</span></span>



| <span data-ttu-id="9f0b6-130">Thema</span><span class="sxs-lookup"><span data-stu-id="9f0b6-130">Topic</span></span>                                                                                                 | <span data-ttu-id="9f0b6-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9f0b6-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f0b6-132">Microsoft Optical Storage Blog</span><span class="sxs-lookup"><span data-stu-id="9f0b6-132">Microsoft Optical Storage Blog</span></span>](/archive/blogs/opticalstorage/)                | <span data-ttu-id="9f0b6-133">Hebt Themen hervor, die sich auf die Implementierung der Bildmaster-API in realen Entwicklungsszenarien konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-133">Highlights topics that focus on the implementation of the Image Mastering API in real world development scenarios.</span></span>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="9f0b6-134">Diskussionsforum zur optischen Plattform</span><span class="sxs-lookup"><span data-stu-id="9f0b6-134">Optical Platform Discussion Forum</span></span>](https://social.msdn.microsoft.com/forums/windowsopticalplatform/threads/)              | <span data-ttu-id="9f0b6-135">Erläutern CDROM.SYS, IMAPIv2- und Live File System-Problemen.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-135">Discuss CDROM.SYS, IMAPIv2 and Live File System issues.</span></span> <span data-ttu-id="9f0b6-136">Dieses Forum konzentriert sich auf Themen auf Systemebene und ist für Anwendungsentwickler und nicht für Endbenutzer vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-136">This forum focuses on system-level topics and is intended for application developers rather than endusers.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="9f0b6-137">T10 Technical Committee</span><span class="sxs-lookup"><span data-stu-id="9f0b6-137">T10 Technical Committee</span></span>](https://www.t10.org/)                       | <span data-ttu-id="9f0b6-138">Ein technischer Ausschuss des InterNational-Ausschuss für Informationstechnologiestandards (INCITS, ausgesprochen als "Erkenntnisse").</span><span class="sxs-lookup"><span data-stu-id="9f0b6-138">A Technical Committee of the InterNational Committee on Information Technology Standards (INCITS, pronounced "insights").</span></span> <span data-ttu-id="9f0b6-139">INCITS wird von der Ansi (American National Standards Institute) zugelassen und arbeitet gemäß diesen Regeln.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-139">INCITS is accredited by, and operates under rules that are approved by, the American National Standards Institute (ANSI).</span></span> <span data-ttu-id="9f0b6-140">Diese Regeln sollen sicherstellen, dass freiwillige Standards durch den Konsens von Branchengruppen entwickelt werden.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-140">These rules are designed to ensure that voluntary standards are developed by the consensus of industry groups.</span></span> |
| [<span data-ttu-id="9f0b6-141">Optical Storage Technology Association (LAGERUNG)</span><span class="sxs-lookup"><span data-stu-id="9f0b6-141">Optical Storage Technology Association (OSTA)</span></span>](http://www.osta.org/) | <span data-ttu-id="9f0b6-142">Arbeitet an der Gestaltung der Zukunft der Branche durch regelmäßige Besprechungen von kommerziellen optischen Speicheranwendungen (Commercial Optical Storage Applications, COSA), DVD-Kompatibilität, Marketing, MPV (MusicPhotoVideo), UDF-Sprechungen und einem neuen Ad-hoc-BlueScan-Ausschuss.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-142">Works to shape the future of the industry through regular meetings of Commercial Optical Storage Applications (COSA), DVD Compatibility, Marketing, MPV (MusicPhotoVideo), UDF committees, and a new adhoc Blue Laser committee.</span></span> <span data-ttu-id="9f0b6-143">Interessierten Unternehmen auf der ganzen Welt werden eingeladen, der Organisation beizunehmen und an deren Programmen und Programmen teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="9f0b6-143">Interested companies worldwide are invited to join the organization and participate in its committees and programs.</span></span>               |



 

 

