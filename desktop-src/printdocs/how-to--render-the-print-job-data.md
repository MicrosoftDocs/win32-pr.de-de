---
description: In diesem Thema wird beschrieben, wie die zu druckenden Programmdaten gerendert werden.
ms.assetid: D1343C53-6F13-49FF-8C7C-25D5A3C31B22
title: 'How To: Rendern von Druckauftragsdaten'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70724cc9dee6b7d3bb0434f08e3db959acfecfc54bc4ebafac5f5a3c6bd4b014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825130"
---
# <a name="how-to-render-print-job-data"></a>How To: Rendern von Druckauftragsdaten

In diesem Thema wird beschrieben, wie die zu druckenden Programmdaten gerendert werden. In diesem Thema wird nicht ausführlich erläutert, wie bestimmte Grafiken oder Textbilder gerendert werden. Stattdessen wird beschrieben, wie die Programmdaten verwaltet und als XPS-Dokument gerendert werden, das mithilfe der [XPS-Druck-API](xps-printing.md)an einen Drucker gesendet wird.

## <a name="overview"></a>Übersicht

Beim Rendern von Druckauftragsdaten für den Druck werden die programmspezifischen Daten wie Text, Bilder und Formatierung verwendet und in ein Format konvertiert, das mit dem Zieldrucker kompatibel ist. Das Programm, das die Daten an den Drucker sendet, muss sie in dem vom Druckertreiber benötigten Format senden.

Verwenden Sie [die XPS-Druck-API,](xps-printing.md) um die Daten an den Drucker zu senden, und die Daten müssen als XPS-Dokument formatiert sein. Um den XPS-Dokumentinhalt zu erzeugen, den die XPS-Druck-API benötigt, verwendet das Beispielprogramm die [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85)).

Wenn der Programminhalt in einem Format vor sich geht, das nicht mit einem Drucker kompatibel ist, muss er gerendert werden, bevor er an den Drucker gesendet wird. Wenn das Programm die [XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85)) verwendet, um seinen Programminhalt zu verwalten, hat der Programminhalt ein Format, das direkt an die [XPS-Druck-API](xps-printing.md) gesendet werden kann und kein zusätzliches Rendering erfordert, bevor Sie ihn an den Drucker senden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[XPS-Dokument-API](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[XPS-Druck-API](xps-printing.md)
</dt> </dl>

 

 
