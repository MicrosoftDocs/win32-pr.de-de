---
description: Eingebettete Transformationen werden in der MSI-Datei des Pakets gespeichert. Dadurch wird Benutzern gewährleistet, dass die Transformation immer verfügbar ist, wenn das Installationspaket verfügbar ist. Alternativ können Transformationen als eigenständige MST-Dateien für Benutzer bereitgestellt werden.
ms.assetid: f7b265df-4b34-44ea-85ab-8dbca4797517
title: Eingebettete Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301e7f188da1a46411636ef90b7e6ae327a06c22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042390"
---
# <a name="embedded-transforms"></a><span data-ttu-id="3f666-105">Eingebettete Transformationen</span><span class="sxs-lookup"><span data-stu-id="3f666-105">Embedded Transforms</span></span>

<span data-ttu-id="3f666-106">Eingebettete Transformationen werden in der MSI-Datei des Pakets gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3f666-106">Embedded transforms are stored inside the .msi file of the package.</span></span> <span data-ttu-id="3f666-107">Dadurch wird Benutzern gewährleistet, dass die Transformation immer verfügbar ist, wenn das Installationspaket verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3f666-107">This guarantees to users that the transform is always available when the installation package is available.</span></span> <span data-ttu-id="3f666-108">Alternativ können Transformationen als eigenständige MST-Dateien für Benutzer bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3f666-108">Alternatively, transforms may be provided to users as standalone .mst files.</span></span>

<span data-ttu-id="3f666-109">Um der Liste Transformationen eine eingebettete Transformation hinzuzufügen, fügen Sie einen Doppelpunkt (:) Präfix des Datei namens.</span><span class="sxs-lookup"><span data-stu-id="3f666-109">To add an embedded transform to the transforms list, add a colon (:) prefix to the file name.</span></span> <span data-ttu-id="3f666-110">Da das Installationsprogramm die Transformation immer aus dem Speicher in der MSI-Datei abrufen kann, werden eingebettete Transformationen nicht auf dem Computer des Benutzers zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="3f666-110">Because the installer can always obtain the transform from storage in the .msi file, embedded transforms are not cached on the user's computer.</span></span> <span data-ttu-id="3f666-111">Eingebettete Transformationen können in Kombination mit [gesicherten Transformationen](secured-transforms.md) oder [ungesicherten Transformationen](unsecured-transforms.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f666-111">Embedded transforms may be used in combination with [secured transforms](secured-transforms.md) or [unsecured transforms](unsecured-transforms.md).</span></span> <span data-ttu-id="3f666-112">Weitere Informationen finden Sie unter [Anwenden von Transformationen](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="3f666-112">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



