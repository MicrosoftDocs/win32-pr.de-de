---
description: Die Windows-Benutzeroberfläche ermöglicht Benutzern den Zugriff auf eine Vielzahl von Objekten, die für die Ausführung von Anwendungen und die Verwaltung des Betriebssystems erforderlich sind.
title: Windows-Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1d0d4ed7-9b85-4d70-bf1f-82567a1687fb
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 448e1d5265ec34ce1889ca36f234622e2b082553
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979904"
---
# <a name="windows-shell"></a>Windows-Shell

Die Windows-Benutzeroberfläche ermöglicht Benutzern den Zugriff auf eine Vielzahl von Objekten, die für die Ausführung von Anwendungen und die Verwaltung des Betriebssystems erforderlich sind. Die häufigsten und vertrauten Objekte sind die Ordner und Dateien, die sich auf Computer Laufwerken befinden. Es gibt auch eine Reihe von virtuellen Objekten, die es dem Benutzer ermöglichen, Aufgaben auszuführen, z. b. das Senden von Dateien an Remote Drucker oder den Zugriff auf den Papierkorb. Die Shell organisiert diese Objekte in einem hierarchischen Namespace und bietet Benutzern und Anwendungen eine konsistente und effiziente Möglichkeit, auf Objekte zuzugreifen und diese zu verwalten.

## <a name="shell-development-scenarios"></a>Shellentwicklungs Szenarien

Die folgenden Entwicklungsszenarien beziehen sich auf die Anwendungsentwicklung:

-   Erweitern der Shell, die das Erstellen einer Datenquelle (im Gegensatz zum Verarbeiten des shelldatenmodells) umfasst
-   Implementieren einer Teilmenge der Shell-Datenquellen Tasks
-   Unterstützende Bibliotheken und Element Ansichten in Windows-Explorer
-   Verwenden des allgemeinen Datei Dialogfelds
-   Implementieren von System Steuerungselementen
-   Verwalten von Benachrichtigungen

Die folgenden Entwicklungsszenarien beziehen sich auf den Besitz des Datei Formats:

-   Implementieren einer Teilmenge der Shell-Datenquellen Tasks
-   Implementieren eines beliebigen Handlers
-   Unterstützung der Desktop Suche

Die folgenden Entwicklungsszenarien beziehen sich auf den Datenspeicher Besitz:

-   Unterstützung der Desktop Suche und OpenSearch
-   Implementieren einer Teilmenge der Shell-Datenquellen Tasks (virtuelle Ordner)
-   Unterstützende Bibliotheken in Windows-Explorer

Das folgende Entwicklungsszenario bezieht sich auf die Geräte Unterstützung:

-   Automatisch ausführen und automatisch abspielen

## <a name="windows-shell-sdk-documentation"></a>Dokumentation zum Windows Shell SDK

Diese Dokumentation ist in drei Hauptabschnitte unterteilt:

-   Das [shellentwicklerhandbuch](intro.md) bietet konzeptionelle Informationen zur Funktionsweise der Shell und zur Verwendung der Shell-API in Ihrer Anwendung.
-   Der Abschnitt " [Shellverweis](shell-reference-bumper.md) " dokumentiert Programmier Elemente, die die verschiedenen Shell-APIs bilden.
-   [Shellbeispiele](samples-entry.md) bieten Links zu verwandten Codebeispielen.

In der folgenden Tabelle finden Sie einen Überblick über den Abschnitt shellreferenz. Sofern nicht anders angegeben, werden alle Programmier Elemente in nicht verwaltetem C++ dokumentiert.



| `Section`                                                               | BESCHREIBUNG                                                                                                          |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Shellklassen](classes.md)                                          | In diesem Abschnitt werden Windows-shellklassen auswählen beschrieben.                                                                 |
| [Shellschnittstellen](interfaces.md)                                    | In diesem Abschnitt werden die Schnittstellen der Windows Shell-Component Object Model (com) beschrieben.                                    |
| [Shellfunktionen](functions.md)                                      | In diesem Abschnitt werden die Windows-Shellfunktionen beschrieben.                                                                  |
| [Shellrückruf Funktionen](callbacks.md)                             | In diesem Abschnitt werden die Vorlagen für Windows Shell-Rückruf Funktionen beschrieben.                                               |
| [Shellkonstanten, Enumerationen und Flags](consts-enums-flags.md)    | In diesem Abschnitt werden die in den Shell-APIs verwendeten Windows Shell-Konstanten, Enumerationen und Flags beschrieben.                  |
| [Shell Lightweight Utility-Funktionen](shlwapi.md)                    | In diesem Abschnitt werden die in Shlwapi.dll bereitgestellten Windows Shell Lightweight Utility-Funktionen beschrieben.                      |
| [Shellmakros](macros.md)                                            | In diesem Abschnitt werden die Makros des Windows Shell-Hilfsprogramms beschrieben.                                                             |
| [Shellnachrichten und Benachrichtigungen](messages.md)                      | In diesem Abschnitt werden die Nachrichten und Benachrichtigungen beschrieben, die von Elementen der Windows-Shell gesendet werden.                         |
| [Shellobjekte für Skripterstellung und Microsoft-Visual Basic](objects.md) | In diesem Abschnitt werden die Windows-Objekte beschrieben, die von der Shell für die Verwendung in Skripts und Microsoft Visual Basic implementiert werden |
| [Shellobjekte für C++](objects-cpp.md)                              | In diesem Abschnitt werden die von der Shell implementierten C++-Windows-Objekte beschrieben.                                             |
| [Shellschemas](schemas.md)                                          | In diesem Abschnitt werden die von der Windows-Shell verwendeten Bibliotheks-, Eigenschafts-und Übertragungs manifest-Schemas beschrieben.                   |
| [Shellstrukturen](structures.md)                                    | In diesem Abschnitt werden die in den Shell-APIs verwendeten Windows Shell-Strukturen beschrieben.                                          |



 

 

 



