---
title: Tutorial
description: Dieses Tutorial führt Sie durch die Schritte, die erforderlich sind, um eine einfache verteilte Anwendung mit einem einzelnen Client aus einer vorhandenen eigenständigen Anwendung zu erstellen.
ms.assetid: afdfa037-58c0-4dcf-aa27-6839db0515e6
keywords:
- Remote Prozedur Aufruf RPC, Tutorial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c19b0d8ec3b3eb55cf29ccfd87eca43775c2ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037327"
---
# <a name="tutorial"></a>Tutorial

Dieses Tutorial führt Sie durch die Schritte, die erforderlich sind, um eine einfache verteilte Anwendung mit einem einzelnen Client aus einer vorhandenen eigenständigen Anwendung zu erstellen. Diese Schritte sind die folgenden:

-   Erstellen Sie Schnittstellendefinitionen und Anwendungs Konfigurationsdateien.
-   Verwenden Sie den-compilercompiler zum Generieren von Client-und Serverstub und-Headern in C-Sprache aus diesen Dateien.
-   Schreiben Sie eine Client Anwendung, die die Verbindung mit dem Server verwaltet.
-   Schreiben Sie eine Serveranwendung, die die eigentlichen Remote Prozeduren enthält.
-   Kompilieren Sie diese Dateien, und verknüpfen Sie Sie mit der RPC-Lauf Zeit Bibliothek, um die verteilte Anwendung zu erstellen.

Die Client Anwendung übergibt eine Zeichenfolge in einem Remote Prozedur Aufrufer an den Server, und der Server gibt die Zeichenfolge "Hello, World" in die Standardausgabe aus.

Die gesamten Quelldateien für diese Beispielanwendung mit zusätzlichem Code zum Behandeln der Befehlszeilen Eingabe und zum ausgeben verschiedener Statusmeldungen an den Benutzer finden Sie im \\ Verzeichnis "Hello Hello" des Platform Software Development Kit (SDK).

In diesem Abschnitt werden die folgenden Themen behandelt:

-   [Die eigenständige Anwendung](the-standalone-application.md)
-   [Definieren der Schnittstelle](defining-the-interface.md)
-   [Die UUID wird erzeugt.](generating-the-uuid.md)
-   [Die IDL-Datei](the-idl-file.md)
-   [Die ACF-Datei](the-acf-file.md)
-   [Erstellen der Stubdateien](generating-the-stub-files.md)
-   [Die Client Anwendung](the-client-application.md)
-   [Die Server Anwendung](the-server-application.md)
-   [Beenden der Server Anwendung](stopping-the-server-application.md)
-   [Kompilieren und verknüpfen](compiling-and-linking.md)
-   [Ausführen der Anwendung](running-the-application.md)

 

 




