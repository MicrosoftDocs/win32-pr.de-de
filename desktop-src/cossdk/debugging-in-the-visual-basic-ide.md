---
description: Die Verwendung der integrierten Entwicklungsumgebung (Integrated Development Environment, IDE) von Microsoft Visual Basic zum Debuggen bietet Visual Basic Entwicklern Zugriff auf vertraute Tools und benutzerfreundliche Funktionen.
ms.assetid: d31efc97-c286-434d-93f5-77b34ec16205
title: Debuggen in der Visual Basic-IDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 284e97a766256cd281b3515bdd142d15ff5208e2c1a1555438c428daeca8f3a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548009"
---
# <a name="debugging-in-the-visual-basic-ide"></a>Debuggen in der Visual Basic-IDE

Die Verwendung der integrierten Entwicklungsumgebung (Integrated Development Environment, IDE) von Microsoft Visual Basic zum Debuggen bietet Visual Basic Entwicklern Zugriff auf vertraute Tools und benutzerfreundliche Funktionen. Obwohl viele Komponenten letztendlich mithilfe der Microsoft Visual C++-Umgebung vollständiger debuggen werden müssen, kann eine Strategie darin sein, zuerst so viele Funktionen wie möglich mit Visual Basic zu debuggen. Beispielsweise können Sie die Visual Basic-IDE für das Debuggen in COM+ verwenden, wenn Sie noch kein Multithreading, Komponentennachverfolgung, Remoteaufrufe oder Prozessisolation debuggen.

Wenn Sie die Visual Basic-Umgebung zum Debuggen verwenden, kompilieren Sie zunächst das Projekt und fügen die DLL einer COM+-Anwendung hinzu. Anschließend legen Sie binäre Kompatibilität für das Projekt fest, verweisen auf die dll, die Sie erstellt haben, und starten das Projekt, um mit dem Debuggen zu beginnen.

## <a name="general-guidelines-for-debugging-in-the-visual-basic-environment"></a>Allgemeine Richtlinien für das Debuggen in der Visual Basic-Umgebung

-   Beim Debuggen mit Visual Basic behandelt COM+ die Visual Basic Komponenten so, als ob sie zu einer Bibliotheksanwendung gehören, auch wenn die Komponenten als zu einer Serveranwendung gehörend registriert sind. Da sie als Bibliotheksanwendung ausgeführt wird, drehen sich die Komponentensymbole im Verwaltungstool Komponentendienste nicht, wenn die Komponenten debuggen werden.
-   Wenn Sie transaktionsattribute für eine Komponente während des Debuggens ändern oder eine Quellcodeänderung vornehmen, die erfordert, dass Visual Basic eine neue CLSID oder ProgID generiert, stellen Sie sicher, dass Sie die COM+-Anwendung löschen und neu installieren, die die Komponente enthält. Wenn Sie binäre Kompatibilität für die Komponente festgelegt haben, werden Sie gewarnt, dass Änderungen aufgetreten sind.

## <a name="notes-on-debugging-within-a-com-application"></a>Hinweise zum Debuggen innerhalb einer COM+-Anwendung

-   Wenn Sie Änderungen an der Visual Basic-IDE in den Schnittstellen, Klassennamen, Projektnamen, Transaktionsunterstützung oder anderen Einstellungen ihrer Komponente vornehmen, kann es zu Einem Konflikt zwischen den Konfigurationsdaten im Komponentendienste-Explorer und der tatsächlichen Konfiguration kommen, die im Visual Basic Debugger ausgeführt wird.
-   Exportieren Sie keine COM+-Anwendung, während Sie eine Komponente in der Anwendung debuggen. COM+ behandelt die Visual Basic Entwicklungsumgebung als Komponente.
-   Wenn Sie eine Komponente außerhalb des Debuggers ausführen und dann mit dem Debuggen beginnen möchten, wird eine Instanz der Komponente möglicherweise weiterhin in COM+ ausgeführt, wenn Sie sie im Debugger starten. COM+ erkennt diese Bedingung und versucht, die von ihr kontrollierte Instanz unbeaufsichtigt herunterzufahren. Um dieses Problem zu vermeiden, entfernen Sie die Komponente aus dem Component Services-Verwaltungstool, bevor Sie mit dem Debuggen beginnen.

**So debuggen Sie mithilfe der Visual Basic-Umgebung**

1.  Öffnen Sie das Komponentenprojekt in Visual Basic.

2.  Kompilieren Sie die Komponente, und legen Sie dann binäre Kompatibilität in Ihrem Projekt auf die kompilierte Komponente fest.

3.  Legen Sie die MTSTransactionMode-Eigenschaft auf einen anderen Wert als 0 fest: NotAnMTSObject. Wenn Sie das Projekt starten, fordert diese Einstellung Visual Basic auf, Ihre Komponente in COM+ zu aktivieren.

4.  Klicken Sie **im menü Project** auf **Eigenschaften**, und geben Sie dann das Startprogramm auf der Registerkarte **Debuggen** ein. Das Startprogramm ist die ausführbare Clientdatei, die diese Komponente aufruft.

    > [!Note]  
    > Das Startprogramm muss lokal für die Komponente sein, die Sie debuggen.

     

5.  Drücken Sie F5, um mit dem Debuggen der Komponente zu beginnen.

Nachdem Sie F5 gedrückt haben, startet Visual Basic die Clientanwendung und führt die Komponente im Debugmodus aus. Sie können Haltepunkte im Code der Komponente platzieren und Überwachungen für Variablen festlegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+ Visual Basic Debugunterstützung im Vergleich zu MTS](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Debuggen von kompilierten Visual Basic Komponenten](debugging-compiled-visual-basic-components.md)
</dt> </dl>

 

 



