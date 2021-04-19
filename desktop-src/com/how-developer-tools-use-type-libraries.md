---
title: Verwendung von Typbibliotheken in Entwicklertools
description: Verwendung von Typbibliotheken in Entwicklertools
ms.assetid: 260aa694-1055-4a43-93aa-69a9d7359881
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cc0f5249075aa861a1301466f86a0f769b8bf3
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "106349751"
---
# <a name="how-developer-tools-use-type-libraries"></a>Verwendung von Typbibliotheken in Entwicklertools

Im folgenden Diagramm wird veranschaulicht, wie die verschiedenen Entwicklungs Tools mit der Typbibliothek eines COM-Objekts interagieren. Jede Typbibliothek stellt standardmäßige programmgesteuerte Schnittstellen zur Verfügung, die von Tools aufgerufen werden können, um Informationen zu den in dieser Typbibliothek beschriebenen Elementen abzurufen. In diesem Diagramm steht GUID für Globally Unique Identifier und RPC für Remote Prozedur Aufrufe.

![Diagramm, das zeigt, wie das Entwicklungs Objekt mit der Typbibliothek eines C O M-Objekts interagiert.](images/09983c96-3f01-4ad5-8d3e-12b8ed28c35d.png)

Im vorangehenden Diagramm generieren die C++-Konvertierungs Tools, wie z. b. der mittlerer l-Compiler und die vom Microsoft Visual C++ Entwicklungssystem bereitgestellten Assistenten, Header-und Stubdateien. Sie können diese Dateien dem Projekt hinzufügen, um das COM-Objekt zu verwenden, das von der Typbibliothek beschrieben wird.

Ebenso generieren die Entwicklertools in Java Java-Klassen-und Quelldateien, die Sie dann in Ihre Anwendung importieren können.

In Visual Basic ist das Szenario etwas einfacher. Sie müssen keine zusätzlichen Dateien generieren. Die Visual Basic Umgebung enthält Dialogfelder, in denen die aktuell auf dem Computer installierten COM-Objekte aufgelistet sind. Sie wählen die Komponente aus, die Sie aus der Anwendung abrufen möchten, und Sie wird dem Projekt hinzugefügt, entweder als Komponente oder als Verweis.

Der OLE-com-Viewer liest eine Typbibliothek, generiert eine temporäre IDL-Datei auf Grundlage der Typbibliothek und zeigt Sie Benutzern an. Der OLE-com-Viewer zeigt auch die C++-Syntax für die in der Typbibliothek aufgelisteten com-Elemente an.

Weitere Informationen zu Typbibliotheken finden Sie unter [Typbibliotheken und die Object Description Language](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).

 

 