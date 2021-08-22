---
description: Die Tablet PC-Plattform generiert mehrere Persistenzformate, die als Bausteine für die zuvor aufgeführten Formate nützlich sind. Die folgenden Formate werden alle mithilfe der Load- und Save-Methoden des Ink-Objekts generiert und verwendet.
ms.assetid: 76d42a3d-22f5-47f9-89e8-7c5c098ac62e
title: Bausteine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dbf34cc0159bdf2efe9b68255292a8b644ab10e684f44c11fa60d484bd45516
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714290"
---
# <a name="building-blocks"></a>Bausteine

Die Tablet PC-Plattform generiert mehrere Persistenzformate, die als Bausteine für die zuvor aufgeführten Formate nützlich sind. Die folgenden Formate werden alle mithilfe der [**Load-**](/previous-versions/ms569609(v=vs.100)) und [**Save-Methoden**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) des [**Ink-Objekts**](/previous-versions/ms583670(v=vs.100)) generiert und verwendet.

-   Serialisiertes Ink-Format (ISF): serialisiertes Freihandformat (ISF) ist die kompakteste persistente Darstellung von Ink. Sie können ISF in ein binäres Dokumentformat einbetten oder direkt in die Zwischenablage verschieben. In ISF gespeicherte Ink-Dateien sollten das Standardkoordinatensystem HIMETRIC verwenden, wobei die vertikale Achse umgekehrt ist.
-   Base64-codierte ISF: Sie können base64-codierte ISF verwenden, um Freihanddaten direkt in eine Extensible Markup Language -Datei (XML) oder HTML-Datei zu codieren.
-   Fortified Graphics Interchange Format (GIF): Fortified GIF ist eine GIF-Datei, die ISF als in die Datei eingebettete Metadaten enthält. Als gefestigtes GIF generierte Tusche können in Anwendungen angezeigt werden, die keine Ink-Daten erkennen, und alle Ink-Daten werden beibehalten, wenn die Ink-Datei zu einer Anwendung zurückkehrt, die Ink erkennt. Dieses Format eignet sich ideal zum Übertragen von Ink-Inhalten innerhalb einer HTML-Datei. Die Freihand ist für jede Anwendung verfügbar, unabhängig davon, ob die Anwendung Freihanderkennungen erkennt.
-   Base-64-codiertes gif-Format: Dieses Format wird für Entwickler bereitgestellt, die Freihand direkt in eine XML- oder HTML-Datei codieren und die Datei dann zu einem späteren Zeitpunkt in ein Bild konvertieren möchten. Sie können dies verwenden, wenn eine generierte XML-Datei alle Freihandinformationen enthalten und als Möglichkeit zum Generieren von HTML mithilfe von Extensible Stylesheet Language Transformationen (XSLT) verwendet werden soll.
    > [!Note]  
    > Die LZW-Komprimierungs- und Dekomprimierungstechnologie wird von der US-Patentnr. 4.558.302 und die zugehörigen und fremden Gegenstücke (zusammen das LZW-Patent) im Besitz der Unisys Corporation. Microsoft Corporation hat von Unisys unter dem LZW-Patent eine Lizenz für die Verwendung des GIF und der LZW-Technologie in bestimmten Microsoft-Produkten erhalten. Diese Lizenz gilt jedoch nicht für Drittanbieterentwickler, die Microsoft-Entwicklungsprodukte wie Microsoft-Toolkit- und Sprachentwicklungsprodukte verwenden, um GIF-Lese-/Schreibzugriff oder andere LZW-Funktionen in ihren eigenen Produkten bereitzustellen. Drittanbieterentwickler müssen selbst bestimmen, ob sie eine Lizenz von Unisys für ihre Produkte benötigen.

     

Eine Anwendung kann eines dieser persistenten Formate generieren, indem sie [microsoft.Ink.Stroke.HitTest](/previous-versions/ms828460(v=msdn.10)) oder die [Microsoft.Ink.Ink.HitTest-Methode](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) verwendet, um eine Strichsammlung zu generieren, und eine der folgenden Methoden:

-   Hinzufügen dieser Striche zu einem neuen [**Ink-Objekt**](/previous-versions/ms583670(v=vs.100)) mithilfe der [AddStrokesAtRectangle-Methode.](/previous-versions/ms569548(v=vs.100))
-   Generieren eines neuen [**Ink-Objekts**](/previous-versions/ms583670(v=vs.100)) mithilfe der [ExtractStrokes-Methode.](/previous-versions/dotnet/netframework-3.5/ms571326(v=vs.90))

Der erste übersetzt das Auswahlrechteck in den Ursprung, das zweite nicht. Die Anwendung verwendet dann die [**Save-Methode**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) des [**Ink-Objekts.**](/previous-versions/ms583670(v=vs.100))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[sInk- und tInk-Objekte](sink-and-tink-objects.md)
</dt> </dl>

 

 
