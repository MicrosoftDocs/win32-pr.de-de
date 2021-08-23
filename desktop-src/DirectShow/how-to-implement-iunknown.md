---
description: Implementieren von IUnknown
ms.assetid: 4e363ccb-9725-4be6-bb31-283bf1d658f5
title: Implementieren von IUnknown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f905ac7e31be955a7b24f8504fc6b52ca8031e4a7deef86ef8bccd537b5ca6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748700"
---
# <a name="how-to-implement-iunknown"></a>Implementieren von IUnknown

Microsoft DirectShow basiert auf dem Component Object Model (COM). Wenn Sie einen eigenen Filter schreiben, müssen Sie ihn als COM-Objekt implementieren. Die DirectShow-Basisklassen stellen ein Framework für dies zur Verfügung. Die Verwendung der Basisklassen ist nicht erforderlich, kann aber den Entwicklungsprozess vereinfachen. In diesem Artikel werden einige der internen Details von COM-Objekten und deren Implementierung in den DirectShow-Basisklassen beschrieben.

In diesem Artikel wird davon ausgegangen, dass Sie wissen, wie SIE COM-Clientanwendungen programmieren , d.h. dass Sie die Methoden in **IUnknown** verstehen, aber keine erfahrung mit der Entwicklung von COM-Objekten. DirectShow verarbeitet viele der Details der Entwicklung eines COM-Objekts. Wenn Sie Erfahrung mit der Entwicklung von COM-Objekten haben, sollten Sie den Abschnitt Verwenden von [CUnknown](using-cunknown.md)lesen, in dem die [**CUnknown-Basisklasse**](cunknown.md) beschrieben wird.

COM ist eine Spezifikation, keine Implementierung. Sie definiert die Regeln, die eine Komponente befolgen muss. Die Umsetzung dieser Regeln bleibt dem Entwickler übrig. In DirectShow werden alle Objekte von einem Satz von C++-Basisklassen ableiten. Die Basisklassenkonstruktoren und -methoden führen den Großteil der COM-"Buchhaltung" aus, z. B. die Beibehaltung einer konsistenten Verweisanzahl. Indem Sie ihren Filter von einer Basisklasse ableiten, erben Sie die Funktionalität der -Klasse. Um Basisklassen effektiv zu verwenden, benötigen Sie ein allgemeines Verständnis der Implementierung der COM-Spezifikation.

Dieser Artikel enthält die folgenden Themen.

-   [Funktionsweise von IUnknown](how-iunknown-works.md)
-   [Verwenden von CUnknown](using-cunknown.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow und COM](directshow-and-com.md)
</dt> </dl>

 

 



