---
description: Dumpfilterbeispiel
ms.assetid: 2ce52e6c-a02f-4737-822a-87b2cf2d933d
title: Dumpfilterbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd64d1f16b0b504743890543b617a24df6bbaab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522416"
---
# <a name="dump-filter-sample"></a>Dumpfilterbeispiel

## <a name="description"></a>BESCHREIBUNG

Der dumpfilter ist ein rendererfilter, der die empfangenen Medien Beispiele in eine Textdatei schreibt.

In diesem Beispiel wird veranschaulicht, wie die Basis Filterklasse [**cbasefilter**](cbasefilter.md) und die gerenderte Eingabe-PIN-Klasse [**crenderedinputpin**](crenderedinputpin.md)verwendet werden. Außerdem wird veranschaulicht, wie die [**ifilesink Filter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) -Schnittstelle implementiert wird. Der dumpfilter verfügt über eine einzelne Eingabe-PIN, die jedes empfangene Beispiel direkt in eine Datei schreibt.

## <a name="usage"></a>Verbrauch

Dieser Filter ist ein nützliches Debugtool. Beispielsweise können Sie die Ergebnisse eines Transformations Filters mit Bit und Bit überprüfen. Sie können ein Diagramm manuell erstellen, indem Sie GraphEdit verwenden und den dumpfilter mit der Ausgabe eines Transformations Filters oder einer anderen Ausgabepin verbinden. Sie können auch einen Tee-Filter verbinden und den dumpfilter auf einem Teil des Tee-Filters und die typische Ausgabe in einem anderen Abschnitt platzieren, um die Ergebnisse in einem echt Zeit Szenario zu überwachen.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK \] root* \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ Dump.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



