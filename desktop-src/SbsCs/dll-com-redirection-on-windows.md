---
description: Die DLL-/COM-Umleitung ist eine Anwendungs Isolations Strategie, die von Unternehmens Administratoren unter Windows XP verwendet wird.
ms.assetid: 5bbb0bee-d457-4dfa-93a0-82537fe11f2d
title: DLL-/COM-Umleitung unter Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e356c7b4cc6e5616a03eba60439c7478d65e626a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867268"
---
# <a name="dllcom-redirection-on-windows"></a>DLL-/COM-Umleitung unter Windows

Die DLL-/COM-Umleitung ist eine Anwendungs Isolations Strategie, die von Unternehmens Administratoren unter Windows XP verwendet wird.

* * Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP mit SP2: * * die Verwendung von dll/com-Umleitungs Strategien ist nicht empfehlenswert, da isolierte Anwendungen, die Manifeste und parallele Assemblys verwenden, einfacher zu [aktualisieren und zu bedienen sein können.](about-side-by-side-assemblies-.md) Das vorhanden sein einer lokalen Datei wird ignoriert, wenn ein Manifest vorhanden ist. Die dll/com-Umleitungs Strategie, die lokale Dateien verwendet, funktioniert, wenn die Anwendung nicht über ein Manifest verfügt.

Die DLL-/COM-Umleitung bindet eine Anwendung an eine lokale Version einer Komponente. Die Dateien der lokalen Komponente können getrennt von der System Version der Komponente an einem Speicherort gespeichert werden, der für die Anwendung privat ist. Die Version der Komponente des Systems ist Global registriert und steht allen anderen Anwendungen zur Verfügung, die Sie binden. Die lokale Version der Komponente ist für die ausschließliche Verwendung der Anwendung reserviert. Falls erforderlich, können die von der Anwendung verwendeten Komponenten Dateien zur gleichen Zeit wie die Komponenten Dateien des Systems in den Arbeitsspeicher geladen werden.

Die DLL-/COM-Umleitung wird aktiviert, indem eine spezielle Datei zusammen mit einer Kopie der lokalen Komponenten Datei in demselben Verzeichnis wie die ausführbare Datei der Anwendung installiert wird. Die spezielle Datei ist eine leere Datei, die nach dem Dateinamen der ausführbaren Anwendung benannt und mit. local angefügt wird. Um z. b. die DLL-/COM-Umleitung für eine Anwendung mit dem Namen "MyApp" zu aktivieren, müssen die lokale Version der Komponente und eine leere Datei mit dem Namen "Myapp.exe. local" in den Ordner mit Myapp.exe kopiert werden. Dadurch wird die Anwendung an die lokale Version der Komponente und nicht an die Global freigegebene Version der Komponente gebunden.

Wenn eine Anwendung eine Komponenten Datei (z. b. eine DLL-oder OCX-Datei) lädt, sucht Windows zuerst in dem Ordner, in dem die lokale und ausführbare Datei der Anwendung installiert ist. Wenn Sie gefunden wird, verwendet die Anwendung diese Komponenten Datei unabhängig von einem Verzeichnis Suchpfad, der in der Anwendung oder in der Registrierung definiert ist. Wenn nicht gefunden, wird die Komponenten Datei im definierten Suchpfad verwendet.

Das Installations Dienstprogramm muss Folgendes ausführen, um die Anwendung mit DLL-/COM-Umleitung zu installieren:

-   Eine leere lokale Datei muss in denselben Ordner wie die ausführbare Datei der Anwendung kopiert werden.
-   Alle Komponenten, DLL-Dateien und OCX-Dateien, die von der Anwendung verwendet werden, müssen in denselben Ordner wie die ausführbare Datei der Anwendung kopiert werden.
-   Isolierte COM-Komponenten müssen bei Windows registriert werden, damit verschiedene Versionen der Assembly nicht miteinander in Konflikt stehen, wenn Sie gleichzeitig in den Arbeitsspeicher geladen werden. Der Registrierungsvorgang erfordert, dass die Implementierung der Komponente Zwischenversionen geändert werden kann, bestimmte com-Metadaten, wie z. b. CLSID, ProgID, Typbibliothek und Threading Modell, sind jedoch nicht möglich.
-   Wenn die Anwendung mit dem Windows Installer installiert wird, kann das Anwendungsverzeichnis mithilfe der lockberechtigungs-Tabelle gesichert werden. In der Regel erhält das System Lese-, Schreib-und Ausführungs Zugriff. alle anderen Prozesse erhalten nur den Ausführungs-und Lesezugriff.

 

 



