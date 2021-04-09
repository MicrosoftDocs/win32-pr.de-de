---
title: Verwalten von Dateien und Daten
description: Benutzer haben in Windows 7 einen einfacheren Zugriff auf Dateien und Daten.
ms.assetid: 44756220-1cd0-4c7e-a49e-5786a6220f8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5617d7746746186933bce022aa2202175fb994e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948895"
---
# <a name="managing-files-and-data"></a><span data-ttu-id="739ae-103">Verwalten von Dateien und Daten</span><span class="sxs-lookup"><span data-stu-id="739ae-103">Managing Files and Data</span></span>

<span data-ttu-id="739ae-104">Benutzer haben in Windows 7 einen einfacheren Zugriff auf Dateien und Daten.</span><span class="sxs-lookup"><span data-stu-id="739ae-104">Users have easier access to files and data in Windows 7.</span></span> <span data-ttu-id="739ae-105">Neue APIs machen Dateien und Ansichten informativer, sodass Anwendungen relevante und besondere Informationen an Windows Explorer übermitteln können.</span><span class="sxs-lookup"><span data-stu-id="739ae-105">New APIs make files and views more informative, enabling applications to deliver relevant and distinctive information to Windows Explorer.</span></span> <span data-ttu-id="739ae-106">Darüber hinaus profitieren Anwendungen vom neuen *Bibliotheks* Modell, einem nützlichen, stärker abstrakten Konzept des Benutzer Speicherplatzes als Ordnern und können auch an gemeinsamen Bibliotheken ähnlicher Dateitypen teilnehmen, die von verschiedenen Anwendungen gemeinsam genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="739ae-106">In addition, applications benefit from the new *Libraries* model, a useful, more abstract notion of user storage space than folders, and can also participate in common libraries of similar file types that are shared by different applications.</span></span>

## <a name="libraries"></a><span data-ttu-id="739ae-107">Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="739ae-107">Libraries</span></span>

<span data-ttu-id="739ae-108">Mit Windows 7 wird das Konzept der *Bibliotheken* als Ziele eingeführt, bei denen Entwickler und Endbenutzer Ihre Daten als Sammlungen von Elementen suchen und organisieren können, die mehrere Standorte auf dem lokalen Computer und auf Remote Computern umfassen können.</span><span class="sxs-lookup"><span data-stu-id="739ae-108">Windows 7 introduces the concept of *Libraries* as destinations where developers and end-users can find and organize their data as collections of items that can span multiple locations on the local computer as well as on remote computers.</span></span>

<span data-ttu-id="739ae-109">Die *Bibliotheks*-APIs bieten Entwicklern eine einfache Möglichkeit, Anwendungen zu erstellen, die *Bibliotheken* als erstklassige Elemente innerhalb von Anwendungen erstellen, mit ihnen interagieren und diese unterstützen.</span><span class="sxs-lookup"><span data-stu-id="739ae-109">The *Library* APIs provide a straightforward way for developers to create applications that create, interact with, and support *Libraries* as first-class items within applications.</span></span> <span data-ttu-id="739ae-110">*Bibliotheken* können auch über das Dialogfeld Ordner Auswahl ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="739ae-110">*Libraries* can also be selected by using the folder picker dialog box.</span></span> <span data-ttu-id="739ae-111">Anwendungen können relevante Bibliotheks Bereiche auflisten, oder Sie können die Bibliothek direkt als Ordner verwenden.</span><span class="sxs-lookup"><span data-stu-id="739ae-111">Applications can enumerate relevant library scopes, or they can use the library directly as a folder.</span></span> <span data-ttu-id="739ae-112">(Weitere Informationen finden Sie unter [Windows-Bibliotheken](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) und [Windows 7-Bibliotheken: Entwickler Ressourcen](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)).</span><span class="sxs-lookup"><span data-stu-id="739ae-112">(See [Windows Libraries](/previous-versions/windows/desktop/legacy/dd758096(v=vs.85)) and [Windows 7 Libraries: Developer Resources](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/dataaccess)).</span></span>

![Windows 7-Bildbibliothek](images/windows7-10.jpg)

