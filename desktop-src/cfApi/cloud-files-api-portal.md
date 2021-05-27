---
description: Die Cloudfilter-API stellt Funktionen an der Grenze zwischen dem Benutzermodus und dem Dateisystem bereit.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Cloudsynchronisierungs-Engines
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: d40b195a442859441138ae4e61cb0eb946411623
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549595"
---
# <a name="cloud-sync-engines"></a><span data-ttu-id="87407-103">Cloudsynchronisierungs-Engines</span><span class="sxs-lookup"><span data-stu-id="87407-103">Cloud Sync Engines</span></span>

<span data-ttu-id="87407-104">Siehe auch [CloudSpiegel-Beispiel.](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample)</span><span class="sxs-lookup"><span data-stu-id="87407-104">Also see [Cloud Mirror sample](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample).</span></span>

<span data-ttu-id="87407-105">Ab Windows 10 Version 1709 stellt Windows die *Clouddateien-API bereit.*</span><span class="sxs-lookup"><span data-stu-id="87407-105">Starting in Windows 10, version 1709, Windows provides the *cloud files API*.</span></span> <span data-ttu-id="87407-106">Diese API besteht aus mehreren nativen Win32- und WinRT-APIs, die die Unterstützung für Cloudsynchronisierungs-Engines formalisieren und Aufgaben wie das Erstellen und Verwalten von Platzhalterdateien und Verzeichnissen durchführen.</span><span class="sxs-lookup"><span data-stu-id="87407-106">This API consists of several native Win32 and WinRT APIs that formalize support for cloud sync engines, and handles tasks such as creating and managing placeholder files and directories.</span></span> <span data-ttu-id="87407-107">Benutzer dieser API sind in der Regel Synchronisierungsanbieter und in gewissem Umfang Windows-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="87407-107">Users of this API are typically sync providers and to some extent, Windows applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="87407-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="87407-108">In this section</span></span>

| <span data-ttu-id="87407-109">Thema</span><span class="sxs-lookup"><span data-stu-id="87407-109">Topic</span></span>                                                                | <span data-ttu-id="87407-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87407-110">Description</span></span>                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87407-111">Erstellen eines Cloudsynchronisierungsmoduls, das Platzhalterdateien unterstützt</span><span class="sxs-lookup"><span data-stu-id="87407-111">Build a Cloud Sync Engine that Supports Placeholder Files</span></span>](build-a-cloud-file-sync-engine.md)<br/> | <span data-ttu-id="87407-112">Erfahren Sie, wie Sie die Clouddatei-API verwenden, um ein Clouddateisynchronisierungsmodul zu erstellen, das Platzhalterdateien und die Datei-Explorer-Integration enthält.</span><span class="sxs-lookup"><span data-stu-id="87407-112">Learn how to use the cloud files API to build a cloud file sync engine that includes placeholder files and File Explorer integration.</span></span> <br/> |
| [<span data-ttu-id="87407-113">Cloudfilterreferenz</span><span class="sxs-lookup"><span data-stu-id="87407-113">Cloud Filter Reference</span></span>](cloud-filter-reference.md)<br/> | <span data-ttu-id="87407-114">Die Cloudfilter-API ist eine native Win32-API, die Teil der umfassenderen Clouddateien-API ist.</span><span class="sxs-lookup"><span data-stu-id="87407-114">The cloud filter API is a native Win32 API that is part of the broader cloud files API.</span></span> <span data-ttu-id="87407-115">Die Cloudfilter-API stellt Funktionen an der Grenze zwischen dem Benutzermodus und dem Dateisystem bereit.</span><span class="sxs-lookup"><span data-stu-id="87407-115">The cloud filter API provides functionality at the boundary between the user mode and the file system.</span></span> <span data-ttu-id="87407-116">Diese API übernimmt die Erstellung und Verwaltung von Platzhalterdateien und Verzeichnissen.</span><span class="sxs-lookup"><span data-stu-id="87407-116">This API handles the creation and management of placeholder files and directories.</span></span> <br/> |