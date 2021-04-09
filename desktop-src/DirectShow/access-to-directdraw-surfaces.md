---
description: Zugriff auf DirectDraw-Oberflächen
ms.assetid: 21002c9f-8b8b-49f3-9ea3-3703780e3412
title: Zugriff auf DirectDraw-Oberflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac1acdd122fa7d21fd49868c45f065f59b06ad8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860480"
---
# <a name="access-to-directdraw-surfaces"></a>Zugriff auf DirectDraw-Oberflächen

Die Media Sample Objects, die von VMR für upstreamfilter bereitgestellt werden, unterstützen die [**ivmrsurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) -Schnittstelle. Rufen Sie zum Abrufen der Schnittstelle QueryInterface für die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle auf, und geben Sie IID \_ ivmrsurface an. Upstreamfilter können dann die ivmrsurface-Methoden verwenden, um auf die von VMR erstellte Oberfläche zuzugreifen und Sie zu bearbeiten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von VMR für DirectShow-Filter Entwickler](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



