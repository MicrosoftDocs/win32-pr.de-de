---
description: Die cloudfilterapi bietet Funktionen an der Grenze zwischen dem Benutzermodus und dem Dateisystem.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Cloud Sync Engines
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: debe32a1849a393a067017f90f5405c4b3ba77d1
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106353411"
---
# <a name="cloud-sync-engines"></a><span data-ttu-id="122a0-103">Cloud Sync Engines</span><span class="sxs-lookup"><span data-stu-id="122a0-103">Cloud Sync Engines</span></span>

<span data-ttu-id="122a0-104">Siehe auch [Cloud-Spiegel Beispiel](/windows/win32/cfapi/build-a-cloud-file-sync-engine#cloud-mirror-sample).</span><span class="sxs-lookup"><span data-stu-id="122a0-104">Also see [Cloud Mirror sample](/windows/win32/cfapi/build-a-cloud-file-sync-engine#cloud-mirror-sample).</span></span>

<span data-ttu-id="122a0-105">Ab Windows 10, Version 1709, stellt Windows die *Cloud Files-API* bereit.</span><span class="sxs-lookup"><span data-stu-id="122a0-105">Starting in Windows 10, version 1709, Windows provides the *cloud files API*.</span></span> <span data-ttu-id="122a0-106">Diese API besteht aus mehreren nativen Win32-und WinRT-APIs, die die Unterstützung für Cloud-Synchronisierungs Module formalisieren und Aufgaben wie das Erstellen und Verwalten von Platzhalter Dateien und Verzeichnissen verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="122a0-106">This API consists of several native Win32 and WinRT APIs that formalize support for cloud sync engines, and handles tasks such as creating and managing placeholder files and directories.</span></span> <span data-ttu-id="122a0-107">Benutzer dieser API sind in der Regel Synchronisierungs Anbieter und ein gewisser Umfang von Windows-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="122a0-107">Users of this API are typically sync providers and to some extent, Windows applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="122a0-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="122a0-108">In this section</span></span>

| <span data-ttu-id="122a0-109">Thema</span><span class="sxs-lookup"><span data-stu-id="122a0-109">Topic</span></span>                                                                | <span data-ttu-id="122a0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="122a0-110">Description</span></span>                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="122a0-111">Erstellen einer Cloud-Synchronisierungs-Engine, die Platzhalter Dateien unterstützt</span><span class="sxs-lookup"><span data-stu-id="122a0-111">Build a Cloud Sync Engine that Supports Placeholder Files</span></span>](build-a-cloud-file-sync-engine.md)<br/> | <span data-ttu-id="122a0-112">Erfahren Sie, wie Sie die Cloud Files-API verwenden, um ein clouddateisynchronisierungs-Engine zu erstellen, das Platzhalter Dateien und Datei-Explorer-Integration</span><span class="sxs-lookup"><span data-stu-id="122a0-112">Learn how to use the cloud files API to build a cloud file sync engine that includes placeholder files and File Explorer integration.</span></span> <br/> |
| [<span data-ttu-id="122a0-113">Cloudfilterverweis</span><span class="sxs-lookup"><span data-stu-id="122a0-113">Cloud Filter Reference</span></span>](cloud-filter-reference.md)<br/> | <span data-ttu-id="122a0-114">Die Cloud Filter-API ist eine native Win32-API, die Teil der umfassenderen Cloud Files-API ist.</span><span class="sxs-lookup"><span data-stu-id="122a0-114">The cloud filter API is a native Win32 API that is part of the broader cloud files API.</span></span> <span data-ttu-id="122a0-115">Die cloudfilterapi bietet Funktionen an der Grenze zwischen dem Benutzermodus und dem Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="122a0-115">The cloud filter API provides functionality at the boundary between the user mode and the file system.</span></span> <span data-ttu-id="122a0-116">Diese API behandelt die Erstellung und Verwaltung von Platzhalter Dateien und Verzeichnissen.</span><span class="sxs-lookup"><span data-stu-id="122a0-116">This API handles the creation and management of placeholder files and directories.</span></span> <br/> |

