---
description: Die Verwendung der integrierten Entwicklungsumgebung (Integrated Development Environment, IDE) von Microsoft Visual Basic für das Debuggen ermöglicht Visual Basic Entwicklern den Zugriff auf vertraute Tools und Benutzerfreundlichkeit.
ms.assetid: d31efc97-c286-434d-93f5-77b34ec16205
title: Debuggen in der Visual Basic IDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74574fdb289e1ad334337f17943c6961b95bf288
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393002"
---
# <a name="debugging-in-the-visual-basic-ide"></a>Debuggen in der Visual Basic IDE

Die Verwendung der integrierten Entwicklungsumgebung (Integrated Development Environment, IDE) von Microsoft Visual Basic für das Debuggen ermöglicht Visual Basic Entwicklern den Zugriff auf vertraute Tools und Benutzerfreundlichkeit. Obwohl viele Komponenten zu einem späteren Zeitpunkt mit der Microsoft Visual C++ Umgebung vollständig debuggt werden müssen, könnte eine Strategie darin bestehen, so viele Funktionen wie möglich mit Visual Basic zu debuggen. Beispielsweise können Sie die Visual Basic IDE für das Debuggen in com+ verwenden, wenn Sie noch kein Debugging von Multithreading, Komponenten Nachverfolgung, Remote aufrufen oder Prozess Isolation durchführen möchten.

Wenn Sie die Visual Basic Umgebung für das Debuggen verwenden, kompilieren Sie das Projekt im allgemeinen und fügen die dll einer COM+-Anwendung hinzu. Anschließend legen Sie die binäre Kompatibilität für das Projekt fest, verweisen auf die von Ihnen erstellte DLL und starten das Projekt, um mit dem Debuggen zu beginnen.

## <a name="general-guidelines-for-debugging-in-the-visual-basic-environment"></a>Allgemeine Richtlinien für das Debuggen in der Visual Basic Umgebung

-   Beim Debuggen mit Visual Basic behandelt com+ die Visual Basic Komponenten so, als ob Sie zu einer Bibliotheks Anwendung gehören, auch wenn die Komponenten als zu einer Serveranwendung gehörend registriert sind. Da es als Bibliotheks Anwendung ausgeführt wird, werden die Komponenten Symbole im Verwaltungs Programmkomponenten Dienste beim debuggten der Komponenten nicht gedreht.
-   Wenn Sie während des Debuggens Transaktions Attribute für eine Komponente ändern oder eine Quell Codeänderung vornehmen, bei der Visual Basic eine neue CLSID oder ProgID generieren müssen, müssen Sie die COM+-Anwendung, die die Komponente enthält, löschen und neu installieren. Wenn Sie die binäre Kompatibilität für die Komponente festgelegt haben, werden Sie gewarnt, dass Änderungen aufgetreten sind.

## <a name="notes-on-debugging-within-a-com-application"></a>Hinweise zum Debuggen in einer COM+-Anwendung

-   Wenn Sie Änderungen an der Visual Basic IDE in den Schnittstellen der Komponente, Klassennamen, Projektnamen, Transaktionsunterstützung oder anderen Einstellungen vornehmen, treten möglicherweise Konflikte zwischen den Konfigurationsdaten im Komponenten Dienst-Explorer und der eigentlichen Konfiguration auf, die im Visual Basic Debugger ausgeführt wird.
-   Exportieren Sie eine COM+-Anwendung nicht, während Sie eine Komponente in der Anwendung debuggen. Com+ behandelt die Visual Basic Entwicklungsumgebung als Komponente.
-   Wenn Sie eine Komponente außerhalb des Debuggers ausführen und dann das Debuggen starten möchten, wird eine Instanz der Komponente möglicherweise weiterhin in com+ ausgeführt, wenn Sie Sie im Debugger starten. Com+ erkennt diese Bedingung und versucht, die Instanz, die Sie steuert, automatisch herunterzufahren. Um dieses Problem zu vermeiden, entfernen Sie die Komponente aus dem Verwaltungs Programmkomponenten Dienste, bevor Sie mit dem Debuggen beginnen.

**So debuggen Sie mithilfe der Visual Basic Umgebung**

1.  Öffnen Sie das Komponenten Projekt in Visual Basic.

2.  Kompilieren Sie die Komponente, und legen Sie dann die binäre Kompatibilität in Ihrem Projekt auf die kompilierte Komponente fest.

3.  Legen Sie die mtstransaktionmode-Eigenschaft auf einen anderen Wert als 0-notanmtsobject fest. Wenn Sie das Projekt starten, werden Visual Basic durch diese Einstellung aufgefordert, Ihre Komponente in com+ zu aktivieren.

4.  Klicken Sie im Menü **Projekt** auf **Eigenschaften**, und geben Sie dann das Programmstart auf der Registerkarte **Debuggen** ein. Das Start Programm ist die ausführbare Client Datei, die diese Komponente aufruft.

    > [!Note]  
    > Das Start Programm muss für die Komponente, die Sie Debuggen, lokal sein.

     

5.  Drücken Sie F5, um mit dem Debuggen der Komponente zu beginnen.

Nachdem Sie F5 drücken, wird Visual Basic die Client Anwendung starten und die Komponente im Debugmodus ausführen. Sie können Haltepunkte im Code der Komponente platzieren und Uhren für Variablen festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Com+-Visual Basic Debugunterstützung im Vergleich zu MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Debuggen kompilierter Visual Basic Komponenten](debugging-compiled-visual-basic-components.md)
</dt> </dl>

 

 



