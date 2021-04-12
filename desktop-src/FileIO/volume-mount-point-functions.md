---
description: Funktionen, die zum Verwalten bereitgestellter Ordner verwendet werden.
ms.assetid: 2624500b-11d6-4892-97d7-22efa450f681
title: Funktionen für bereitgestellte Ordner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e984b9bee902f11af9d7b2b956ea0681cd6e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346079"
---
# <a name="mounted-folder-functions"></a><span data-ttu-id="de406-103">Funktionen für bereitgestellte Ordner</span><span class="sxs-lookup"><span data-stu-id="de406-103">Mounted Folder Functions</span></span>

<span data-ttu-id="de406-104">Die Funktionen für den bereitgestellten Ordner können in drei Gruppen unterteilt werden: allgemeine Funktionen, Funktionen, die für die Suche nach Volumes verwendet werden, und Funktionen, die zum Scannen eines Volumes für bereitgestellte Ordner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de406-104">The mounted folder functions can be divided into three groups: general-purpose functions, functions used to scan for volumes, and functions used to scan a volume for mounted folders.</span></span>

## <a name="general-purpose-mounted-folder-functions"></a><span data-ttu-id="de406-105">Bereitgestellte Ordner Funktionen General-Purpose</span><span class="sxs-lookup"><span data-stu-id="de406-105">General-Purpose Mounted Folder Functions</span></span>



| <span data-ttu-id="de406-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="de406-106">Function</span></span>                                                                     | <span data-ttu-id="de406-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de406-107">Description</span></span>                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de406-108">**DeleteVolumeMountPoint**</span><span class="sxs-lookup"><span data-stu-id="de406-108">**DeleteVolumeMountPoint**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw)                     | <span data-ttu-id="de406-109">Löscht einen Laufwerk Buchstaben oder einen bereitgestellten Ordner.</span><span class="sxs-lookup"><span data-stu-id="de406-109">Deletes a drive letter or mounted folder.</span></span>                                                                                                                   |
| [<span data-ttu-id="de406-110">**Getvolumenameforvolumemountpoint**</span><span class="sxs-lookup"><span data-stu-id="de406-110">**GetVolumeNameForVolumeMountPoint**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) | <span data-ttu-id="de406-111">Ruft den Volume-GUID-Pfad für das Volume ab, das dem angegebenen volumeeinstellungspunkt (Laufwerk Buchstabe, VolumeGuid-Pfad oder eingebundener Ordner) zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="de406-111">Retrieves the volume GUID path for the volume that is associated with the specified volume mount point (drive letter, volume GUID path, or mounted folder).</span></span> |
| [<span data-ttu-id="de406-112">**Getvolumepathname**</span><span class="sxs-lookup"><span data-stu-id="de406-112">**GetVolumePathName**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumepathnamew)                               | <span data-ttu-id="de406-113">Ruft den bereitgestellten Ordner ab, der dem angegebenen Volume zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="de406-113">Retrieves the mounted folder that is associated with the specified volume.</span></span>                                                                                  |
| [<span data-ttu-id="de406-114">**Setvolumemountpoint**</span><span class="sxs-lookup"><span data-stu-id="de406-114">**SetVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa)                           | <span data-ttu-id="de406-115">Ordnet ein Volume einem Laufwerk Buchstaben oder einem Verzeichnis auf einem anderen Volume zu.</span><span class="sxs-lookup"><span data-stu-id="de406-115">Associates a volume with a drive letter or a directory on another volume.</span></span>                                                                                   |



 

## <a name="volume-scanning-functions"></a><span data-ttu-id="de406-116">Volume-Scanning Funktionen</span><span class="sxs-lookup"><span data-stu-id="de406-116">Volume-Scanning Functions</span></span>



| <span data-ttu-id="de406-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="de406-117">Function</span></span>                                   | <span data-ttu-id="de406-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de406-118">Description</span></span>                                                                                                                                    |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de406-119">**Findfirstvolume**</span><span class="sxs-lookup"><span data-stu-id="de406-119">**FindFirstVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) | <span data-ttu-id="de406-120">Gibt den Namen eines Volumes auf einem Computer zurück.</span><span class="sxs-lookup"><span data-stu-id="de406-120">Returns the name of a volume on a computer.</span></span> <span data-ttu-id="de406-121">" [**Findfirstvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) " wird verwendet, um mit dem Auflisten der Volumes eines Computers zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="de406-121">[**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew) is used to begin enumerating the volumes of a computer.</span></span> |
| [<span data-ttu-id="de406-122">**Findnextvolume**</span><span class="sxs-lookup"><span data-stu-id="de406-122">**FindNextVolume**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextvolumew)   | <span data-ttu-id="de406-123">Setzt eine volumesuche fort, die durch einen Befehl von [**findfirstvolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew)gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="de406-123">Continues a volume search started by a call to [**FindFirstVolume**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstvolumew).</span></span>                                                     |
| [<span data-ttu-id="de406-124">**Findvolumeclose**</span><span class="sxs-lookup"><span data-stu-id="de406-124">**FindVolumeClose**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findvolumeclose) | <span data-ttu-id="de406-125">Schließt eine Suche nach Volumes.</span><span class="sxs-lookup"><span data-stu-id="de406-125">Closes a search for volumes.</span></span>                                                                                                                   |



 

## <a name="mounted-folder-scanning-functions"></a><span data-ttu-id="de406-126">Scanfunktionen für eingebundene Ordner</span><span class="sxs-lookup"><span data-stu-id="de406-126">Mounted Folder Scanning Functions</span></span>



| <span data-ttu-id="de406-127">Funktion</span><span class="sxs-lookup"><span data-stu-id="de406-127">Function</span></span>                                                       | <span data-ttu-id="de406-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de406-128">Description</span></span>                                                                                                                                                                               |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de406-129">**Findfirstvolumemountpoint**</span><span class="sxs-lookup"><span data-stu-id="de406-129">**FindFirstVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) | <span data-ttu-id="de406-130">Ruft den Namen eines eingebundenen Ordners auf dem angegebenen Volume ab.</span><span class="sxs-lookup"><span data-stu-id="de406-130">Retrieves the name of a mounted folder on the specified volume.</span></span> <span data-ttu-id="de406-131">[**Findfirstvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) wird verwendet, um mit dem Scannen der bereitgestellten Ordner auf einem Volume zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="de406-131">[**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa) is used to begin scanning the mounted folders on a volume.</span></span> |
| [<span data-ttu-id="de406-132">**Findnextvolumemountpoint**</span><span class="sxs-lookup"><span data-stu-id="de406-132">**FindNextVolumeMountPoint**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findnextvolumemountpointa)   | <span data-ttu-id="de406-133">Setzt eine bereitgestellte Ordner Suche fort, die durch einen Befehl von [**findfirstvolumemountpoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa)gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="de406-133">Continues a mounted folder search started by a call to [**FindFirstVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-findfirstvolumemountpointa).</span></span>                                                                    |
| [<span data-ttu-id="de406-134">**Findvolumemountpointclose**</span><span class="sxs-lookup"><span data-stu-id="de406-134">**FindVolumeMountPointClose**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findvolumemountpointclose) | <span data-ttu-id="de406-135">Schließt eine Suche nach bereitgestellten Ordnern.</span><span class="sxs-lookup"><span data-stu-id="de406-135">Closes a search for mounted folders.</span></span>                                                                                                                                                      |



 

 

 



