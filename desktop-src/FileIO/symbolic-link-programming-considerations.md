---
description: Programmier Überlegungen für die Arbeit mit symbolischen Verknüpfungen.
ms.assetid: 8966ac3e-a92b-4d68-b40b-e32a4173f869
title: Überlegungen zur Programmierung (lokale Dateisysteme)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a5d63c231c88da95efc0e5078506bf9fc0d6d9a
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "106370351"
---
# <a name="programming-considerations-local-file-systems"></a><span data-ttu-id="c1518-103">Überlegungen zur Programmierung (lokale Dateisysteme)</span><span class="sxs-lookup"><span data-stu-id="c1518-103">Programming Considerations (Local File Systems)</span></span>

<span data-ttu-id="c1518-104">Beachten Sie beim Arbeiten mit symbolischen Verknüpfungen die folgenden Programmier Überlegungen:</span><span class="sxs-lookup"><span data-stu-id="c1518-104">Keep the following programming considerations in mind when working with symbolic links:</span></span>

-   <span data-ttu-id="c1518-105">Symbolische Verknüpfungen können auf ein nicht vorhandenes Ziel verweisen.</span><span class="sxs-lookup"><span data-stu-id="c1518-105">Symbolic links can point to a non-existent target.</span></span>
-   <span data-ttu-id="c1518-106">Beim Erstellen eines symbolischen Links überprüft das Betriebssystem nicht, ob das Ziel vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c1518-106">When creating a symbolic link, the operating system does not check to see if the target exists.</span></span>
-   <span data-ttu-id="c1518-107">Wenn eine Anwendung versucht, ein nicht vorhandenes Ziel zu öffnen, wird die **Fehler \_ Datei \_ nicht \_ gefunden** .</span><span class="sxs-lookup"><span data-stu-id="c1518-107">If an application tries to open a non-existent target, **ERROR\_FILE\_NOT\_FOUND** is returned.</span></span>
-   <span data-ttu-id="c1518-108">Symbolische Verknüpfungen sind Analyse Punkte.</span><span class="sxs-lookup"><span data-stu-id="c1518-108">Symbolic links are reparse points.</span></span> <span data-ttu-id="c1518-109">Weitere Informationen finden Sie unter [bestimmen, ob ein Verzeichnis ein](determining-whether-a-directory-is-a-volume-mount-point.md)bereitgestellter Ordner ist.</span><span class="sxs-lookup"><span data-stu-id="c1518-109">For more information, see [Determining Whether a Directory Is a Mounted Folder](determining-whether-a-directory-is-a-volume-mount-point.md).</span></span>
-   <span data-ttu-id="c1518-110">Es sind maximal 63 Analyse Punkte (und daher symbolische Verknüpfungen) in einem bestimmten Pfad zulässig.</span><span class="sxs-lookup"><span data-stu-id="c1518-110">There is a maximum of 63 reparse points (and therefore symbolic links) allowed in a particular path.</span></span>

    <span data-ttu-id="c1518-111">**Windows Server 2003 und Windows XP:** Es gibt ein Limit von 31 Analyse Punkten für einen beliebigen Pfad.</span><span class="sxs-lookup"><span data-stu-id="c1518-111">**Windows Server 2003 and Windows XP:** There is a limit of 31 reparse points on any given path.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1518-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c1518-112">Related topics</span></span>

<dl> <span data-ttu-id="c1518-113"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c1518-113"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="c1518-114">Feste Links und Verbindungen</span><span class="sxs-lookup"><span data-stu-id="c1518-114">Hard Links and Junctions</span></span>](hard-links-and-junctions.md)
</dt> </dl>

 

 



