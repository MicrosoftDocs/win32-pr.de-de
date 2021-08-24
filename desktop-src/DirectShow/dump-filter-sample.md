---
description: Beispiel für Dumpfilter
ms.assetid: 2ce52e6c-a02f-4737-822a-87b2cf2d933d
title: Beispiel für Dumpfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5643f0334071b8c238a70ed31eee87de4e93e3637b5403d886d79f2816e39c97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148733"
---
# <a name="dump-filter-sample"></a>Beispiel für Dumpfilter

## <a name="description"></a>Beschreibung

Der Dumpfilter ist ein Rendererfilter, der die empfangenen Medienbeispiele in eine Textdatei schreibt.

In diesem Beispiel wird veranschaulicht, wie die Basisfilterklasse [**CBaseFilter**](cbasefilter.md) und die gerenderte Eingabepinklasse [**CRenderedInputPin verwendet werden.**](crenderedinputpin.md) Außerdem wird veranschaulicht, wie die [**IFileSinkFilter-Schnittstelle implementiert**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) wird. Der Dumpfilter verfügt über einen einzelnen Eingabepin, der jedes empfangene Beispiel direkt in eine Datei schreibt.

## <a name="usage"></a>Verbrauch

Dieser Filter ist ein nützliches Debugtool. Beispielsweise können Sie die Ergebnisse eines Transformationsfilters bit für Bit überprüfen. Sie können ein Diagramm manuell mit GraphEdit erstellen und den Dumpfilter mit der Ausgabe eines Transformationsfilters oder eines anderen Ausgabepins verbinden. Sie können auch einen Teefilter verbinden und den Dumpfilter auf einem Bein des Teefilters und die typische Ausgabe auf einem anderen Bein setzen, um die Ergebnisse in einem Echtzeitszenario zu überwachen.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Um die DirectShow SDK-Beispiele herunterzuladen, installieren Sie die neueste Version des [Windows SDK.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK \] Root* Samples Multimedia \\ \\ \\ DirectShow Filters \\ \\ Dump.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



