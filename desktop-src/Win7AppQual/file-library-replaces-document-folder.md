---
description: Dateibibliothek ersetzt Dokumentordner
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: Dateibibliothek ersetzt Dokumentordner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699c645d574012a419f77538bcc58d61a4938120
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088378"
---
# <a name="file-library-replaces-document-folder"></a><span data-ttu-id="bb669-103">Dateibibliothek ersetzt Dokumentordner</span><span class="sxs-lookup"><span data-stu-id="bb669-103">File Library Replaces Document Folder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="bb669-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="bb669-104">Affected Platforms</span></span>

<span data-ttu-id="bb669-105">**Clients** – Windows 7</span><span class="sxs-lookup"><span data-stu-id="bb669-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="bb669-106">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bb669-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="bb669-107">Auswirkung von Features</span><span class="sxs-lookup"><span data-stu-id="bb669-107">Feature Impact</span></span>

<span data-ttu-id="bb669-108">**Schweregrad:** Mittel</span><span class="sxs-lookup"><span data-stu-id="bb669-108">**Severity** - Medium</span></span>  
<span data-ttu-id="bb669-109">**Häufigkeit** – Hoch</span><span class="sxs-lookup"><span data-stu-id="bb669-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="bb669-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb669-110">Description</span></span>

<span data-ttu-id="bb669-111">Bibliotheken bieten eine zentrale ordnerbasierte Begehung für Dateispeicherung, Suche und Zugriff über mehrere Lokale und Remotespeicherorte hinweg.</span><span class="sxs-lookup"><span data-stu-id="bb669-111">Libraries provide a centralized folder-like experience for file storage, search, and access across multiple locations, both local and remote.</span></span>

<span data-ttu-id="bb669-112">Die von allgemeinen Dateidialogfeldern verwendeten Standardspeicherorte (z. B. Öffnen und Speichern) wurden vom Dokumentordner in die Dokumentbibliothek geändert.</span><span class="sxs-lookup"><span data-stu-id="bb669-112">The default locations used by common file dialogs (for example, Open, and Save) have been changed from the Document Folder to the Documents Library.</span></span> <span data-ttu-id="bb669-113">Die Benutzeroberfläche unverändert, aber der Benutzer kann die Bibliothek nun mithilfe verschiedener Anordnungsansichten anzeigen, durchsuchen und durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="bb669-113">The User Interface is unchanged, but the user will now be able to view, browse, and search the Library using various arrangement views.</span></span> <span data-ttu-id="bb669-114">Dateien werden im Standardspeicherort Bibliothek gespeichert, es sei denn, der Benutzer ändert den Standardspeicherort oder wählt einen anderen Ordner aus.</span><span class="sxs-lookup"><span data-stu-id="bb669-114">Files will be saved into the Library default save location unless the user changes the default save location or chooses a different folder.</span></span>

<span data-ttu-id="bb669-115">Entwickler können über die IShellLibrary-Schnittstelle eigene Bibliotheken erstellen oder vorhandenen Bibliotheken Speicherorte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bb669-115">Developers could create their own libraries or add locations to existing libraries using the IShellLibrary interface.</span></span> <span data-ttu-id="bb669-116">Benutzer können Bibliotheken mithilfe des Systems Für bekannte Ordner suchen (z. B. FOLDERID \_ DocumentsLibrary).</span><span class="sxs-lookup"><span data-stu-id="bb669-116">Users can find libraries by using the Known Folder system (for example, FOLDERID\_DocumentsLibrary).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="bb669-117">Auswirkungen</span><span class="sxs-lookup"><span data-stu-id="bb669-117">Manifestation of Impact</span></span>

<span data-ttu-id="bb669-118">Die Bibliothek selbst ist eine Datei und kein Ordner.</span><span class="sxs-lookup"><span data-stu-id="bb669-118">The Library is itself a file, and not a folder.</span></span> <span data-ttu-id="bb669-119">Aus diesem Grund können Pfadbearbeitungen zu Fehlern führen, weil die Anwendung versucht, Dateien mit Dateien zu verketten.</span><span class="sxs-lookup"><span data-stu-id="bb669-119">Therefore, path manipulations could result errors due to the attempt by the application to concatenate files to files.</span></span>

## <a name="solution"></a><span data-ttu-id="bb669-120">Lösung</span><span class="sxs-lookup"><span data-stu-id="bb669-120">Solution</span></span>

<span data-ttu-id="bb669-121">Bei Verwendung von IFileDialog müssen Sie die GetResult-Methode anstelle der Kombination aus GetFolder und GetFilename verwenden, wie in den vorherigen Betriebssystemversionen.</span><span class="sxs-lookup"><span data-stu-id="bb669-121">When using IFileDialog, you must use GetResult method instead of combination of GetFolder and GetFilename as you would in the previous operating system versions.</span></span> <span data-ttu-id="bb669-122">Verwenden Sie nach Möglichkeit die Shell-APIs, um mit Elementen im Shellnamespace (z. B. IShellItem) zu interagieren und diese zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="bb669-122">Use the Shell APIs where possible to interact with and manipulate items in the Shell Namespace (for example, IShellItem).</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="bb669-123">Nutzen von Featurefunktionen</span><span class="sxs-lookup"><span data-stu-id="bb669-123">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="bb669-124">Wenn Sie Eigene Bibliotheken erstellen oder vorhandenen Bibliotheken Speicherorte hinzufügen möchten, müssen Sie die IShellLibrary-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="bb669-124">If you want to create your own libraries or add locations to existing libraries, you must use IShellLibrary API.</span></span> <span data-ttu-id="bb669-125">Bibliotheken sind selbst Shellordner, sodass Sie sie genau wie jeden anderen Shellordner aufzählen können.</span><span class="sxs-lookup"><span data-stu-id="bb669-125">Libraries are themselves Shell Folders so you can enumerate them just like any other Shell Folder.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="bb669-126">Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Benutzerfreundlichkeitstests</span><span class="sxs-lookup"><span data-stu-id="bb669-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="bb669-127">Mithilfe des allgemeinen Dateidialogfelds wird sichergestellt, dass Benutzer direkt in ihren Bibliotheken speichern können.</span><span class="sxs-lookup"><span data-stu-id="bb669-127">Using the common file dialog will ensure that users can save directly to their libraries.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="bb669-128">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bb669-128">Links to Other Resources</span></span>

-   <span data-ttu-id="bb669-129">**Windows-Bibliotheken:**https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span><span class="sxs-lookup"><span data-stu-id="bb669-129">**Windows Libraries:** https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span></span>
-   <span data-ttu-id="bb669-130">**Synchronisierung mit einer Bibliothek:**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span><span class="sxs-lookup"><span data-stu-id="bb669-130">**Keeping in sync with a library:** https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span></span>

 

 



