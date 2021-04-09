---
title: Start der Windows-Abbild Datei (wimboot)
description: Start der Windows-Abbild Datei (wimboot)
ms.assetid: 1C4EFC42-6698-4981-8C55-D1DFC6309F31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f14ea506226e2c16d771ecec52fa31a8c871b4
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "103734641"
---
# <a name="windows-image-file-boot-wimboot"></a><span data-ttu-id="2357b-103">Start der Windows-Abbild Datei (wimboot)</span><span class="sxs-lookup"><span data-stu-id="2357b-103">Windows Image File Boot (WimBoot)</span></span>

## <a name="platform"></a><span data-ttu-id="2357b-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="2357b-104">Platform</span></span>

<span data-ttu-id="2357b-105">**Clients:** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2357b-105">**Clients:** Windows 8.1</span></span>  

## <a name="description"></a><span data-ttu-id="2357b-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2357b-106">Description</span></span>

<span data-ttu-id="2357b-107">Wimboot ist eine alternative Möglichkeit für OEMs, Windows bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="2357b-107">WimBoot is an alternative way for OEMs to deploy Windows.</span></span> <span data-ttu-id="2357b-108">Eine wimboot-Bereitstellung startet Windows direkt aus einer komprimierten Windows-Abbild Datei (WIM) und führt Sie aus.</span><span class="sxs-lookup"><span data-stu-id="2357b-108">A WimBoot deployment boots and runs Windows directly out of a compressed Windows Image File (WIM).</span></span> <span data-ttu-id="2357b-109">Diese WIM-Datei ist unveränderlich, und der Zugriff darauf wird von einem neuen Dateisystem-Filtertreiber (WoF.sys) verwaltet.</span><span class="sxs-lookup"><span data-stu-id="2357b-109">This WIM file is immutable, and access to it is managed by a new file system filter driver (WoF.sys).</span></span>

<span data-ttu-id="2357b-110">Das Ergebnis ist eine erhebliche Verringerung des Speicherplatzes, der für die Installation von Windows erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="2357b-110">The result is a significant reduction in the disk space required to install Windows.</span></span>

## <a name="manifestations"></a><span data-ttu-id="2357b-111">Kundgebungen</span><span class="sxs-lookup"><span data-stu-id="2357b-111">Manifestations</span></span>

<span data-ttu-id="2357b-112">Die meisten Anwendungen sollten von wimboot vollständig betroffen sein.</span><span class="sxs-lookup"><span data-stu-id="2357b-112">Most applications should be completely unaffected by WimBoot.</span></span> <span data-ttu-id="2357b-113">Nur Anwendungen, die auf Systemdateien oder vorab geladene Dateien für Schreibzugriffe zugreifen und diese entsperren, sind möglicherweise betroffen.</span><span class="sxs-lookup"><span data-stu-id="2357b-113">Only applications that access and unlock system files or pre-loaded files for write access may be affected.</span></span> <span data-ttu-id="2357b-114">Da die WIM unveränderlich ist, werden Aktualisierungen an der Datei (d. h. System-oder vorab geladene Dateien) einfach auf der C:- \\ Partition gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2357b-114">Since the WIM is immutable, updates to it (that is, system or pre-loaded files) are simply stored on the C:\\ partition.</span></span>

<span data-ttu-id="2357b-115">Wenn eine Anwendung den Schreibzugriff für alle WIM-gestützten Systemdateien und vorab geladenen Dateien entsperrt hat, würden die Einsparungen, die von wimboot bereitgestellt werden, vollständig verloren gehen, da alle diese Dateien dekomprimiert und auf dem Volume "C:" abgelegt werden \\ .</span><span class="sxs-lookup"><span data-stu-id="2357b-115">If an application unlocked write access for all WIM-backed system and pre-loaded files, the savings that WimBoot delivers would be completely lost, as all of these files would be decompressed and placed on the C:\\ volume.</span></span>

<span data-ttu-id="2357b-116">Außerdem müssen Sicherungs-und Wiederherstellungs Anwendungen die wimboot-bereit Stellungen beachten, da die WIM in einer separaten Partition vorhanden ist. Das heißt, bei der Sicherungskopie müssen sowohl die C: \\ -als auch die WIM-Partitionen gespeichert werden, und beide müssen gleichzeitig wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="2357b-116">Furthermore, back-up and restore applications need to be aware of WimBoot deployments, as the WIM is present in a separate partition; that is, on back-up, both the C:\\ and WIM partitions must be saved and both must be restored together.</span></span>

## <a name="solution"></a><span data-ttu-id="2357b-117">Lösung</span><span class="sxs-lookup"><span data-stu-id="2357b-117">Solution</span></span>

<span data-ttu-id="2357b-118">Es wurden neue APIs eingeführt, mit denen Anwendungen direkt abfragen können, ob ein bestimmtes Volume oder eine Datei durch eine WIM-Datei unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2357b-118">New APIs were introduced that allow applications to directly query if a given volume or file is backed by a WIM.</span></span> <span data-ttu-id="2357b-119">Diese Informationen ermöglichen es Anwendungen, geeignete Entscheidungen zu treffen, z. b. das Öffnen dieser Dateien nur für den Lesezugriff oder das Identifizieren von Volumes/Partitionen, die gleichzeitig gesichert und wieder hergestellt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2357b-119">This information allows applications to make appropriate decisions, such as opening these files only for read access or to identify volumes/partitions that have to be backed up and restored together.</span></span>

## <a name="compatibility-performance-reliability-or-usability-tests"></a><span data-ttu-id="2357b-120">Kompatibilitäts-, Leistungs-, Zuverlässigkeits-oder Nutzbarkeits Tests</span><span class="sxs-lookup"><span data-stu-id="2357b-120">Compatibility, performance, reliability, or usability tests</span></span>

<span data-ttu-id="2357b-121">Anwendungsentwickler sollten Ihre Software und die entsprechenden Szenarios auf einem wimboot-System testen, insbesondere dann, wenn diese Anwendungen auf Systemdateien oder vorab geladene Dateien zugreifen.</span><span class="sxs-lookup"><span data-stu-id="2357b-121">Application developers should test their software and its corresponding scenarios on a WimBoot system, especially if these applications access system or pre-loaded files.</span></span> <span data-ttu-id="2357b-122">Wenn ein Szenario abgeschlossen ist, sollte eine beträchtliche Reduzierung des verfügbaren Speicherplatzes gezahlt werden.</span><span class="sxs-lookup"><span data-stu-id="2357b-122">Special attention should be paid to a significant reduction in available disk space after a scenario has been completed.</span></span>

 

 




