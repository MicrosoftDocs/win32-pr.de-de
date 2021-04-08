---
description: Wenn beide Dateien eine Versionsnummer aufweisen, verwendet die Windows Installer die im folgenden Flussdiagramm veranschaulichte Logik, um zu bestimmen, ob alle installierten Dateien, die der Komponente angehören, ersetzt werden sollen.
ms.assetid: c4c8a23b-e1c2-4c96-b708-7cbcbcab4cd4
title: Beide Dateien haben eine Version.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb52c7333e5455d40475c9f845643535b271d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864428"
---
# <a name="both-files-have-a-version"></a><span data-ttu-id="7b58b-103">Beide Dateien haben eine Version.</span><span class="sxs-lookup"><span data-stu-id="7b58b-103">Both Files Have a Version</span></span>

<span data-ttu-id="7b58b-104">Wenn die Schlüsseldatei einer Komponente, die installiert wird (Copy-a) denselben Namen wie eine Datei hat, die bereits am Ziel Speicherort (Copy-B) installiert ist, vergleicht das Installationsprogramm die Versionsnummer und die Sprache der beiden Dateien.</span><span class="sxs-lookup"><span data-stu-id="7b58b-104">If the key file of a component being installed (copy-A) has the same name as a file already installed in the target location (copy-B), the installer compares the version number and language of the two files.</span></span>

<span data-ttu-id="7b58b-105">Wenn beide Dateien eine Versionsnummer aufweisen, verwendet das Installationsprogramm die im folgenden Flussdiagramm veranschaulichte Logik, um zu bestimmen, ob alle installierten Dateien, die der Komponente angehören, ersetzt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7b58b-105">If both files have a version number, the installer uses the logic illustrated by the following flow diagram to determine whether to replace all of the installed files belonging to the component.</span></span> <span data-ttu-id="7b58b-106">Da beim Installer nur die gesamten Komponenten installiert werden, werden alle Dateien der Komponente ersetzt, wenn die installierte Schlüsseldatei ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="7b58b-106">Because the installer only installs entire components, if the installed key file is replaced then all of the component's files are replaced.</span></span>

<span data-ttu-id="7b58b-107">Beachten Sie, dass dieses Diagramm die Standardregeln für die [Datei Versions](file-versioning-rules.md)Verwaltung veranschaulicht, die durch Festlegen der [**REINSTALLMODE**](reinstallmode.md) -Eigenschaft überschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="7b58b-107">Note that this diagram illustrates the default [File Versioning Rules](file-versioning-rules.md), which can be overridden by setting the [**REINSTALLMODE**](reinstallmode.md) property.</span></span> <span data-ttu-id="7b58b-108">Der Standardwert der Eigenschaft **REINSTALLMODE** ist "omus".</span><span class="sxs-lookup"><span data-stu-id="7b58b-108">The default value of the **REINSTALLMODE** property is "omus".</span></span>

![Standardregeln für die Datei Versionsverwaltung, wenn beide Dateien denselben Namen oder dieselbe Versionsnummer aufweisen](images/waiflow1.png)

<span data-ttu-id="7b58b-110">Das vorherige Diagramm kann auch mit Dateien verwendet werden, für die keine Sprache angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7b58b-110">The previous diagram can also be used with files with no language specified.</span></span> <span data-ttu-id="7b58b-111">Wenn Copy-A eine angegebene Sprache hat und für Copy-b keine Sprache angegeben ist, wird Copy-b durch Copy-a ersetzt.</span><span class="sxs-lookup"><span data-stu-id="7b58b-111">If copy-A has a specified language and copy-B has no specified language, copy-B is replaced with copy-A.</span></span> <span data-ttu-id="7b58b-112">Wenn für Copy-A und copy-b keine Sprache angegeben ist, wird Copy-b nicht ersetzt.</span><span class="sxs-lookup"><span data-stu-id="7b58b-112">If copy-A and copy-B both have no language specified, then copy-B is not replaced.</span></span>

<span data-ttu-id="7b58b-113">Weitere Informationen finden Sie unter Beispiele für die Standarddatei Versionsverwaltung beim [Ersetzen vorhandener Dateien](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="7b58b-113">See examples of default file versioning in [Replacing Existing Files](replacing-existing-files.md).</span></span>

-   [<span data-ttu-id="7b58b-114">Keine der Dateien hat eine Version.</span><span class="sxs-lookup"><span data-stu-id="7b58b-114">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="7b58b-115">Keine der Dateien weist eine Version mit Datei Hash Überprüfung auf.</span><span class="sxs-lookup"><span data-stu-id="7b58b-115">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="7b58b-116">Eine Datei hat eine Version.</span><span class="sxs-lookup"><span data-stu-id="7b58b-116">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



