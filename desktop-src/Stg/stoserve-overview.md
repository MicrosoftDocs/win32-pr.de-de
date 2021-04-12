---
title: Übersicht über stoservice
description: Im stoservice-Codebeispiel wird veranschaulicht, wie strukturierte Speicherdienste verwendet werden, die in der Implementierung der Verbund Dateien bereitgestellt werden. Die Verwendung der IStorage-Standardschnittstellen und der IStream-Schnittstelle wird beschrieben.
ms.assetid: 41ccd333-15c8-46b2-91c6-3e1929f7198c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0c8325fbc20d4917785d0b83ca70bffa996824
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315932"
---
# <a name="stoserve-overview"></a>Übersicht über stoservice

## <a name="purpose"></a>Zweck

Der Hauptschwerpunkt dieses Code Beispiels ist die Verwendung strukturierter Speicherdienste, die in der Implementierung der Verbund Dateien bereitgestellt werden. Die Verwendung der [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Standardschnittstellen und der [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) -Schnittstelle wird beschrieben. **Stoservice** arbeitet mit dem Codebeispiel von [stoclien](structured-storage-client-sample--stoclien-.md) zusammen, um die gemeinsame Verwendung der Verbund Dateispeicherung durch Client und Server zu veranschaulichen.

## <a name="functionality"></a>Funktionalität

Im **stoservice** -Beispiel wird das copaper-com-Objekt eingeführt, das praktisch ein leeres Blatt mit Zeichnungs Papier darstellt.

Copaper-Objekte machen eine Reihe von Funktionen für die Freiformzeichnung auf der Papieroberfläche verfügbar, indem "Ink" der angegebenen Farbe und Breite verwendet wird. Die Funktionalität ähnelt der "Scribble"-Lernprogramm Beispiele in vielen Versionen von Microsoft Visual C++. Der Unterschied in den **stoservitebeispielen von stoservien** /  ist eine Architektur basiert hauptsächlich auf der com-Technologie. Die elektronischen Zeichnungs Papier Features von copaper-Objekten sind für Clients über eine benutzerdefinierte [**iPaper**](ipaper-methods.md) -Schnittstelle verfügbar. Copaper implementiert die **iPaper** -Schnittstelle. Zwischen Client und Server wird eine deutliche Unterscheidung der Architektur beibehalten. Es wird keine grafische Benutzeroberfläche (GUI) von copaper bereitgestellt. Der Entwurf des copaper-Objekts basiert auf dem Client für alle GUI-Verhaltensweisen. Copaper kapselt nur die serverbasierte Erfassung und Speicherung der gezeichneten frei Hand Daten.

Die frei Hand Daten, die auf der copaper-Oberfläche gezeichnet werden, können in Verbund Dateien gespeichert und aus diesen geladen werden. Die [**iPaper**](ipaper-methods.md)-, [**Save**](ipaper--save.md) -und [**Load**](ipaper--load.md) -Methoden akzeptieren einen [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstellen Zeiger. Copaper verwendet diese vom Client bereitgestellte **IStorage** -Schnittstelle zum Speichern der Zeichnungsdaten.

Copaper ist in einem in-Process-Server abgelegt und wird als benutzerdefinierte COM-Komponente öffentlich verfügbar gemacht. Ähnlich wie andere Server in dieser tutorialreihe ist stoservice ein com-Server, der sich selbst registriert. Der copaper-Objekttyp wird den Clients als dllpaper-Komponente mithilfe einer CLSID- \_ dllpaper-Registrierung in der Registrierung zur Verfügung gestellt.

Wie beim vorherigen Server für die Einsparung werden Verbindungs fähigen Object-Funktionen in copaper unterstützt. Die [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) -Schnittstelle ist verfügbar, und es wird ein geeigneter Verbindungspunkt implementiert. In diesem Kontext wird eine ausgehende benutzerdefinierte ipapersink-Schnittstelle für das Senden von Benachrichtigungen an den Client deklariert.

Die zwei benutzerdefinierten [**iPaper**](ipaper-methods.md) -und [**ipapersink**](ipapersink-methods.md) -Schnittstellen werden in iPaper deklariert. H befindet sich im Verzeichnis "Common sibens \\ Inc". Die GUIDs für die Schnittstellen und Objekte werden in papguids definiert. H befindet sich in demselben allgemeinen Include-Verzeichnis.

Die cThread-Funktion in apputil wird von **stoservice** verwendet, um Thread Sicherheit zu erzielen, wie Sie im Beispiel "freservice" war. Copaper-Objekte werden von der cthreaded-Klasse abgeleitet und Erben deren ownthis-und unownthis-Methoden. Diese Methoden ermöglichen nur einem Thread gleichzeitig Zugriff auf den **stoservice** -Server und auf copaper-Objekte, die vom Server verwaltet werden.

## <a name="copaper-com-object"></a>Copaper com-Objekt

Das copaper com-Objekt ist der einzelne Objekttyp, der von diesem **stoservice** -Prozess internen Server verwaltet wird. Copaper wird als Verbindbares com-Objekt mit einer Implementierung der standardmäßigen [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) -Schnittstelle und einer Implementierung der benutzerdefinierten [**iPaper**](ipaper-methods.md) -Schnittstelle erstellt. Copaper macht die **iPaper** -Schnittstelle verfügbar, damit Clients einen kleinen Satz elektronischer Papier Operationen für eine Instanz des copaper ausführen können. Die grundlegenden Vorgänge sind das Starten einer frei Hand Zeichnungs Sequenz, das Zeichnen der frei Hand Daten auf einer kopierenden virtuellen Papieroberfläche und das Beenden der frei Hand Zeichnungs Sequenz. In diesem Schema wird angenommen, dass es sich bei dem Client um eine GUI-Anwendung handelt, die von einer Maus oder einem Tablet Gerät gesteuert wird Der Client ist für die Übersetzung von Mausbewegungen in Anforderungen an copaper zuständig, wodurch diese Anforderungen als frei Hand Daten gespeichert werden.

Es gibt zwei Ebenen von frei Hand Daten, die in copaper gespeichert werden. Copaper speichert die frei Hand Daten in einem RAM-basierten Array, das die aktuelle Zeichnung darstellt, und copaper speichert permanent eine gesamte Zeichnung in einer Verbund Datei. Methoden in der [**iPaper**](ipaper-methods.md) -Schnittstelle führen beide aus.

Da der Client die gezeichneten Papier Daten nicht verwaltet, sondern als Bild auf dem Bildschirm Rendern muss, muss die [**iPaper**](ipaper-methods.md) -Implementierung in copaper eine Methode verfügbar machen, die dem Client das Abrufen der Zeichnungsdaten ermöglicht. Zu diesem Zweck wird die Verbindungs fähige Objekttechnologie in copaper verwendet. Ein \_ Verbindungspunkt für einen Verbindungspunkt mit einem Verbindungspunkt wird von copaper implementiert, sodass ein Client eine Verbindung mit copaper herstellen kann, um die frei Hand Daten zum Zeichnen zu empfangen. Der Client ruft zunächst die [iPaper:: Redraw](ipaper--redraw.md) -Methode für das copaper-Objekt auf, um alle frei Hand Daten der aktuellen Zeichnung anzufordern. Die copaper-Implementierung von Redraw verwendet dann die Client Implementierung von [**itaschen Sink**](ipapersink-methods.md) , um die Daten an den Client zu übergeben.

Wenn der Benutzer die Daten interaktiv auf dem Client zeichnet, werden die Daten sofort auf den Bildschirm gezeichnet, während Sie auch zum Speichern an copaper gesendet werden. Wenn der Client erfordert, dass der Bildschirm neu gezeichnet wird, ruft er die copaper [Redraw](ipaper--redraw.md) -Methode auf. Solche Neuzeichnungen werden in-Anwendungen häufig eingesetzt. Beispielsweise tritt ein Neuzeichnen auf, wenn das Client Fenster durch ein anderes Anwendungsfenster überlagert wird. Der Client verfügt über ein Bitmap-Rendering des gezeichneten Bilds, aber die Bitmap ist leicht verloren und muss häufig neu gezeichnet werden. Der Client verwendet copaper auf dem Server für die frei Hand Daten, die für das Neuzeichnen erforderlich sind.

Dabei handelt es sich um eine gemeinsame Client/Server-Division von Arbeit. Dies ist insbesondere dann sinnvoll, wenn es erforderlich ist, dass mehrere Clients die Daten gemeinsam nutzen. Copaper ist so codiert, dass dies möglich ist. Er verwendet die apputil-cthreadfunktion, um Thread Sicherheit zu erzielen. Eine Anwendung, die dieses Design ausnutzen könnte, ist eine freigegebene Whiteboardanwendung, bei der mehrere Clients an einer häufig angezeigten Zeichnung mitwirken können. Die com-Unterstützung für verteiltes com (DCOM) unterstützt diese Art von Anwendungs Verwendung im gesamten Netzwerk. Weitere Informationen finden Sie im vorherigen remclien-Beispiel.

Eine präziseere Verwendung des copaper-Client-/Serverschemas besteht darin, das Verhalten für Objekte zu integrieren, die in verschiedenen Anwendungen auf demselben Computer implementiert werden. In diesem Fall kann es sich bei den Clients um einen ActiveX-Container in separaten Anwendungen handeln, die vom selben Objekt verwaltete Daten gemeinsam nutzen. Bei diesen Daten handelt es sich möglicherweise nicht um frei Handzeichen Daten, die von der Komponente dllpaper unterstützt **Stoservice** kann als Start Framework für die Programmierung von Komponenten verwendet werden, die andere Typen von freigegebenen Daten verwalten.

## <a name="support-information"></a>Supportinformationen

Der **stoservice** Makefile registriert die " **stoservice** "-com-Komponente "dllpaper" in der Registrierung. Diese Komponente muss registriert werden, bevor **stoservice** für externe COM-Clients als Server für diese Komponente verfügbar ist. Diese Selbstregistrierung erfolgt mithilfe des Register.exe-Hilfsprogramms, das in das Register Sample integriert ist. Zum Erstellen oder Ausführen von **stoservice** erstellen Sie zuerst das Register Codebeispiel.

Weitere Informationen zum Einrichten des Systems zum Erstellen und Testen der Codebeispiele in dieser com-tutorialreihe finden Sie unter [Erstellen von Beispielen](how-to-build-samples.md). Das angegebene Makefile-Element (Makefile) ist Microsoft NMAKE-kompatibel. Wenn Sie einen Debugbuild erstellen möchten, geben Sie im Eingabe Aufforderungs Fenster den Befehl NMAKE aus.

Für eine bequeme Verwendung in Microsoft Visual Studio wird eine Projektdatei für jedes Beispiel bereitgestellt. Wenn Sie das Projekt für das **stoservice** -Beispiel laden möchten, können Sie Visual Studio wie folgt an der Eingabeaufforderung im Verzeichnis "Samples" ausführen:

Msdev-stoservice. DSP

Sie können auch auf die Datei stoservice. DSP in Windows-Explorer doppelklicken, um ein Beispiel Projekt in Visual Studio zu laden. In Visual Studio können Sie die C++-Klassen der Beispiel Quelle durchsuchen und im Allgemeinen die anderen edit-compile-Debug-Vorgänge durchführen.

> [!Note]  
> Als Teil des Platform Software Development Kit (SDK) erfordert die Kompilierung dieser Beispiele in Visual Studio die ordnungsgemäße Einstellung von Verzeichnis Pfaden in Visual Studio. Weitere Informationen finden Sie unter [Erstellen von Beispielen](how-to-build-samples.md).

 

 

 