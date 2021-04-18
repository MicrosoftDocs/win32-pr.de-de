---
description: Csourceposition ist eine abstrakte Klasse zum Implementieren der imediaposition-Schnittstelle für einen Quell Filter.
ms.assetid: 838d2efd-6870-4412-98e2-fb2628e14bf3
title: Csourceposition-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourcePosition
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0b88289381641edcef5922557862729acbb81f54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341092"
---
# <a name="csourceposition-class"></a><span data-ttu-id="ef698-103">Csourceposition-Klasse</span><span class="sxs-lookup"><span data-stu-id="ef698-103">CSourcePosition class</span></span>

<span data-ttu-id="ef698-104">`CSourcePosition` ist eine abstrakte Klasse zum Implementieren der [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) -Schnittstelle für einen Quell Filter.</span><span class="sxs-lookup"><span data-stu-id="ef698-104">`CSourcePosition` is an abstract class for implementing the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface on a source filter.</span></span>

<span data-ttu-id="ef698-105">Diese Klasse ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="ef698-105">This class is obsolete.</span></span> <span data-ttu-id="ef698-106">Wenn der Quell Filter suchbar ist, sollte er anstelle von **imediaposition** die [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="ef698-106">If your source filter is seekable, it should expose the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface instead of **IMediaPosition**.</span></span> <span data-ttu-id="ef698-107">Hierfür können Sie die [**csourceseeking**](csourceseeking.md) -Basisklasse verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef698-107">You can use the [**CSourceSeeking**](csourceseeking.md) base class for this purpose.</span></span>

 

 



