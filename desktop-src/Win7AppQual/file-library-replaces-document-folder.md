---
description: .
ms.assetid: 80b97bfc-4212-4401-a4a9-d96e2f39be60
title: Datei Bibliothek ersetzt Dokument Ordner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15431f5fb5fb5e73dbaf171625a0a6582fa7add2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868140"
---
# <a name="file-library-replaces-document-folder"></a><span data-ttu-id="aa2d4-103">Datei Bibliothek ersetzt Dokument Ordner</span><span class="sxs-lookup"><span data-stu-id="aa2d4-103">File Library Replaces Document Folder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="aa2d4-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="aa2d4-104">Affected Platforms</span></span>

<span data-ttu-id="aa2d4-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="aa2d4-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="aa2d4-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="aa2d4-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="aa2d4-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="aa2d4-107">Feature Impact</span></span>

<span data-ttu-id="aa2d4-108">**Schweregrad** -Mittel</span><span class="sxs-lookup"><span data-stu-id="aa2d4-108">**Severity** - Medium</span></span>  
<span data-ttu-id="aa2d4-109">**Häufigkeit** -hoch</span><span class="sxs-lookup"><span data-stu-id="aa2d4-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="aa2d4-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa2d4-110">Description</span></span>

<span data-ttu-id="aa2d4-111">Bibliotheken bieten eine zentralisierte Ordner ähnliche Umgebung für die Speicherung von Dateien, die Suche und den Zugriff über mehrere Standorte hinweg, sowohl lokal als auch Remote.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-111">Libraries provide a centralized folder-like experience for file storage, search, and access across multiple locations, both local and remote.</span></span>

<span data-ttu-id="aa2d4-112">Die Standard Speicherorte, die von allgemeinen Datei Dialogfeldern (z. b. "Öffnen" und "Speichern") verwendet werden, wurden aus dem Dokument Ordner in die Dokumentbibliothek geändert.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-112">The default locations used by common file dialogs (for example, Open, and Save) have been changed from the Document Folder to the Documents Library.</span></span> <span data-ttu-id="aa2d4-113">Die Benutzeroberfläche ist unverändert, aber der Benutzer kann die Bibliothek nun mithilfe verschiedener Ansichts Ansichten anzeigen, durchsuchen und durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-113">The User Interface is unchanged, but the user will now be able to view, browse, and search the Library using various arrangement views.</span></span> <span data-ttu-id="aa2d4-114">Dateien werden im Standard Speicherort der Bibliothek gespeichert, es sei denn, der Benutzer ändert den Standard Speicherort oder wählt einen anderen Ordner aus.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-114">Files will be saved into the Library default save location unless the user changes the default save location or chooses a different folder.</span></span>

<span data-ttu-id="aa2d4-115">Entwickler können Ihre eigenen Bibliotheken erstellen oder vorhandenen Bibliotheken mithilfe der ishelllibrary-Schnittstelle Speicherorte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-115">Developers could create their own libraries or add locations to existing libraries using the IShellLibrary interface.</span></span> <span data-ttu-id="aa2d4-116">Benutzer können Bibliotheken mit dem bekannten Ordnersystem suchen (z. b. folderid \_ documentslibrary).</span><span class="sxs-lookup"><span data-stu-id="aa2d4-116">Users can find libraries by using the Known Folder system (for example, FOLDERID\_DocumentsLibrary).</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="aa2d4-117">Erscheinung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="aa2d4-117">Manifestation of Impact</span></span>

<span data-ttu-id="aa2d4-118">Die Bibliothek ist selbst eine Datei und kein Ordner.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-118">The Library is itself a file, and not a folder.</span></span> <span data-ttu-id="aa2d4-119">Daher können Pfad Manipulationen aufgrund des Versuchs, dass die Anwendung Dateien zu Dateien verkettet, zu Fehlern führen.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-119">Therefore, path manipulations could result errors due to the attempt by the application to concatenate files to files.</span></span>

## <a name="solution"></a><span data-ttu-id="aa2d4-120">Lösung</span><span class="sxs-lookup"><span data-stu-id="aa2d4-120">Solution</span></span>

<span data-ttu-id="aa2d4-121">Wenn Sie ifiledialog verwenden, müssen Sie die GetResult-Methode anstelle der Kombination aus "GetFolder" und "GetFileName" verwenden, wie in den vorherigen Betriebssystemversionen.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-121">When using IFileDialog, you must use GetResult method instead of combination of GetFolder and GetFilename as you would in the previous operating system versions.</span></span> <span data-ttu-id="aa2d4-122">Verwenden Sie nach Möglichkeit die Shell-APIs, um mit Elementen im Shellnamespace (z. b. IShellItem) zu interagieren und diese zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-122">Use the Shell APIs where possible to interact with and manipulate items in the Shell Namespace (for example, IShellItem).</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="aa2d4-123">Nutzen von Featurefunktionen</span><span class="sxs-lookup"><span data-stu-id="aa2d4-123">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="aa2d4-124">Wenn Sie eigene Bibliotheken erstellen oder vorhandenen Bibliotheken Speicherorte hinzufügen möchten, müssen Sie die ishelllibrary-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-124">If you want to create your own libraries or add locations to existing libraries, you must use IShellLibrary API.</span></span> <span data-ttu-id="aa2d4-125">Bibliotheken sind selbst Shellordner, sodass Sie Sie wie alle anderen Shellordner auflisten können.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-125">Libraries are themselves Shell Folders so you can enumerate them just like any other Shell Folder.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="aa2d4-126">Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="aa2d4-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="aa2d4-127">Mithilfe des Dialog Felds "allgemeine Datei" wird sichergestellt, dass Benutzer direkt in ihren Bibliotheken speichern können.</span><span class="sxs-lookup"><span data-stu-id="aa2d4-127">Using the common file dialog will ensure that users can save directly to their libraries.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="aa2d4-128">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aa2d4-128">Links to Other Resources</span></span>

-   <span data-ttu-id="aa2d4-129">**Windows-Bibliotheken:**https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span><span class="sxs-lookup"><span data-stu-id="aa2d4-129">**Windows Libraries:** https://msdn.microsoft.com/library/dd758096(VS.85).aspx</span></span>
-   <span data-ttu-id="aa2d4-130">**Synchronisierung mit einer Bibliothek:**https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span><span class="sxs-lookup"><span data-stu-id="aa2d4-130">**Keeping in sync with a library:** https://msdn.microsoft.com/library/dd758094(VS.85).aspx\#library\_keeping\_in\_sync</span></span>

 

 