<span data-ttu-id="739ae-114">*Bilderbibliothek* zeigt Ihre Bilder an, unabhängig davon, wo Sie gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="739ae-114">*Pictures Library* shows your pictures no matter where they are stored</span></span>

## <a name="file-formats-and-data-stores"></a><span data-ttu-id="739ae-115">Dateiformate und Datenspeicher</span><span class="sxs-lookup"><span data-stu-id="739ae-115">File Formats and Data Stores</span></span>

<span data-ttu-id="739ae-116">In Windows 7 erleichtert Windows Explorer das Verwalten und manipulieren von Dateien für den Benutzer auf verschiedene Weise:</span><span class="sxs-lookup"><span data-stu-id="739ae-116">In Windows 7, Windows Explorer makes file management and manipulation easier for the user in several ways:</span></span>

-   <span data-ttu-id="739ae-117">Die Vorschau für den Dateityp Ihrer Anwendung ist mit einer neuen Schaltfläche, über die Benutzer den Vorschaufenster anzeigen und ausblenden können, besser zugänglich.</span><span class="sxs-lookup"><span data-stu-id="739ae-117">The preview for your application's file type is more accessible with a new button that lets users show and hide the preview pane.</span></span>
-   <span data-ttu-id="739ae-118">Immersive visuelle Stapel aggregieren Miniaturbilder für Dateitypen in einer Ansicht.</span><span class="sxs-lookup"><span data-stu-id="739ae-118">Immersive visual stacks aggregate thumbnail images for file types in a view.</span></span>
-   <span data-ttu-id="739ae-119">Windows Explorer-Ansichten zeigen nützliche Informationen auf der Grundlage von Eigenschaften an, die mit Ihrem Eigenschaften Handler geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="739ae-119">Windows Explorer views show useful information based on properties written with your property handler.</span></span>
-   <span data-ttu-id="739ae-120">Dokument Ausschnitte und Treffer Hervorhebung verwenden Sie die Implementierung der **IFilter** -Schnittstelle, um das Suchen und suchen von Dateien zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="739ae-120">Document snippets and hit highlighting use your **IFilter** interface implementation to make searching and finding files easier.</span></span>
-   <span data-ttu-id="739ae-121">Kontextmenü Verben und Befehle sind einfacher als je zuvor zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="739ae-121">Context-menu verbs and commands are easier than ever to implement.</span></span>

<span data-ttu-id="739ae-122">Durch Implementieren aller entsprechenden Format Handler für die Elemente, die von Ihrem Protokollhandler zurückgegeben werden, können Suchergebnisse aus dem benutzerdefinierten Datenspeicher so umfangreich sein wie Suchergebnisse aus Dateien.</span><span class="sxs-lookup"><span data-stu-id="739ae-122">By implementing all of the appropriate format handlers for the items returned from your protocol handler, search results from your custom data store can be as rich as search results from files.</span></span> <span data-ttu-id="739ae-123">*Bibliotheken* werden automatisch für Ihre Protokollhandler erstellt, damit Benutzer Ihre Suchvorgänge problemlos festlegen können.</span><span class="sxs-lookup"><span data-stu-id="739ae-123">*Libraries* are automatically created for your protocol handlers so users can scope their searches easily.</span></span> <span data-ttu-id="739ae-124">Und die Logik zum Erstellen von *Bibliotheken* kann problemlos über die Registrierung angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="739ae-124">And the logic for creating *Libraries* can be easily customized through the registry.</span></span> <span data-ttu-id="739ae-125">(Siehe [entwickeln von Filtern für die Windows-Suche](../search/-search-3x-wds-extidx-filters.md).)</span><span class="sxs-lookup"><span data-stu-id="739ae-125">(See [Developing Filters for Windows Search](../search/-search-3x-wds-extidx-filters.md).)</span></span>

![Windows 7-Dokumentbibliothek](images/windows7-11.jpg)

<span data-ttu-id="739ae-127">In Windows 7 erleichtert Windows Explorer die Dateiverwaltung und-Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="739ae-127">In Windows 7, Windows Explorer makes file management and manipulation easier</span></span>

 

 