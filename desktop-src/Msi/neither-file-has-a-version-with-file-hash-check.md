---
description: File hashingist mit Windows Installer verfügbar. Weitere Informationen finden Sie unter msigetflehash und in der Tabelle msigetfash. Die msiflehash-Tabelle kann nur mit Dateien ohne Versions Angabe verwendet werden.
ms.assetid: 608859ac-6640-4c28-b4f0-34ab36d804d7
title: Keine der Dateien weist eine Version mit Datei Hash Überprüfung auf.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 415019838ac29418b13b513b393a18af2131510f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528172"
---
# <a name="neither-file-has-a-version-with-file-hash-check"></a><span data-ttu-id="5eea7-105">Keine der Dateien weist eine Version mit Datei Hash Überprüfung auf.</span><span class="sxs-lookup"><span data-stu-id="5eea7-105">Neither File Has a Version with File Hash Check</span></span>

<span data-ttu-id="5eea7-106">File hashingist mit Windows Installer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5eea7-106">File hashing is available with Windows Installer.</span></span> <span data-ttu-id="5eea7-107">Weitere Informationen finden Sie unter [**msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) und in der [Tabelle msigetfash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="5eea7-107">For more information, see [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) and the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="5eea7-108">Die msiflehash-Tabelle kann nur mit Dateien ohne Versions Angabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5eea7-108">The MsiFileHash table can only be used with unversioned files.</span></span>

<span data-ttu-id="5eea7-109">Wenn die Schlüsseldatei einer installierten Komponente (Copy-a) denselben Namen wie eine Datei hat, die bereits am Ziel Speicherort (Copy-B) installiert ist, vergleicht das Installationsprogramm die Versionsnummer, das Datum und die Sprache der beiden Dateien.</span><span class="sxs-lookup"><span data-stu-id="5eea7-109">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number, date, and language of the two files.</span></span>

<span data-ttu-id="5eea7-110">Wenn keine der Dateien über eine Versionsnummer verfügt, verwendet das Installationsprogramm die im folgenden Flussdiagramm veranschaulichte Logik, um zu bestimmen, ob alle installierten Dateien, die der Komponente angehören, ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5eea7-110">If neither file has a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="5eea7-111">Da beim Installer nur die gesamten Komponenten installiert werden, werden alle Dateien der Komponente ersetzt, wenn die installierte Schlüsseldatei ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="5eea7-111">Because the installer only installs entire components, if the installed key file is replaced then, all of the component's files are replaced.</span></span>

<span data-ttu-id="5eea7-112">Beachten Sie, dass dieses Diagramm die Standardregeln für die [Datei Versions](file-versioning-rules.md)Verwaltung veranschaulicht, die durch Festlegen der [**REINSTALLMODE**](reinstallmode.md) -Eigenschaft überschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="5eea7-112">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="5eea7-113">Der Standardwert der Eigenschaft **REINSTALLMODE** ist "omus".</span><span class="sxs-lookup"><span data-stu-id="5eea7-113">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![Standardregeln für die Datei Versionsverwaltung, wenn Sie durch die rein Stall Mode-Eigenschaften Einstellung überschrieben werden](images/waiflow2b.png)

<span data-ttu-id="5eea7-115">Weitere Informationen finden Sie in den Beispielen für die Standarddatei Versionsverwaltung beim [Ersetzen vorhandener Dateien](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="5eea7-115">See the examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="5eea7-116">Beide Dateien haben eine Version.</span><span class="sxs-lookup"><span data-stu-id="5eea7-116">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="5eea7-117">Keine der Dateien hat eine Version.</span><span class="sxs-lookup"><span data-stu-id="5eea7-117">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="5eea7-118">Eine Datei hat eine Version.</span><span class="sxs-lookup"><span data-stu-id="5eea7-118">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



