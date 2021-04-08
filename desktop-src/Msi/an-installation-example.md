---
description: In diesem Beispiel wird veranschaulicht, wie ein einfaches Windows Installer Paket erstellt wird, mit dem eine Anwendung installiert wird.
ms.assetid: eee1e3e6-74e9-41d0-b732-1f792a4df423
title: Ein Installations Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eefaab2977bf7cc31e86ac7541b21b345c1aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864492"
---
# <a name="an-installation-example"></a><span data-ttu-id="d6bc3-103">Ein Installations Beispiel</span><span class="sxs-lookup"><span data-stu-id="d6bc3-103">An Installation Example</span></span>

<span data-ttu-id="d6bc3-104">In diesem Beispiel wird veranschaulicht, wie ein einfaches Windows Installer Paket erstellt wird, mit dem eine Anwendung installiert wird.</span><span class="sxs-lookup"><span data-stu-id="d6bc3-104">This example illustrates how to create a simple Windows Installer package that installs an application.</span></span> <span data-ttu-id="d6bc3-105">Das Beispiel installiert Notepad, einen Text-Editor, der in Windows enthalten ist, und mehrere Textdateien, die Ereignisse und Eintritte in der imaginären roten Park Arena beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d6bc3-105">The sample installs Notepad, a text editor included with Windows, and several text files describing events and admissions at the imaginary Red Park Arena.</span></span>

<span data-ttu-id="d6bc3-106">Das Beispiel verfügt über die folgenden Spezifikationen:</span><span class="sxs-lookup"><span data-stu-id="d6bc3-106">The sample has the following specifications:</span></span>

-   <span data-ttu-id="d6bc3-107">Die Anwendung wird Benutzern als selbst installierendes Windows Installer Paket bereitgestellt, mit dem alle erforderlichen Dateien, Verknüpfungen und Registrierungsinformationen installiert werden.</span><span class="sxs-lookup"><span data-stu-id="d6bc3-107">The application is provided to users as a self-installing Windows Installer package that installs all the required files, shortcuts, and registry information.</span></span>
-   <span data-ttu-id="d6bc3-108">Das Installationspaket stellt dem Benutzer während des Setups möglicherweise einen Benutzeroberflächen-Assistenten zur Verfügung, um Benutzerinformationen zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="d6bc3-108">The installation package may present a UI wizard to the user during setup to collect user information.</span></span>
-   <span data-ttu-id="d6bc3-109">Während des Setups haben Benutzer die Möglichkeit, einzelne Funktionen auszuwählen, die für die lokale Installation, die aus der Quelle auszuwählende oder nicht installiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d6bc3-109">During setup, users have the option of selecting individual features to be installed to run-locally, to run-from-source, or to not be installed.</span></span>
-   <span data-ttu-id="d6bc3-110">Eines der Features kann Benutzern als Funktion zum Installieren nach Bedarf angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d6bc3-110">One of the features can be presented to users as an install-on-demand feature.</span></span>
-   <span data-ttu-id="d6bc3-111">Mit demselben Paket wird die Anwendung deinstalliert, und alle Anwendungs Dateien und Registrierungsinformationen werden auf dem Computer des Benutzers entfernt.</span><span class="sxs-lookup"><span data-stu-id="d6bc3-111">The same package uninstalls the application and removes all the application files and registry information from the user's computer.</span></span>
-   <span data-ttu-id="d6bc3-112">Das Paket ist darauf vorbereitet, ein umfangreiches Upgrade zu erhalten, das das Ändern des Produktcodes umfasst.</span><span class="sxs-lookup"><span data-stu-id="d6bc3-112">The package is prepared to receive a major upgrade that includes changing its product code.</span></span>

<span data-ttu-id="d6bc3-113">Um das Beispiel zu reproduzieren, benötigen Sie ein Software Tool, das eine leere Windows Installer Datenbank erstellen und bearbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="d6bc3-113">To reproduce the example, you need a software tool capable of creating and editing a blank Windows Installer database.</span></span> <span data-ttu-id="d6bc3-114">Mehrere Tools zur Paket Erstellung sind von unabhängigen Softwareanbietern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d6bc3-114">Several package creation tools are available from independent software vendors.</span></span> <span data-ttu-id="d6bc3-115">Ein Windows Installer Datenbank-Editor namens Orca wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d6bc3-115">A Windows Installer database editor called Orca is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="d6bc3-116">Um das Beispiel abzuschließen, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="d6bc3-116">To complete the example, follow these steps:</span></span>

