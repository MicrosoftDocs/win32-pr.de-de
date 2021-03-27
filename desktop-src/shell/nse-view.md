---
description: Die meisten Namespace Erweiterungen sind eine Teilmenge des Shell-Namespace.
ms.assetid: 00b6b281-b157-4a61-9852-8aafd9ba68d3
title: Anzeigen einer Self-Contained Ansicht einer Namespace Erweiterung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6f8555cfb8cdac6248c5ea1c70ce8af29bfd16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980008"
---
# <a name="displaying-a-self-contained-view-of-a-namespace-extension"></a><span data-ttu-id="46575-103">Anzeigen einer Self-Contained Ansicht einer Namespace Erweiterung</span><span class="sxs-lookup"><span data-stu-id="46575-103">Displaying a Self-Contained View of a Namespace Extension</span></span>

<span data-ttu-id="46575-104">Die meisten Namespace Erweiterungen sind eine Teilmenge des Shell-Namespace.</span><span class="sxs-lookup"><span data-stu-id="46575-104">Most namespace extensions are a subset of the Shell namespace.</span></span> <span data-ttu-id="46575-105">Wenn Sie einen Verknüpfungs Punkt erstellen, wie unter [angeben des Speicher Orts einer Namespace Erweiterung](nse-junction.md)beschrieben, können Benutzer mithilfe von Windows-Explorer genau wie bei jedem anderen Ordner zu ihrer Namespace Erweiterung navigieren.</span><span class="sxs-lookup"><span data-stu-id="46575-105">When you create a junction point, as described in [Specifying a Namespace Extension's Location](nse-junction.md), Windows Explorer allows users to navigate into and out of your namespace extension just like any other folder.</span></span> <span data-ttu-id="46575-106">Es ist jedoch auch möglich, Windows-Explorer zu verwenden, um nur den Inhalt der Namespace Erweiterung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="46575-106">However, it is also possible to use Windows Explorer to display only the contents of your namespace extension.</span></span> <span data-ttu-id="46575-107">Diese Anzeigeoption wird manchmal als Stamm *Ansicht* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="46575-107">This display option is sometimes referred to as a *rooted view*.</span></span> <span data-ttu-id="46575-108">Auch wenn es nicht häufig verwendet wird, können rootansichten normalen Ansichten für einige Erweiterungs Typen vorzuziehen sein.</span><span class="sxs-lookup"><span data-stu-id="46575-108">Although not commonly used, rooted views might be preferable to normal views for some types of extensions.</span></span>

<span data-ttu-id="46575-109">Mit einer Ansicht im Stammverzeichnis wird eine neue Instanz von Windows Explorer erstellt, in der der Inhalt der Erweiterung als separater Namespace angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="46575-109">With a rooted view, a new instance of Windows Explorer is created that displays the contents of the extension as a separate namespace.</span></span> <span data-ttu-id="46575-110">Die Strukturansicht einer Stamm Ansicht zeigt nur die Ordner an, die Teil der Erweiterung sind.</span><span class="sxs-lookup"><span data-stu-id="46575-110">The tree view of a rooted view shows only those folders that are part of the extension.</span></span> <span data-ttu-id="46575-111">Benutzer können nicht von einer rootansicht zu anderen Teilen des Shell-Namespace navigieren.</span><span class="sxs-lookup"><span data-stu-id="46575-111">Users cannot navigate from a rooted view to other parts of the Shell namespace.</span></span>

<span data-ttu-id="46575-112">Erweiterungen werden auf die gleiche Weise für rootansichten implementiert wie für normale Ansichten.</span><span class="sxs-lookup"><span data-stu-id="46575-112">Extensions are implemented in the same way for rooted views as they are for normal views.</span></span> <span data-ttu-id="46575-113">Der einzige Unterschied besteht darin, wie der Inhalt der Erweiterung von Windows-Explorer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="46575-113">The only difference is in the way the contents of the extension are displayed by Windows Explorer.</span></span> <span data-ttu-id="46575-114">Es ist sogar möglich, die Ansichten "Normal" und "Rooting" der gleichen Erweiterung zu haben.</span><span class="sxs-lookup"><span data-stu-id="46575-114">It is even possible to have normal and rooted views of the same extension.</span></span>

<span data-ttu-id="46575-115">Wenn Sie eine Ansicht einer Erweiterung öffnen möchten, müssen Sie eine Instanz von Explorer.exe mit einem/root-Flag starten.</span><span class="sxs-lookup"><span data-stu-id="46575-115">To open a view of an extension, you must launch an instance of Explorer.exe with a /root flag.</span></span> <span data-ttu-id="46575-116">Es gibt verschiedene Möglichkeiten zum Starten einer Ansicht mit Rootzugriff, abhängig von der Art der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="46575-116">There are several different ways to launch a rooted view, depending on the nature of your extension.</span></span>

-   [<span data-ttu-id="46575-117">Verwenden eines Verknüpfungs Punkts zum Öffnen einer rootansicht</span><span class="sxs-lookup"><span data-stu-id="46575-117">How To Use a Junction Point to Open a Rooted View</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
-   [<span data-ttu-id="46575-118">Verwenden einer Verknüpfungs Datei zum Öffnen einer rootansicht</span><span class="sxs-lookup"><span data-stu-id="46575-118">How To Use a Shortcut File to Open a Rooted View</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
-   [<span data-ttu-id="46575-119">Anzeigen einer rootansicht einer Datei</span><span class="sxs-lookup"><span data-stu-id="46575-119">How To Display a Rooted View of a File</span></span>](how-to-display-a-rooted-view-of-a-file.md)

 

 



