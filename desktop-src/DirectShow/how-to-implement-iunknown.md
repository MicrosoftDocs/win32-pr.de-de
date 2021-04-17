---
description: Implementieren von IUnknown
ms.assetid: 4e363ccb-9725-4be6-bb31-283bf1d658f5
title: Implementieren von IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27c12e25d56adab1841a375ac6c1ce0857a73b5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520499"
---
# <a name="how-to-implement-iunknown"></a>Implementieren von IUnknown

Microsoft DirectShow basiert auf dem Component Object Model (com). Wenn Sie einen eigenen Filter schreiben, müssen Sie ihn als COM-Objekt implementieren. Die DirectShow-Basisklassen stellen ein Framework bereit, aus dem dies zu tun ist. Die Verwendung der Basisklassen ist nicht erforderlich, kann jedoch den Entwicklungsprozess vereinfachen. In diesem Artikel werden einige der internen Details von COM-Objekten und deren Implementierung in den DirectShow-Basisklassen beschrieben.

In diesem Artikel wird davon ausgegangen, dass Sie wissen, wie Sie com-Client Anwendungen programmieren können – mit anderen Worten, dass Sie die Methoden in **IUnknown**– verstehen, aber keine vorherige Erfahrung bei der Entwicklung von COM-Objekten annimmt. DirectShow behandelt viele der Details der Entwicklung eines COM-Objekts. Wenn Sie mit der Entwicklung von COM-Objekten vertraut sind, sollten Sie den Abschnitt [mit cunknown](using-cunknown.md)lesen, in dem die [**cunknown**](cunknown.md) -Basisklasse beschrieben wird.

COM ist eine Spezifikation und keine Implementierung. Es definiert die Regeln, denen eine Komponente folgen muss. Diese Regeln werden dem Entwickler überlassen. In DirectShow werden alle Objekte von einem Satz von C++-Basisklassen abgeleitet. Die Basisklassenkonstruktoren und-Methoden führen die meisten com-Buchhaltungsaufgaben aus, z. b. die Beibehaltung einer konsistenten Verweis Anzahl. Durch Ableiten des Filters von einer Basisklasse erben Sie die Funktionalität der-Klasse. Um Basisklassen effektiv zu verwenden, benötigen Sie ein allgemeines Verständnis der Implementierung der com-Spezifikation.

Dieser Artikel enthält die folgenden Themen:

-   [Funktionsweise von IUnknown](how-iunknown-works.md)
-   [Verwenden von cunknown](using-cunknown.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow und com](directshow-and-com.md)
</dt> </dl>

 

 



