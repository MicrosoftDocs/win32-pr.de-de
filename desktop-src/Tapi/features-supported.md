---
description: Die folgende Liste enthält die von TAPI MSP unterstützten Funktionen.
ms.assetid: e36bba94-1fa7-4514-9f8a-bcd690b04d73
title: Unterstützte Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d10fd9ac787483b8dfa6e15046a733992adb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214624"
---
# <a name="features-supported"></a>Unterstützte Features

Die folgende Liste enthält die von TAPI MSP unterstützten Funktionen.

-   Implementiert ein msp, das eine einzelne Adresse pro MSP-Instanz verarbeitet. Mehrere like-Adressen werden verarbeitet, indem das MSP mehrmals instanziiert wird. Dies vereinfacht die Implementierung des MSP und der Basisklassen erheblich.
-   Implementiert alle MSPi-Schnittstellen, einschließlich [**itmspaddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**itterminalsupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**itstreamcontrol**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)und [**itstream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).
-   Implementiert gebrauchsfertige statische Terminals für Audiodaten und Videos.
-   Implementiert generische Terminal Basisklassen. Diese Terminal Basisklassen werden sowohl von den oben erwähnten statischen Terminal Implementierungen als auch von den Implementierungen dynamischer Terminals verwendet, die in Termmgr.dll gefunden werden. Der MSP kann Sie auch verwenden, um zusätzliche Terminals zu implementieren.
-   Verwendet den Terminal-Manager zum Verarbeiten dynamischer Terminals. Erstellt dynamische Terminals in einem Arbeitsthread mit einem nachrichtenpump (um Konsolen Anwendungen zu untersuchen, um Fenster Meldungen für videorenderterminals zu verarbeiten und Synchronisierungs Probleme zu vereinfachen).
-   Unterstützt Aufrufe, bei denen ein Filter Diagramm pro Stream verwendet wird.
-   Implementiert die Verarbeitung von Diagramm Ereignissen.
-   Verwendet die Thread Pooling-APIs in Verbindung mit einem eigenen Arbeits Thread, um Ereignisse zu behandeln.
-   Verwendet die Ablaufverfolgungs-APIs von Windows 2000 (ursprünglich für das Routing Projekt entwickelt) zusammen mit zusätzlicher Logik, um einen flexiblen, generischen Protokollierungs Mechanismus bereitzustellen, der gleichzeitig in einer beliebigen Kombination aus folgendem protokolliert werden kann: einem Benutzer-oder Kernel Modus-Debugger. ein separates Konsolenfenster, in dem Protokollmeldungen durch die Komponente getrennt sind. eine Protokolldatei.
-   Führt eine kostenlose Thread Ausführung aus.

 

 
