---
description: Die folgende Liste enthält die öffentlichen cmspcallmultigraph-Methoden, die vom Thread Pool aufgerufen werden.
ms.assetid: f0a5f621-99c4-40f0-8a0e-0e43792e00a1
title: Vom Thread Pool aufgerufene öffentliche cmspcallmultigraph-Methoden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3878298024164a4c940b96dceb88e0ff005d59ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358486"
---
# <a name="cmspcallmultigraph-public-methods-called-by-thread-pool"></a>Vom Thread Pool aufgerufene öffentliche cmspcallmultigraph-Methoden



| Öffentliche cmspcallmultigraph-Methoden                                   | BESCHREIBUNG                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Dispatchgraphevent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) | Wird aufgerufen, wenn das Filter Diagramm ein Ereignis signalisiert.                                                                                                                                                           |
| [**"Lenker"**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-handlegraphevent)     | Wird von der statischen [**dispatchgraphevent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-dispatchgraphevent) -Methode aufgerufen. Warteschlangen [**processgraphevent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent) auf dem Haupt-MSP-Arbeits Thread. |
| [**Processgraphevent**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallmultigraph-processgraphevent)   | Ermöglicht der MSP-Aufruf Objektinstanz, das Filter Diagramm Ereignis zu behandeln.                                                                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Cmspcallmultigraph**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)
</dt> </dl>

 

 



