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
# <a name="access-to-directdraw-surfaces"></a><span data-ttu-id="37c94-103">Zugriff auf DirectDraw-Oberflächen</span><span class="sxs-lookup"><span data-stu-id="37c94-103">Access to DirectDraw Surfaces</span></span>

<span data-ttu-id="37c94-104">Die Media Sample Objects, die von VMR für upstreamfilter bereitgestellt werden, unterstützen die [**ivmrsurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="37c94-104">The Media Sample objects provided by the VMR to upstream filters support the [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) interface.</span></span> <span data-ttu-id="37c94-105">Rufen Sie zum Abrufen der Schnittstelle QueryInterface für die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle auf, und geben Sie IID \_ ivmrsurface an.</span><span class="sxs-lookup"><span data-stu-id="37c94-105">To obtain the interface, call QueryInterface on the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface and specify IID\_IVMRSurface.</span></span> <span data-ttu-id="37c94-106">Upstreamfilter können dann die ivmrsurface-Methoden verwenden, um auf die von VMR erstellte Oberfläche zuzugreifen und Sie zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="37c94-106">Upstream filters can then use the IVMRSurface methods to access and manipulate the surface that has been created by the VMR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37c94-107">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="37c94-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37c94-108">Verwenden von VMR für DirectShow-Filter Entwickler</span><span class="sxs-lookup"><span data-stu-id="37c94-108">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



