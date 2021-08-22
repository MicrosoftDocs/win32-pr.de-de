---
description: Die DLL/COM-Umleitung ist eine Isolationsstrategie für Anwendungen, die von Unternehmensadministratoren auf Windows XP verwendet wird.
ms.assetid: 5bbb0bee-d457-4dfa-93a0-82537fe11f2d
title: DLL/COM-Umleitung auf Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ce6b55c2a66d298b7b80248613eab7cefe96c25f8f53dd9218966e235ea267f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142263"
---
# <a name="dllcom-redirection-on-windows"></a>DLL/COM-Umleitung auf Windows

Die DLL/COM-Umleitung ist eine Isolationsstrategie für Anwendungen, die von Unternehmensadministratoren auf Windows XP verwendet wird.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP mit SP2: ** Die Verwendung von [DLL/COM-Umleitungsstrategien](about-side-by-side-assemblies-.md) wird nicht empfohlen, da isolierte Anwendungen, die Manifeste und nebenseitige Assemblys verwenden, einfacher zu aktualisieren und zu bedienen sind. Das Vorhandensein einer LOKALEN Datei wird ignoriert, wenn ein Manifest vorhanden ist. Die DLL/COM-Umleitungsstrategie mit lokalen Dateien funktioniert, wenn die Anwendung über kein Manifest verfügt.

Die DLL/COM-Umleitung bindet eine Anwendung an eine lokale Version einer Komponente. Die Dateien der lokalen Komponente können getrennt von der Systemversion der Komponente an einem Speicherort gespeichert werden, der für die Anwendung privat ist. Die Systemversion der Komponente ist global registriert und für alle anderen Anwendungen verfügbar, die daran gebunden sind. Die lokale Version der Komponente ist für die exklusive Verwendung der Anwendung reserviert. Bei Bedarf können die von der Anwendung verwendeten Komponentendateien gleichzeitig mit den Komponentendateien des Systems in den Arbeitsspeicher geladen werden.

Die DLL/COM-Umleitung wird aktiviert, indem eine spezielle Datei zusammen mit einer Kopie der lokalen Komponentendatei in demselben Verzeichnis wie die ausführbare Datei der Anwendung installiert wird. Die spezielle Datei ist eine leere Datei, die nach dem Dateinamen der ausführbaren Datei der Anwendung benannt und mit .local angefügt wird. Um beispielsweise die DLL/COM-Umleitung für eine Anwendung namens Myapp zu aktivieren, müssen die lokale Version der Komponente und eine leere Datei namens Myapp.exe.local in den Ordner kopiert werden, der Myapp.exe. Dadurch wird die Anwendung an die lokale Version der Komponente und nicht an die global freigegebene Version der Komponente gebunden.

Wenn eine Anwendung eine Komponentendatei lädt, z. B. eine DLL- oder OCX-Datei, sucht Windows zuerst in dem Ordner, in dem die LOKALE DATEI und die ausführbare Datei der Anwendung installiert sind. Wenn sie gefunden wird, verwendet die Anwendung diese Komponentendatei unabhängig von einem Verzeichnissuchpfad, der in der Anwendung oder in der Registrierung definiert ist. Wenn sie nicht gefunden wird, wird die Komponentendatei im definierten Suchpfad verwendet.

Das Installations-Hilfsprogramm muss folgende Schritte ausführen, um die Anwendung mit DLL/COM-Umleitung zu installieren:

-   Eine leere LOCAL-Datei muss in den gleichen Ordner wie die ausführbare Datei der Anwendung kopiert werden.
-   Alle komponenten-, DLL- und OCX-Dateien, die von der Anwendung verwendet werden, müssen in denselben Ordner wie die ausführbare Datei der Anwendung kopiert werden.
-   Isolierte COM-Komponenten müssen bei Windows registriert werden, damit verschiedene Versionen der Assembly nicht miteinander in Konflikt stehen, wenn sie gleichzeitig in den Arbeitsspeicher geladen werden. Der Registrierungsprozess erfordert, dass die Implementierung der Komponente zwischen Versionen geändert werden kann, bestimmte COM-Metadaten wie CLSID, ProgID, Typbibliothek und Threadingmodell jedoch nicht.
-   Wenn die Anwendung mithilfe des Windows Installers installiert wird, kann das Anwendungsverzeichnis mithilfe der LockPermissions-Tabelle gesichert werden. In der Regel erhält das System Lese-, Schreib- und Ausführungszugriff. allen anderen Prozessen wird nur Ausführungs- und Lesezugriff erteilt.

 

 



