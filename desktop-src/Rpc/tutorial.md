---
title: Lernprogramm
description: In diesem Tutorial werden die Schritte beschrieben, die zum Erstellen einer einfachen verteilten Einzelclientanwendung mit einem Einzelnen Server aus einer vorhandenen eigenständigen Anwendung erforderlich sind.
ms.assetid: afdfa037-58c0-4dcf-aa27-6839db0515e6
keywords:
- Remoteprozeduraufruf RPC , Tutorial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd7259e5f5f0b9d0d273ff99a7cd5b42d15d57beaa60300fadecb7045a96876
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011178"
---
# <a name="tutorial"></a>Lernprogramm

In diesem Tutorial werden die Schritte beschrieben, die zum Erstellen einer einfachen verteilten Einzelclientanwendung mit einem Einzelnen Server aus einer vorhandenen eigenständigen Anwendung erforderlich sind. Diese Schritte sind die folgenden:

-   Erstellen Sie Schnittstellendefinitions- und Anwendungskonfigurationsdateien.
-   Verwenden Sie den MIDL-Compiler, um C-Sprachclient- und Serverstubs und Header aus diesen Dateien zu generieren.
-   Schreiben Sie eine Clientanwendung, die ihre Verbindung mit dem Server verwaltet.
-   Schreiben Sie eine Serveranwendung, die die eigentlichen Remoteprozeduren enthält.
-   Kompilieren Sie diese Dateien, und verknüpfen Sie sie mit der RPC-Laufzeitbibliothek, um die verteilte Anwendung zu erstellen.

Die Clientanwendung übergibt eine Zeichenfolge in einem Remoteprozeduraufruf an den Server, und der Server gibt die Zeichenfolge "Hello, World" in der Standardausgabe aus.

Die vollständigen Quelldateien für diese Beispielanwendung mit zusätzlichem Code zum Verarbeiten von Befehlszeileneingaben und zum Ausgeben verschiedener Statusmeldungen an den Benutzer befinden sich im Verzeichnis RPC \\ Hello des Platform Software Development Kit (SDK).

In diesem Abschnitt wird die Diskussion in den folgenden Themen behandelt:

-   [Die eigenständige Anwendung](the-standalone-application.md)
-   [Definieren der Schnittstelle](defining-the-interface.md)
-   [Generieren der UUID](generating-the-uuid.md)
-   [Die IDL-Datei](the-idl-file.md)
-   [Die ACF-Datei](the-acf-file.md)
-   [Generieren der Stubdateien](generating-the-stub-files.md)
-   [Die Clientanwendung](the-client-application.md)
-   [Die Serveranwendung](the-server-application.md)
-   [Beenden der Serveranwendung](stopping-the-server-application.md)
-   [Kompilieren und Verknüpfen](compiling-and-linking.md)
-   [Ausführen der Anwendung](running-the-application.md)

 

 




