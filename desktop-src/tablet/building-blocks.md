---
description: Es gibt mehrere Persistenzformate, die von der Tablet PC-Plattform generiert werden, die als Bausteine für die zuvor aufgeführten Formate nützlich sind. Die folgenden Formate werden alle generiert und verwendet, indem die Load-und Save-Methoden des Ink-Objekts verwendet werden.
ms.assetid: 76d42a3d-22f5-47f9-89e8-7c5c098ac62e
title: Bausteine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32e6121ddfaabfc860239019ce62df65bdc36c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346041"
---
# <a name="building-blocks"></a>Bausteine

Es gibt mehrere Persistenzformate, die von der Tablet PC-Plattform generiert werden, die als Bausteine für die zuvor aufgeführten Formate nützlich sind. Die folgenden Formate werden alle generiert und verwendet, indem die [**Load**](/previous-versions/ms569609(v=vs.100)) -und [**Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) -Methoden des [**Ink**](/previous-versions/ms583670(v=vs.100)) -Objekts verwendet werden.

-   Ink-serialisiertes Format (ISF): das frei Hand Format (Ink serialisiert Format, ISF) ist die kompakteste permanente Darstellung von frei Hand Eingaben. Sie können ISF in ein binäres Dokumentformat einbetten oder es direkt in die Zwischenablage verschieben. In ISF gespeicherte frei Hand Eingaben sollten das Standard Koordinatensystem verwenden, bei dem es sich um eine himetrik handelt und die vertikale Achse invertiert ist.
-   Base-64-codierte ISF: Sie können mit Base-64-codiertem ISF-Code direkt in eine Extensible Markup Language (XML)-oder HTML-Datei codieren.
-   Befestigte Graphics Interchange Format (GIF): das befestigte GIF ist eine GIF-Datei, die ISF als in die Datei eingebettete Metadaten enthält. Frei Hand Eingaben, die als ein befestigtes GIF generiert werden, können in Anwendungen angezeigt werden, die keine frei Hand Eingaben erkennen. alle frei Hand Daten werden beibehalten, wenn die frei Hand Eingaben an eine Anwendung zurückgegeben werden, die Dieses Format eignet sich ideal zum Transportieren von frei Hand Inhalten innerhalb einer HTML-Datei. Die frei Hand Eingaben sind für jede Anwendung verfügbar, unabhängig davon, ob die Anwendung frei Hand Eingaben erkennt.
-   Base-64-codiertes geschütztes GIF: dieses Format wird für Entwickler bereitgestellt, die frei Hand Eingaben direkt in eine XML-oder HTML-Datei codieren möchten, und die Datei dann zu einem späteren Zeitpunkt in ein Bild konvertieren. Sie können diese Option verwenden, wenn eine XML-Datei, die generiert wird, alle frei Hand Informationen enthalten soll und als Methode zum Generieren von HTML mithilfe von Extensible Stylesheet Language Transformationen (XSLT) verwendet werden soll.
    > [!Note]  
    > Die LZW-Komprimierungs-und-Komprimierungs Technologie wird angeblich von US-Patent Nr. abgedeckt. 4.558.302 und seine zugehörigen und ausländischen Gegenstücke (kollektiv die LZW-Patente) im Besitz der Unisys Corporation. Die Microsoft Corporation hat eine Lizenz von Unisys unter den LZW-Patenten erworben, um GIF und die LZW-Technologie in bestimmten Microsoft-Produkten zu verwenden. Diese Lizenz gilt jedoch nicht für Entwickler von Drittanbietern, die Microsoft-Entwicklungsprodukte wie Microsoft Toolkit und sprach Entwicklungsprodukte verwenden, um GIF-Lese-/Schreibzugriff oder andere LZW-Funktionen in ihren eigenen Produkten bereitzustellen. Entwickler von Drittanbietern müssen selbst bestimmen, ob Sie eine Lizenz von Unisys für Ihre Produkte benötigen.

     

Eine Anwendung kann eines dieser persistenten Formate mithilfe der [Microsoft. Ink. Stroke. HitTest](/previous-versions/ms828460(v=msdn.10)) -Methode oder der [Microsoft. Ink. Ink. HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) -Methode generieren, um eine Striche-Auflistung zu generieren, und entweder:

-   Hinzufügen dieser Striche zu einem neuen [**Ink**](/previous-versions/ms583670(v=vs.100)) -Objekt mithilfe der [addstrokesatrechteck](/previous-versions/ms569548(v=vs.100)) -Methode.
-   Erstellen eines neuen [**Ink**](/previous-versions/ms583670(v=vs.100)) -Objekts mithilfe der [ExtractStrokes](/previous-versions/dotnet/netframework-3.5/ms571326(v=vs.90)) -Methode.

Der erste übersetzt das Auswahl Rechteck in den Ursprung, während das zweite nicht. Die Anwendung verwendet dann die [**Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) -Methode des [**Ink**](/previous-versions/ms583670(v=vs.100)) -Objekts.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[sInk-und Tink-Objekte](sink-and-tink-objects.md)
</dt> </dl>

 

 
