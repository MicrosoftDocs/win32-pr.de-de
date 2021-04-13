---
title: Multithread-Probleme
description: Multithread-Probleme
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0910e1602d00d3429bb9e4c7a1667bf8113cd659
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388821"
---
# <a name="multi-threaded-issues"></a>Multithread-Probleme

OLE bietet Unterstützung für Multithreadanwendungen und ermöglicht Anwendungen das Erstellen von OLE-aufrufen aus mehreren Threads. Diese Multithreadunterstützung wird als Apartment Modell bezeichnet. es ist wichtig, dass alle OLE-Komponenten, die mehrere Threads verwenden, diesem Modell folgen. Das Apartment Modell erfordert, dass Schnittstellen Zeiger gemarshallt werden (mithilfe von " [**comarshalinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)" und " [**framarshalinterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)"), wenn Sie zwischen Threads übermittelt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Prozesse, Threads und Apartments](processes--threads--and-apartments.md)
</dt> </dl>

 

 




