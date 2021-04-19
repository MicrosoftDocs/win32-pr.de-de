---
description: Ein-Installationspaket enthält alle Informationen, die die Windows Installer zum Installieren oder Deinstallieren einer Anwendung oder eines Produkts und zum Ausführen der Setup-Benutzeroberfläche benötigt.
ms.assetid: 532b3492-919f-4999-b86c-e3c210876141
title: Installationspaket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe5e5ff79d0c868036dd12ed533b1cd18f9f70d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349281"
---
# <a name="installation-package"></a><span data-ttu-id="7a745-103">Installationspaket</span><span class="sxs-lookup"><span data-stu-id="7a745-103">Installation Package</span></span>

<span data-ttu-id="7a745-104">Ein-Installationspaket enthält alle Informationen, die die Windows Installer zum Installieren oder Deinstallieren einer Anwendung oder eines Produkts und zum Ausführen der Setup-Benutzeroberfläche benötigt.</span><span class="sxs-lookup"><span data-stu-id="7a745-104">An installation package contains all of the information that the Windows Installer requires to install or uninstall an application or product and to run the setup user interface.</span></span> <span data-ttu-id="7a745-105">Jedes Installationspaket enthält eine MSI-Datei, die eine Installations Datenbank, einen Zusammenfassungs Datenstrom und Datenströme für verschiedene Teile der Installation enthält.</span><span class="sxs-lookup"><span data-stu-id="7a745-105">Each installation package includes an .msi file, containing an installation database, a summary information stream, and data streams for various parts of the installation.</span></span> <span data-ttu-id="7a745-106">Die MSI-Datei kann auch eine oder mehrere Transformationen, interne Quelldateien und externe Quelldateien oder CAB-Dateien enthalten, die für die Installation erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7a745-106">The .msi file can also contain one or more transforms, internal source files, and external source files or cabinet files required by the installation.</span></span>

<span data-ttu-id="7a745-107">Anwendungsentwickler müssen eine Installation erstellen, um das Installationsprogramm zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a745-107">Application developers must author an installation to use the installer.</span></span> <span data-ttu-id="7a745-108">Da das Installationsprogramm Installationen im Zusammenhang mit dem Konzept der [Komponenten und Features](components-and-features.md)organisiert und alle Informationen zur Installation in einer relationalen Datenbank speichert, umfasst der Prozess der Erstellung eines Installationspakets im Allgemeinen die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="7a745-108">Because the installer organizes installations around the concept of [components and features](components-and-features.md), and stores all information about the installation in a relational database, the process of authoring an installation package broadly entails the following steps:</span></span>

-   <span data-ttu-id="7a745-109">Identifizieren Sie die Features, die Benutzern angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7a745-109">Identify the features to be presented to users.</span></span>
-   <span data-ttu-id="7a745-110">Organisieren Sie die Anwendung in Komponenten.</span><span class="sxs-lookup"><span data-stu-id="7a745-110">Organize the application into components.</span></span>
-   <span data-ttu-id="7a745-111">Füllen Sie die Installations Datenbank mit Informationen auf.</span><span class="sxs-lookup"><span data-stu-id="7a745-111">Populate the installation database with information.</span></span>
-   <span data-ttu-id="7a745-112">Überprüfen Sie das Installationspaket.</span><span class="sxs-lookup"><span data-stu-id="7a745-112">Validate the installation package.</span></span>

<span data-ttu-id="7a745-113">Im nächsten Abschnitt werden die Installationsprogramm Komponenten und-Funktionen erläutert.</span><span class="sxs-lookup"><span data-stu-id="7a745-113">The next section discusses installer components and features.</span></span> <span data-ttu-id="7a745-114">Weitere Informationen finden Sie unter [Komponenten und Features](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="7a745-114">For more information, see [Components and Features](components-and-features.md).</span></span> <span data-ttu-id="7a745-115">Die Auswahl der Features hängt häufig von der Funktionalität der Anwendung aus der Sicht des Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="7a745-115">The choice of features is commonly determined by the application's functionality from the user's perspective.</span></span>

<span data-ttu-id="7a745-116">Es wird empfohlen, dass Entwickler ein Standardverfahren zum Auswählen von-Komponenten verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a745-116">It is recommended that developers use a standard procedure for choosing components.</span></span> <span data-ttu-id="7a745-117">Weitere Informationen finden Sie unter [Organisieren von Anwendungen in Komponenten](organizing-applications-into-components.md).</span><span class="sxs-lookup"><span data-stu-id="7a745-117">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

<span data-ttu-id="7a745-118">Paket Autoren können Paket Erstellungs Tools von Drittanbietern oder einen Tabellen-Editor und das Windows Installer SDK zum Auffüllen der Installations Datenbank verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a745-118">Package authors can use third-party package creation tools, or a table editor and the Windows Installer SDK, to populate the installation database.</span></span> <span data-ttu-id="7a745-119">Alle Installationspakete müssen auf interne Konsistenz überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="7a745-119">All installation packages need to be validated for internal consistency.</span></span> <span data-ttu-id="7a745-120">Weitere Informationen finden Sie unter [Paket Validierung](package-validation.md).</span><span class="sxs-lookup"><span data-stu-id="7a745-120">For more information, see [Package Validation](package-validation.md).</span></span>

 

 



