---
description: Veranschaulicht die Verwendung der ishelllibrary-Schnittstelle zum Erstellen einer Befehlszeilen Anwendung, die programmgesteuerten Zugriff auf die Untersuchung und Bearbeitung von Bibliotheken und Bibliotheksdateien ermöglicht.
title: Beispiel für die Befehlszeile der Shellbibliothek
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 5EC06E69-8AC8-4d9e-BAFC-C1AFC1294023
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c9db182498791fee344061c91ea570ed770f3a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485771"
---
# <a name="shell-library-command-line-sample"></a><span data-ttu-id="61b09-103">Beispiel für die Befehlszeile der Shellbibliothek</span><span class="sxs-lookup"><span data-stu-id="61b09-103">Shell Library Command Line Sample</span></span>

<span data-ttu-id="61b09-104">Veranschaulicht die Verwendung der [**ishelllibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) -Schnittstelle zum Erstellen einer Befehlszeilen Anwendung, die programmgesteuerten Zugriff auf die Untersuchung und Bearbeitung von Bibliotheken und Bibliotheksdateien ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="61b09-104">Demonstrates how to use the [**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary) interface to create a command-line application that provides programmatic access for inspecting and manipulating libraries and library files.</span></span>

<span data-ttu-id="61b09-105">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="61b09-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="61b09-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61b09-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="61b09-107">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="61b09-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="61b09-108">Beispiel zum Aufbau</span><span class="sxs-lookup"><span data-stu-id="61b09-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="61b09-109">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="61b09-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="61b09-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="61b09-110">Requirements</span></span>



| <span data-ttu-id="61b09-111">Produkt</span><span class="sxs-lookup"><span data-stu-id="61b09-111">Product</span></span>                                | <span data-ttu-id="61b09-112">Minimale Produkt Version</span><span class="sxs-lookup"><span data-stu-id="61b09-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="61b09-113">Windows</span><span class="sxs-lookup"><span data-stu-id="61b09-113">Windows</span></span>                                | <span data-ttu-id="61b09-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="61b09-114">Windows 7</span></span>               |
| <span data-ttu-id="61b09-115">Windows Software Development Kit (SDK)</span><span class="sxs-lookup"><span data-stu-id="61b09-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="61b09-116">7.0</span><span class="sxs-lookup"><span data-stu-id="61b09-116">7.0</span></span>                     |



 

<span data-ttu-id="61b09-117">Weitere Anforderungen finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="61b09-117">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="61b09-118">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="61b09-118">Downloading the Sample</span></span>

| <span data-ttu-id="61b09-119">Standort</span><span class="sxs-lookup"><span data-stu-id="61b09-119">Location</span></span>      | <span data-ttu-id="61b09-120">Pfad-URL</span><span class="sxs-lookup"><span data-stu-id="61b09-120">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61b09-121">GitHub</span><span class="sxs-lookup"><span data-stu-id="61b09-121">GitHub</span></span>  | [<span data-ttu-id="61b09-122">Shelllibrarycommandline-Beispiel</span><span class="sxs-lookup"><span data-stu-id="61b09-122">ShellLibraryCommandLine sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ShellLibraryCommandLine) |

## <a name="building-the-sample"></a><span data-ttu-id="61b09-123">Erstellen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="61b09-123">Building the Sample</span></span>

<span data-ttu-id="61b09-124">Anweisungen zum Erstellen des Beispiels finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="61b09-124">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="61b09-125">Ausführen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="61b09-125">Running the Sample</span></span>

<span data-ttu-id="61b09-126">Anweisungen zum Erstellen des Beispiels finden Sie in der im Beispiel enthaltenen Infodatei.</span><span class="sxs-lookup"><span data-stu-id="61b09-126">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



