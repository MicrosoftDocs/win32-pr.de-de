---
description: Wenn nur eine der Dateien über eine Versionsnummer verfügt, verwendet die Windows Installer die im folgenden Flussdiagramm veranschaulichte Logik, um zu bestimmen, ob alle installierten Dateien, die der Komponente angehören, ersetzt werden sollen.
ms.assetid: 1eda5521-6e23-49b8-9870-f5370def487e
title: Eine Datei hat eine Version.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417060119f8b13b1545161faa80552c79e8ca9aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130284"
---
# <a name="one-file-has-a-version"></a><span data-ttu-id="51440-103">Eine Datei hat eine Version.</span><span class="sxs-lookup"><span data-stu-id="51440-103">One File Has a Version</span></span>

<span data-ttu-id="51440-104">Wenn die Schlüsseldatei einer installierten Komponente (Copy-a) denselben Namen wie eine Datei hat, die bereits am Ziel Speicherort (Copy-B) installiert ist, vergleicht das Installationsprogramm die Versionsnummer, das Datum und die Sprache der beiden Dateien.</span><span class="sxs-lookup"><span data-stu-id="51440-104">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number, date, and language of the two files.</span></span>

<span data-ttu-id="51440-105">Wenn nur eine der Dateien über eine Versionsnummer verfügt, verwendet das Installationsprogramm die im folgenden Flussdiagramm veranschaulichte Logik, um zu bestimmen, ob alle installierten Dateien, die der Komponente angehören, ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="51440-105">If only one of the files has a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="51440-106">Da beim Installer nur die gesamten Komponenten installiert werden, werden alle Dateien der Komponente ersetzt, wenn die installierte Schlüsseldatei ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="51440-106">Because the installer only installs entire components, if the installed key file is replaced, then all of the component's files are replaced.</span></span>

<span data-ttu-id="51440-107">Beachten Sie, dass dieses Diagramm die Standardregeln für die [Datei Versions](file-versioning-rules.md)Verwaltung veranschaulicht, die durch Festlegen der [**REINSTALLMODE**](reinstallmode.md) -Eigenschaft überschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="51440-107">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="51440-108">Der Standardwert der Eigenschaft **REINSTALLMODE** ist "omus".</span><span class="sxs-lookup"><span data-stu-id="51440-108">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![Standardregeln für die Datei Versionsverwaltung, wenn nur eine Datei eine Versionsnummer aufweist](images/waiflow3.png)

<span data-ttu-id="51440-110">Weitere Informationen finden Sie in den Beispielen für die Standarddatei Versionsverwaltung beim [Ersetzen vorhandener Dateien](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="51440-110">See the examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="51440-111">Beide Dateien haben eine Version.</span><span class="sxs-lookup"><span data-stu-id="51440-111">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="51440-112">Keine der Dateien hat eine Version.</span><span class="sxs-lookup"><span data-stu-id="51440-112">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="51440-113">Keine der Dateien weist eine Version mit Datei Hash Überprüfung auf.</span><span class="sxs-lookup"><span data-stu-id="51440-113">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)

 

 



