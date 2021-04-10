---
description: 'Es gibt zwei Typen von Links, die im NTFS-Dateisystem unterstützt werden: feste Links und Verbindungen.'
ms.assetid: 548acfe5-c9e1-4227-ba20-674e071f121f
title: Verknüpfen von Dateien und Verzeichnissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70bcb905b73f7635ba5bdc4afcc44280023c7a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960652"
---
# <a name="file-and-directory-linking"></a><span data-ttu-id="a9a90-103">Verknüpfen von Dateien und Verzeichnissen</span><span class="sxs-lookup"><span data-stu-id="a9a90-103">File and Directory Linking</span></span>

<span data-ttu-id="a9a90-104">Das NTFS-Dateisystem bietet die Möglichkeit, eine System Darstellung einer Datei oder eines Verzeichnisses an einem Speicherort in der Verzeichnisstruktur zu erstellen, der sich von dem Datei-oder Verzeichnis Objekt unterscheidet, mit dem verknüpft wird.</span><span class="sxs-lookup"><span data-stu-id="a9a90-104">The NTFS file system provides the ability to create a system representation of a file or directory in a location in the directory structure that is different from the file or directory object that is being linked to.</span></span> <span data-ttu-id="a9a90-105">Dieser Vorgang wird als Verknüpfung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a9a90-105">This process is called linking.</span></span> <span data-ttu-id="a9a90-106">Es gibt zwei Typen von Links, die im NTFS-Dateisystem unterstützt werden: feste [Links und](hard-links-and-junctions.md)Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="a9a90-106">There are two types of links supported in the NTFS file system: [hard links and junctions](hard-links-and-junctions.md).</span></span>

<span data-ttu-id="a9a90-107">Das NTFS-Dateisystem bietet auch den [Überwachungsdienst für verteilte Links](distributed-link-tracking-and-object-identifiers.md), der die Verknüpfungen automatisch nachverfolgt, wenn Sie verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="a9a90-107">The NTFS file system also provides the [distributed link tracking service](distributed-link-tracking-and-object-identifiers.md), which automatically tracks links as they are moved.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a9a90-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a9a90-108">In this section</span></span>



| <span data-ttu-id="a9a90-109">Thema</span><span class="sxs-lookup"><span data-stu-id="a9a90-109">Topic</span></span>                                                                                                               | <span data-ttu-id="a9a90-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9a90-110">Description</span></span>                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9a90-111">Feste Links und Verbindungen</span><span class="sxs-lookup"><span data-stu-id="a9a90-111">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)<br/>                                                 | <span data-ttu-id="a9a90-112">Beschreibt feste Links und Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="a9a90-112">Describes hard links and junctions.</span></span><br/>                                                                          |
| [<span data-ttu-id="a9a90-113">Nachverfolgung verteilter Links und Objekt Bezeichner</span><span class="sxs-lookup"><span data-stu-id="a9a90-113">Distributed Link Tracking and Object Identifiers</span></span>](distributed-link-tracking-and-object-identifiers.md)<br/> | <span data-ttu-id="a9a90-114">Der **Dienst für die verteilte Link Überwachung** ermöglicht Client Anwendungen das Nachverfolgen von Verknüpfungs Quellen, die verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="a9a90-114">The **distributed link tracking service** enables client applications to track link sources that have moved.</span></span><br/> |



 

 

 




