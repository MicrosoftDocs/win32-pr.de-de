---
description: Veranschaulicht, wie Bibliotheken als Container aufgelistet werden.
title: Shellbibliothekssicherung (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 206356B2-3998-4a19-BC4D-F6A043AFDBD3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7e1b4746d2e559b567adb4cbd2305ea474b03129
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980760"
---
# <a name="shell-library-backup-sample"></a><span data-ttu-id="61660-103">Shellbibliothekssicherung (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="61660-103">Shell Library Backup Sample</span></span>

<span data-ttu-id="61660-104">Veranschaulicht, wie Bibliotheken als Container aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="61660-104">Demonstrates how to enumerate libraries as containers.</span></span> <span data-ttu-id="61660-105">Bibliotheken sind das neue Speicher Paradigma für Benutzer Dateien und werden in Windows 7 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="61660-105">Libraries are the new storage paradigm for user files and are introduced in Windows 7.</span></span>

<span data-ttu-id="61660-106">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="61660-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="61660-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61660-107">Description</span></span>](#description)
-   [<span data-ttu-id="61660-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61660-108">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="61660-109">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="61660-109">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="61660-110">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="61660-110">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="61660-111">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="61660-111">Running the Sample</span></span>](#running-the-sample)

## <a name="description"></a><span data-ttu-id="61660-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="61660-112">Description</span></span>

<span data-ttu-id="61660-113">Bei diesem Beispiel handelt es sich um eine fiktive Sicherungs Anwendung, die zeigt, wie Bibliotheken über das Dialogfeld "allgemeine Datei" ausgewählt werden</span><span class="sxs-lookup"><span data-stu-id="61660-113">This sample is a fictional backup application that shows how to pick libraries through the common file dialog.</span></span> <span data-ttu-id="61660-114">Außerdem wird veranschaulicht, wie Bibliotheken mithilfe des Shell-Namespace Walker gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="61660-114">It also demonstrates how to back up libraries using the Shell namespace walker.</span></span>

## <a name="requirements"></a><span data-ttu-id="61660-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="61660-115">Requirements</span></span>



| <span data-ttu-id="61660-116">Produkt</span><span class="sxs-lookup"><span data-stu-id="61660-116">Product</span></span>                                | <span data-ttu-id="61660-117">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="61660-117">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="61660-118">Windows</span><span class="sxs-lookup"><span data-stu-id="61660-118">Windows</span></span>                                | <span data-ttu-id="61660-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="61660-119">Windows 7</span></span>               |
| <span data-ttu-id="61660-120">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="61660-120">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="61660-121">7.0</span><span class="sxs-lookup"><span data-stu-id="61660-121">7.0</span></span>                     |



 

<span data-ttu-id="61660-122">Weitere Anforderungen finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="61660-122">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="61660-123">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="61660-123">Downloading the Sample</span></span>

| <span data-ttu-id="61660-124">Standort</span><span class="sxs-lookup"><span data-stu-id="61660-124">Location</span></span>      | <span data-ttu-id="61660-125">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="61660-125">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61660-126">GitHub</span><span class="sxs-lookup"><span data-stu-id="61660-126">GitHub</span></span>  | [<span data-ttu-id="61660-127">Shelllibrarybackup-Beispiel</span><span class="sxs-lookup"><span data-stu-id="61660-127">ShellLibraryBackup sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ShellLibraryBackup) |

## <a name="building-the-sample"></a><span data-ttu-id="61660-128">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="61660-128">Building the Sample</span></span>

<span data-ttu-id="61660-129">Anweisungen zum Erstellen des Beispiels finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="61660-129">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="61660-130">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="61660-130">Running the Sample</span></span>

<span data-ttu-id="61660-131">Anweisungen zum Erstellen des Beispiels finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="61660-131">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



