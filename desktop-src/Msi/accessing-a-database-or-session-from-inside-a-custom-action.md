---
description: Über eine benutzerdefinierte Aktion, die nicht die aktuelle Installationssitzung ist, kann nicht auf eine installersitzung zugegriffen werden.
ms.assetid: 8aa0ac17-1341-4399-987e-d26175150874
title: Zugreifen auf eine Datenbank oder eine Sitzung innerhalb einer benutzerdefinierten Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 839c34fbfcd6cc69c026db455b0c2e3a59a28e2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959557"
---
# <a name="accessing-a-database-or-session-from-inside-a-custom-action"></a><span data-ttu-id="e49eb-103">Zugreifen auf eine Datenbank oder eine Sitzung innerhalb einer benutzerdefinierten Aktion</span><span class="sxs-lookup"><span data-stu-id="e49eb-103">Accessing a Database or Session from Inside a Custom Action</span></span>

<span data-ttu-id="e49eb-104">Über eine benutzerdefinierte Aktion, die nicht die aktuelle Installationssitzung ist, kann nicht auf eine installersitzung zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="e49eb-104">You cannot access an installer session from a custom action that is not the current installation session.</span></span> <span data-ttu-id="e49eb-105">Benutzerdefinierte Aktionen können nur mit der aktiven Datenbank der Sitzung und ohne andere Datenbanken arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e49eb-105">Custom actions are limited to working with only the active database of the session and no other databases.</span></span> <span data-ttu-id="e49eb-106">Die folgenden Windows Installer- [Datenbankfunktionen](database-functions.md) dürfen nicht von einer benutzerdefinierten Aktion aufgerufen werden, da Sie ein Handle für eine Datenbank erfordern, bei der es sich nicht um die Datenbank der aktuellen Installationssitzung handelt:</span><span class="sxs-lookup"><span data-stu-id="e49eb-106">The following Windows Installer [Database Functions](database-functions.md) must not be called from a custom action, because they require a handle to a database that is not the database of the current installation session:</span></span>

[<span data-ttu-id="e49eb-107">**Msidatabasemerge**</span><span class="sxs-lookup"><span data-stu-id="e49eb-107">**MsiDatabaseMerge**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

[<span data-ttu-id="e49eb-108">**Msikreatetransformsummaryinfo**</span><span class="sxs-lookup"><span data-stu-id="e49eb-108">**MsiCreateTransformSummaryInfo**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)

 

[<span data-ttu-id="e49eb-109">**Msidatabaseapplytransform**</span><span class="sxs-lookup"><span data-stu-id="e49eb-109">**MsiDatabaseApplyTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma)

 

[<span data-ttu-id="e49eb-110">**Msidatabasecommit**</span><span class="sxs-lookup"><span data-stu-id="e49eb-110">**MsiDatabaseCommit**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)

 

[<span data-ttu-id="e49eb-111">**Msidatabaseexport**</span><span class="sxs-lookup"><span data-stu-id="e49eb-111">**MsiDatabaseExport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta)

 

[<span data-ttu-id="e49eb-112">**Msidatabasegeneratetransform**</span><span class="sxs-lookup"><span data-stu-id="e49eb-112">**MsiDatabaseGenerateTransform**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma)

 

[<span data-ttu-id="e49eb-113">**Msidatabaseimport**</span><span class="sxs-lookup"><span data-stu-id="e49eb-113">**MsiDatabaseImport**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)

 

[<span data-ttu-id="e49eb-114">**Msienableuipreview**</span><span class="sxs-lookup"><span data-stu-id="e49eb-114">**MsiEnableUIPreview**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview)

 

[<span data-ttu-id="e49eb-115">**Msigetdatabasestate**</span><span class="sxs-lookup"><span data-stu-id="e49eb-115">**MsiGetDatabaseState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate)

## <a name="related-topics"></a><span data-ttu-id="e49eb-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e49eb-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e49eb-117">Zugreifen auf die aktuelle Installer-Sitzung innerhalb einer benutzerdefinierten Aktion</span><span class="sxs-lookup"><span data-stu-id="e49eb-117">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
</dt> </dl>

 

 



