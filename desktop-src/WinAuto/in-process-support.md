---
title: In-Process Unterstützung
description: Die aktuelle Implementierung der dynamischen Anmerkung ist vollständig in Verarbeitung und ermöglicht folglich nur das Kommentieren von Benutzeroberflächen Elementen durch den Prozess, der diese Elemente der Benutzeroberfläche besitzt.
ms.assetid: 3d32c444-47fb-49fe-be18-0330fea77926
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4cf9ed1c17d84ddc824ce5ac6d412f1ee12b8e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309515"
---
# <a name="in-process-support"></a><span data-ttu-id="e555a-103">In-Process Unterstützung</span><span class="sxs-lookup"><span data-stu-id="e555a-103">In-Process Support</span></span>

<span data-ttu-id="e555a-104">Die aktuelle Implementierung der dynamischen Anmerkung ist vollständig in Verarbeitung und ermöglicht folglich nur das Kommentieren von Benutzeroberflächen Elementen durch den Prozess, der diese Elemente der Benutzeroberfläche besitzt.</span><span class="sxs-lookup"><span data-stu-id="e555a-104">The current implementation of Dynamic Annotation is entirely in-process and consequently allows only UI elements to be annotated by the process that owns those UI elements.</span></span> <span data-ttu-id="e555a-105">Es ist nicht möglich, dass ein Prozess die Benutzeroberflächen Elemente eines anderen Prozesses mit Anmerkungen versehen.</span><span class="sxs-lookup"><span data-stu-id="e555a-105">It is not possible for one process to annotate the UI elements of another process.</span></span>

<span data-ttu-id="e555a-106">Beachten Sie, dass dies nur Auswirkungen auf das Festlegen einer Anmerkung hat. Dies beeinträchtigt nicht die Fähigkeit von Clients, auf die Eigenschaften von Benutzeroberflächen Elementen in anderen Prozessen zuzugreifen (kommentiert oder anderweitig).</span><span class="sxs-lookup"><span data-stu-id="e555a-106">Note that this only affects the act of setting an annotation; it does not interfere with the ability of clients to access the properties (annotated or otherwise) of UI elements in other processes.</span></span>

 

 




