---
description: Mit der Aktion "installadminpackage" wird die Produktdatenbank auf den administrativen Installations Punkt kopiert, der durch die Eigenschaft "TARGETDIR" definiert wird.
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: Installadminpackage-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1eb2f86390fe3a47a6d100a887d34798e7f4d4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959496"
---
# <a name="installadminpackage-action"></a><span data-ttu-id="f31cf-103">Installadminpackage-Aktion</span><span class="sxs-lookup"><span data-stu-id="f31cf-103">InstallAdminPackage Action</span></span>

<span data-ttu-id="f31cf-104">Mit der Aktion "installadminpackage" wird die Produktdatenbank auf den administrativen Installations Punkt kopiert, der durch die Eigenschaft " [**TARGETDIR**](targetdir.md) " definiert wird.</span><span class="sxs-lookup"><span data-stu-id="f31cf-104">The InstallAdminPackage action copies the product database to the administrative installation point, which is defined by the [**TARGETDIR**](targetdir.md) property.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="f31cf-105">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="f31cf-105">Sequence Restrictions</span></span>

<span data-ttu-id="f31cf-106">Es gibt keine Sequenz Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="f31cf-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="f31cf-107">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="f31cf-107">ActionData Messages</span></span>



| <span data-ttu-id="f31cf-108">Feld</span><span class="sxs-lookup"><span data-stu-id="f31cf-108">Field</span></span> | <span data-ttu-id="f31cf-109">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="f31cf-109">Description of action data</span></span>                                 |
|-------|------------------------------------------------------------|
| <span data-ttu-id="f31cf-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="f31cf-110">\[1\]</span></span> | <span data-ttu-id="f31cf-111">Name der Installationsdateien.</span><span class="sxs-lookup"><span data-stu-id="f31cf-111">Name of install files.</span></span>                                     |
| <span data-ttu-id="f31cf-112">\[6\]</span><span class="sxs-lookup"><span data-stu-id="f31cf-112">\[6\]</span></span> | <span data-ttu-id="f31cf-113">Größe der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="f31cf-113">Size of database.</span></span>                                          |
| <span data-ttu-id="f31cf-114">\[9\]</span><span class="sxs-lookup"><span data-stu-id="f31cf-114">\[9\]</span></span> | <span data-ttu-id="f31cf-115">Bezeichner der administrativen Installation – Punkt Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="f31cf-115">Identifier of administrative installation–point directory.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f31cf-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f31cf-116">Remarks</span></span>

<span data-ttu-id="f31cf-117">Die Aktion installadminpackage aktualisiert auch die Zusammenfassungs Informationen der Datenbank und entfernt alle CAB-Dateien, die sich in Streams befinden, nachdem die Datenbank kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f31cf-117">The InstallAdminPackage action also updates the summary information of the database and removes any cabinet files located in streams after the database is copied.</span></span>

 

 