[<span data-ttu-id="d6bc3-117">Planen der Installation</span><span class="sxs-lookup"><span data-stu-id="d6bc3-117">Planning the Installation</span></span>](planning-the-installation.md)

[<span data-ttu-id="d6bc3-118">Importieren einer leeren Datenbank</span><span class="sxs-lookup"><span data-stu-id="d6bc3-118">Importing a Blank Database</span></span>](importing-a-blank-database.md)

[<span data-ttu-id="d6bc3-119">Angeben der Verzeichnisstruktur</span><span class="sxs-lookup"><span data-stu-id="d6bc3-119">Specifying Directory Structure</span></span>](specifying-directory-structure.md)

[<span data-ttu-id="d6bc3-120">Angeben von Komponenten</span><span class="sxs-lookup"><span data-stu-id="d6bc3-120">Specifying Components</span></span>](specifying-components.md)

[<span data-ttu-id="d6bc3-121">Angeben von Dateien und Dateiattributen</span><span class="sxs-lookup"><span data-stu-id="d6bc3-121">Specifying Files and File Attributes</span></span>](specifying-files-and-file-attributes.md)

[<span data-ttu-id="d6bc3-122">Angeben von Quell Medien</span><span class="sxs-lookup"><span data-stu-id="d6bc3-122">Specifying Source Media</span></span>](specifying-source-media.md)

[<span data-ttu-id="d6bc3-123">Angeben von Features</span><span class="sxs-lookup"><span data-stu-id="d6bc3-123">Specifying Features</span></span>](specifying-features.md)

[<span data-ttu-id="d6bc3-124">Angeben von Feature-Component Beziehungen</span><span class="sxs-lookup"><span data-stu-id="d6bc3-124">Specifying Feature-Component Relationships</span></span>](specifying-feature-component-relationships.md)

[<span data-ttu-id="d6bc3-125">Registrierungsinformationen werden hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="d6bc3-125">Adding Registry Information</span></span>](adding-registry-information.md)

[<span data-ttu-id="d6bc3-126">Angeben von Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="d6bc3-126">Specifying Shortcuts</span></span>](specifying-shortcuts.md)

[<span data-ttu-id="d6bc3-127">Angeben von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d6bc3-127">Specifying Properties</span></span>](specifying-properties.md)

[<span data-ttu-id="d6bc3-128">Importieren von InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="d6bc3-128">Importing the InstallExecuteSequence</span></span>](importing-the-installexecutesequence.md)

[<span data-ttu-id="d6bc3-129">Importieren der InstallUISequence-Sequenz</span><span class="sxs-lookup"><span data-stu-id="d6bc3-129">Importing the InstallUISequence</span></span>](importing-the-installuisequence.md)

[<span data-ttu-id="d6bc3-130">Importieren von "AdminExecuteSequence"</span><span class="sxs-lookup"><span data-stu-id="d6bc3-130">Importing the AdminExecuteSequence</span></span>](importing-the-adminexecutesequence.md)

[<span data-ttu-id="d6bc3-131">Importieren der AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="d6bc3-131">Importing the AdminUISequence</span></span>](importing-the-adminuisequence.md)

[<span data-ttu-id="d6bc3-132">Importieren von AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="d6bc3-132">Importing the AdvtExecuteSequence</span></span>](importing-the-advtexecutesequence.md)

[<span data-ttu-id="d6bc3-133">Hinzufügen von Übersichts Informationen</span><span class="sxs-lookup"><span data-stu-id="d6bc3-133">Adding Summary Information</span></span>](adding-summary-information.md)

[<span data-ttu-id="d6bc3-134">Importieren der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d6bc3-134">Importing the User Interface</span></span>](importing-the-user-interface.md)

[<span data-ttu-id="d6bc3-135">Überprüfen einer Installations Datenbank</span><span class="sxs-lookup"><span data-stu-id="d6bc3-135">Validating an Installation Database</span></span>](validating-an-installation-database.md)

 

 



