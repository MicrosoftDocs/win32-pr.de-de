---
description: Beispiel für Ball Filter
ms.assetid: 80a6db64-ef13-46a2-8f2a-e39095e874b2
title: Beispiel für Ball Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b80301b233f0c1e74933c93fe86a0e1878458e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860473"
---
# <a name="ball-filter-sample"></a>Beispiel für Ball Filter

## <a name="description"></a>BESCHREIBUNG

Der Kugel Filter ist ein Video Quell Filter, der ein Bild eines Sprung-Balls erzeugt. Dieses Beispiel veranschaulicht die Format Aushandlung und die Verwendung der Quell Filter-Basisklassen [**CSource**](csource.md) und [**csourcestream**](csourcestream.md).

Der Code in "f. h" und "f. cpp" verwaltet die Filter Schnittstellen. Diese beiden Dateien enthalten ungefähr den minimalen Code, der für einen Quell Filter erforderlich ist. Die Dateien Ball. h und Ball. cpp enthalten den Code, der die Kugel springt.

Dieser Filter verfügt über ein einzelnes Ausgabepin, das einen Videostream bereitstellt, der eine Kugel im Frame aufspringt. Der Kugel Filter akzeptiert auch Qualitäts Verwaltungsanforderungen des downstreamfilters, die eine einfache Qualitäts Verwaltungs Strategie veranschaulichen. Dieser Filter implementiert die [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) -Schnittstelle zu diesem Zweck.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Dieses Beispiel wird unter folgendem Pfad installiert: \[ *SDK Root* \] \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ Ball.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



