---
title: Multithread-Probleme
description: Multithread-Probleme
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ffd1dc3f73c33ca30ebee0072f1c5059c73f25e9e2318d384cd0c3d0dc7bc94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117918530"
---
# <a name="multi-threaded-issues"></a>Multithread-Probleme

OLE bietet Unterstützung für Multithreadanwendungen, sodass Anwendungen OLE-Aufrufe aus mehreren Threads vornehmen können. Diese Multithreadunterstützung wird als Apartmentmodell bezeichnet. Es ist wichtig, dass alle OLE-Komponenten, die mehrere Threads verwenden, diesem Modell folgen. Das Apartmentmodell erfordert, dass Schnittstellenzeiger gemarshallt werden (mit [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)und [**CoUnmarshalInterface),**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)wenn sie zwischen Threads übergeben werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Prozesse, Threads und Apartment](processes--threads--and-apartments.md)
</dt> </dl>

 

 




