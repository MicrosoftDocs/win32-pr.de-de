---
description: Die Windows-Benutzeroberfläche ermöglicht Benutzern den Zugriff auf eine Vielzahl von Objekten, die zum Ausführen von Anwendungen und zum Verwalten des Betriebssystems erforderlich sind.
title: Shellentwickler Handbuch
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f88ef25-3645-4f54-9453-41f919c0fc0a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1be17ca90b7138294be3e1b34fa3fcb4dcb4227a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993854"
---
# <a name="shell-developers-guide"></a><span data-ttu-id="a40ff-103">Shellentwickler Handbuch</span><span class="sxs-lookup"><span data-stu-id="a40ff-103">Shell Developer's Guide</span></span>

<span data-ttu-id="a40ff-104">Die Windows-Benutzeroberfläche ermöglicht Benutzern den Zugriff auf eine Vielzahl von Objekten, die zum Ausführen von Anwendungen und zum Verwalten des Betriebssystems erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="a40ff-104">The Windows UI provides users with access to a wide variety of objects necessary to run applications and manage the operating system.</span></span> <span data-ttu-id="a40ff-105">Die häufigsten und vertrauten Objekte sind die Ordner und Dateien, die sich auf Computer Laufwerken befinden.</span><span class="sxs-lookup"><span data-stu-id="a40ff-105">The most numerous and familiar of these objects are the folders and files that reside on computer disk drives.</span></span> <span data-ttu-id="a40ff-106">Es gibt auch eine Reihe von virtuellen Objekten, die es dem Benutzer ermöglichen, Aufgaben auszuführen, z. b. das Senden von Dateien an Remote Drucker oder den Zugriff auf den Papierkorb.</span><span class="sxs-lookup"><span data-stu-id="a40ff-106">There are also a number of virtual objects that allow the user to do tasks such as sending files to remote printers or accessing the Recycle Bin.</span></span> <span data-ttu-id="a40ff-107">Die Shell organisiert diese Objekte in einem hierarchischen Namespace und bietet Benutzern und Anwendungen eine konsistente und effiziente Möglichkeit, auf Objekte zuzugreifen und diese zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a40ff-107">The Shell organizes these objects into a hierarchical namespace, and provides users and applications with a consistent and efficient way to access and manage objects.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a40ff-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a40ff-108">In this section</span></span>

-   [<span data-ttu-id="a40ff-109">Überlegungen zur Sicherheit: Microsoft Windows Shell</span><span class="sxs-lookup"><span data-stu-id="a40ff-109">Security Considerations: Microsoft Windows Shell</span></span>](sec-shell.md)
-   [<span data-ttu-id="a40ff-110">Leitfaden für die Implementierung von In-Process-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="a40ff-110">Guidance for Implementing In-Process Extensions</span></span>](shell-and-managed-code.md)
-   [<span data-ttu-id="a40ff-111">Versionen der Shell und der allgemeinen Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="a40ff-111">Shell and Common Controls Versions</span></span>](versions.md)
-   [<span data-ttu-id="a40ff-112">Implementieren der grundlegenden Ordner Objekt Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a40ff-112">Implementing the Basic Folder Object Interfaces</span></span>](nse-implement.md)
-   [<span data-ttu-id="a40ff-113">Implementieren eines benutzerdefinierten Datei Formats</span><span class="sxs-lookup"><span data-stu-id="a40ff-113">Implementing a Custom File Format</span></span>](customizing-file-types-bumper.md)
-   [<span data-ttu-id="a40ff-114">Shellerweiterbarkeit (Erstellen einer Datenquelle)</span><span class="sxs-lookup"><span data-stu-id="a40ff-114">Shell Extensibility (Creating a Data Source)</span></span>](shell-extensibility-bumper.md)
-   [<span data-ttu-id="a40ff-115">Implementieren von System Steuerungselementen</span><span class="sxs-lookup"><span data-stu-id="a40ff-115">Implementing Control Panel Items</span></span>](control-panel-applications.md)
-   [<span data-ttu-id="a40ff-116">Unterstützen von Shellanwendungen</span><span class="sxs-lookup"><span data-stu-id="a40ff-116">Supporting Shell Applications</span></span>](application-support-bumper.md)
-   [<span data-ttu-id="a40ff-117">Legacy-shellthemen</span><span class="sxs-lookup"><span data-stu-id="a40ff-117">Legacy Shell Topics</span></span>](miscellaneous-topics-bumper.md)

## <a name="document-conventions"></a><span data-ttu-id="a40ff-118">Dokument Konventionen</span><span class="sxs-lookup"><span data-stu-id="a40ff-118">Document Conventions</span></span>

<span data-ttu-id="a40ff-119">Das shellentwickler Handbuch befolgt die üblichen Dokument Konventionen des Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="a40ff-119">The Shell Developers's Guide follows the usual Windows Software Development Kit (SDK) document conventions.</span></span> <span data-ttu-id="a40ff-120">Insbesondere müssen zwei Konventionen beachtet werden:</span><span class="sxs-lookup"><span data-stu-id="a40ff-120">Two conventions in particular should be noted:</span></span>

-   <span data-ttu-id="a40ff-121">Der Beispielcode lässt normalen Fehlerkorrektur Code aus.</span><span class="sxs-lookup"><span data-stu-id="a40ff-121">Sample code omits normal error-correction code.</span></span> <span data-ttu-id="a40ff-122">Dieser Code wurde nur entfernt, um den Code lesbarer zu machen.</span><span class="sxs-lookup"><span data-stu-id="a40ff-122">This code has been removed only to make the code more readable.</span></span> <span data-ttu-id="a40ff-123">Sie sollten den entsprechenden Fehlerkorrektur Code in Ihre eigenen Anwendungen einschließen.</span><span class="sxs-lookup"><span data-stu-id="a40ff-123">You should include all appropriate error-correction code in your own applications.</span></span>
-   <span data-ttu-id="a40ff-124">Um Beispiel Registrierungseinträge zu löschen, werden Schlüssel, Unterschlüssel und Eintrags Namen sowie Werte mit einer Standard Schriftart angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a40ff-124">To make sample registry entries clear, key, subkey, and entry names as well as values are displayed with a standard font.</span></span> <span data-ttu-id="a40ff-125">Benutzer-oder Anwendungs definierte Elementnamen werden kursiv formatiert.</span><span class="sxs-lookup"><span data-stu-id="a40ff-125">User or application-defined item names are italicized.</span></span>

 

 



