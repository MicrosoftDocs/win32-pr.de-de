---
description: In diesem Thema wird beschrieben, wie die zu druckenden Programm Daten dargestellt werden.
ms.assetid: D1343C53-6F13-49FF-8C7C-25D5A3C31B22
title: 'Gewusst wie: Rendering von Druckauftrags Daten'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2d9f8cbf68394fd56ebcf31cfb37ee8f337f90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868532"
---
# <a name="how-to-render-print-job-data"></a>Gewusst wie: Rendering von Druckauftrags Daten

In diesem Thema wird beschrieben, wie die zu druckenden Programm Daten dargestellt werden. In diesem Thema wird nicht ausführlich erläutert, wie bestimmte Grafiken oder Text Bilder dargestellt werden. Stattdessen wird beschrieben, wie die Programm Daten verwaltet und als XPS-Dokument dargestellt werden, das über die [XPS-Druck-API](xps-printing.md)an einen Drucker gesendet wird.

## <a name="overview"></a>Übersicht

Das Rendern von Druckauftrags Daten für den Druck umfasst das übernehmen der Programm spezifischen Daten, z. b. Text, Bilder und Formatierung, und das Einfügen in ein Format, das mit dem Ziel Drucker kompatibel ist. Das Programm, das die Daten an den Drucker sendet, muss es in dem Format senden, das der Druckertreiber benötigt.

Verwenden Sie die [XPS-Druck-API](xps-printing.md) , um die Daten an den Drucker zu senden, und Sie müssen die Daten als XPS-Dokument formatieren. Zum Entwickeln des XPS-Dokument Inhalts, den die XPS-Druck-API benötigt, verwendet das Beispielprogramm die [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85)).

Wenn der Programm Inhalt in einem Format vorliegt, das mit einem Drucker nicht kompatibel ist, muss es vor dem Senden an den Drucker gerendert werden. Wenn das Programm den Programm Inhalt mithilfe der [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85)) verwaltet, wird der Programm Inhalt in einem Format angezeigt, das direkt an die [XPS-Druck-API](xps-printing.md) gesendet werden kann und kein zusätzliches Rendering erfordert, bevor es an den Drucker gesendet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[XPS-Druck-API](xps-printing.md)
</dt> </dl>

 

 
