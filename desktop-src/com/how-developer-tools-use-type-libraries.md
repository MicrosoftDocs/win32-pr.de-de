---
title: Verwendung von Typbibliotheken in Entwicklertools
description: Verwendung von Typbibliotheken in Entwicklertools
ms.assetid: 260aa694-1055-4a43-93aa-69a9d7359881
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18e829459176d96beab3fd818b7bafe3cddfb7969ff46531d26709ef6391ecc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993074"
---
# <a name="how-developer-tools-use-type-libraries"></a>Verwendung von Typbibliotheken in Entwicklertools

Das folgende Diagramm veranschaulicht, wie die verschiedenen Entwicklungstools mit der Typbibliothek eines COM-Objekts interagieren. Jede Typbibliothek macht programmgesteuerte Standardschnittstellen verfügbar, die Tools aufrufen können, um Informationen zu den in dieser Typbibliothek beschriebenen Elementen zu erhalten. In diesem Diagramm steht GUID für global eindeutiger Bezeichner und RPC für Remoteprozeduraufrufe.

![Diagramm, das zeigt, wie Entwicklungstool mit der Typbibliothek eines C O M-Objekts interagieren.](images/09983c96-3f01-4ad5-8d3e-12b8ed28c35d.png)

Im obigen Diagramm generieren die C++-Konvertierungstools wie der MIDL-Compiler und die vom Microsoft Visual C++-Entwicklungssystem bereitgestellten Assistenten Header- und Stubdateien. Sie können diese Dateien ihrem Projekt hinzufügen, um das von der Typbibliothek beschriebene COM-Objekt zu verwenden.

Auf ähnliche Weise generieren die Entwicklertools in Java Java-Klassen- und Quelldateien, die Sie dann in Ihre Anwendung importieren können.

In Visual Basic ist das Szenario etwas einfacher. Sie müssen keine zusätzlichen Dateien generieren. Die Visual Basic-Umgebung stellt Dialogfelder mit den com-Objekten zur Verfügung, die derzeit auf Ihrem Computer installiert sind. Sie wählen die Komponente aus, die Sie aus Ihrer Anwendung aufrufen möchten, und werden dem Projekt entweder als Komponente oder als Verweis hinzugefügt.

Der OLE-COM-Viewer liest eine Typbibliothek, generiert eine temporäre IDL-Datei basierend auf der Typbibliothek und zeigt sie Benutzern an. Der OLE-COM-Viewer zeigt auch die C++-Syntax für die COM-Elemente an, die in der Typbibliothek aufgeführt sind.

Weitere Informationen zu Typbibliotheken finden Sie unter [Typbibliotheken und Object Description Language](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).

 

 