---
description: In den Flussdiagrammen in den folgenden Abschnitten werden die Standardregeln für die Datei Versionsverwaltung veranschaulicht, die verwendet werden, wenn die Schlüsseldatei einer installierten Komponente den gleichen Namen wie eine Datei hat, die bereits am Ziel Speicherort installiert ist.
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: Standardmäßige Datei Versionsverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad33a7af49c28b560d9d558abbc86b220c4cb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866360"
---
# <a name="default-file-versioning"></a><span data-ttu-id="53b4b-103">Standardmäßige Datei Versionsverwaltung</span><span class="sxs-lookup"><span data-stu-id="53b4b-103">Default File Versioning</span></span>

<span data-ttu-id="53b4b-104">In den Flussdiagrammen in den folgenden Abschnitten werden die Standardregeln für die Datei Versionsverwaltung veranschaulicht, die verwendet werden, wenn die Schlüsseldatei einer installierten Komponente den gleichen Namen wie eine Datei hat, die bereits am Ziel Speicherort installiert ist.</span><span class="sxs-lookup"><span data-stu-id="53b4b-104">The flow diagrams in the following sections illustrate the default file versioning rules used when the key file of a component being installed has the same name as a file already installed in the target location.</span></span> <span data-ttu-id="53b4b-105">Die Standarddatei Versionsverwaltung wird auch unter [Ersetzen vorhandener Dateien](replacing-existing-files.md)veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="53b4b-105">Default file versioning is also illustrated in [Replacing Existing Files](replacing-existing-files.md).</span></span>

<span data-ttu-id="53b4b-106">Beachten Sie, dass mit Windows Installer Datei Hashwert zur Optimierung des Kopierens von Dateien verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="53b4b-106">Note that with Windows Installer, file hashing is available to optimize the copying of files.</span></span> <span data-ttu-id="53b4b-107">Weitere Informationen finden Sie unter [**msigetflehash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) und in der [Tabelle msigetfash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="53b4b-107">For details, see [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) and the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="53b4b-108">Die msiflehash-Tabelle kann nur mit Dateien ohne Versions Angabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="53b4b-108">The MsiFileHash table can only be used with unversioned files.</span></span>

-   [<span data-ttu-id="53b4b-109">Beide Dateien haben eine Version.</span><span class="sxs-lookup"><span data-stu-id="53b4b-109">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="53b4b-110">Keine der Dateien hat eine Version.</span><span class="sxs-lookup"><span data-stu-id="53b4b-110">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="53b4b-111">Keine der Dateien weist eine Version mit Datei Hash Überprüfung auf.</span><span class="sxs-lookup"><span data-stu-id="53b4b-111">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="53b4b-112">Eine Datei hat eine Version.</span><span class="sxs-lookup"><span data-stu-id="53b4b-112">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



