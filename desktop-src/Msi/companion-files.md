---
description: Der Installationsstatus einer Begleit Datei hängt nicht von den eigenen Datei Versionsinformationen, sondern von der Versionsverwaltung des zugehörigen übergeordneten Elements ab.
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: Begleit Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c927c377c7111e89c6f97b385610da9e09f8bdd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960269"
---
# <a name="companion-files"></a><span data-ttu-id="cc48f-103">Begleit Dateien</span><span class="sxs-lookup"><span data-stu-id="cc48f-103">Companion Files</span></span>

<span data-ttu-id="cc48f-104">Der Installationsstatus einer Begleit Datei hängt nicht von den eigenen Datei Versionsinformationen, sondern von der Versionsverwaltung des zugehörigen übergeordneten Elements ab.</span><span class="sxs-lookup"><span data-stu-id="cc48f-104">The installation state of a companion file depends not on its own file versioning information, but on the versioning of its companion parent.</span></span> <span data-ttu-id="cc48f-105">Sehen Sie sich die Regeln für die [Datei Versions](file-versioning-rules.md)Verwaltung an.</span><span class="sxs-lookup"><span data-stu-id="cc48f-105">See the [File Versioning Rules](file-versioning-rules.md).</span></span> <span data-ttu-id="cc48f-106">Um eine Begleit Datei anzugeben, muss der Primärschlüssel des übergeordneten Elements in der [Dateitabelle](file-table.md) in der Versions Spalte des Datensatzes für den begleitenden erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="cc48f-106">To specify a companion file, the primary key of the companion parent in the [File table](file-table.md) must be authored into the Version column of the record for the companion.</span></span>

<span data-ttu-id="cc48f-107">Im folgenden Beispiel ist fileA das übergeordnete Element, und fileB ist die Begleit Datei.</span><span class="sxs-lookup"><span data-stu-id="cc48f-107">In the following example, FileA is the companion parent and FileB is the companion file.</span></span>

<span data-ttu-id="cc48f-108">[Dateitabelle](file-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="cc48f-108">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="cc48f-109">File</span><span class="sxs-lookup"><span data-stu-id="cc48f-109">File</span></span>  | <span data-ttu-id="cc48f-110">Version</span><span class="sxs-lookup"><span data-stu-id="cc48f-110">Version</span></span> |
|-------|---------|
| <span data-ttu-id="cc48f-111">Mit der</span><span class="sxs-lookup"><span data-stu-id="cc48f-111">FileA</span></span> | <span data-ttu-id="cc48f-112">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="cc48f-112">1.0.0.0</span></span> |
| <span data-ttu-id="cc48f-113">FileB</span><span class="sxs-lookup"><span data-stu-id="cc48f-113">FileB</span></span> | <span data-ttu-id="cc48f-114">Mit der</span><span class="sxs-lookup"><span data-stu-id="cc48f-114">FileA</span></span>   |



 

<span data-ttu-id="cc48f-115">In diesem Beispiel hängt der Installationsstatus von fileB von den Regeln für die [Datei Versions](file-versioning-rules.md) Verwaltung und den Versionsinformationen für fileA ab.</span><span class="sxs-lookup"><span data-stu-id="cc48f-115">In this example, the installation state of FileB depends on the [File Versioning Rules](file-versioning-rules.md) and the versioning information for FileA.</span></span> <span data-ttu-id="cc48f-116">Wenn das Installationsprogramm feststellt, dass die Version von fileA im Paket über eine ältere Version von fileA installiert werden soll, die bereits auf dem Computer des Benutzers vorhanden ist, wird fileB unabhängig von der Version der installierten fileB aus dem Paket installiert.</span><span class="sxs-lookup"><span data-stu-id="cc48f-116">If the installer determines that the version of FileA in the package should be installed over an older version of FileA that already exists on the user's computer, it will also install FileB from the package regardless of the version of any installed FileB.</span></span>

<span data-ttu-id="cc48f-117">Beachten Sie, dass es sich bei einer Datei, die den Schlüssel Pfad für Ihre Komponente ist, nicht um eine Begleit Datei handeln darf.</span><span class="sxs-lookup"><span data-stu-id="cc48f-117">Note that a file that is the key path for its component must not be a companion file.</span></span> <span data-ttu-id="cc48f-118">Dies würde dazu führen, dass die versionierungslogik der Schlüssel Pfad Datei von der begleitenden übergeordneten Datei bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="cc48f-118">This would result in the versioning logic of the key path file being determined by the companion parent file.</span></span>

 

 



