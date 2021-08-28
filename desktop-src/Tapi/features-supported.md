---
description: Die folgende Liste enthält die von TAPI MSP unterstützten Features.
ms.assetid: e36bba94-1fa7-4514-9f8a-bcd690b04d73
title: Unterstützte Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f0a37664a578bd091ce9972c1979dc7d22f4db33ab2f8eb803bc2c83642f47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080510"
---
# <a name="features-supported"></a>Unterstützte Features

Die folgende Liste enthält die von TAPI MSP unterstützten Features.

-   Implementiert einen MSP, der eine einzelne Adresse pro Instanz des MSP verarbeitet. Mehrere like-Adressen werden verarbeitet, indem der MSP mehrmals instanziiert wird. Dies vereinfacht die Implementierung des MSP und der Basisklassen erheblich.
-   Implementiert alle MSPI-Schnittstellen, einschließlich [**ITMSPAddress,**](/windows/desktop/api/msp/nn-msp-itmspaddress) [**ITTerminalSupport,**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)und [**ITStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
-   Implementiert sofort einsatzbereite statische Terminals für Audio und Video.
-   Implementiert generische Terminalbasisklassen. Diese Terminalbasisklassen werden sowohl von den oben erwähnten statischen Terminalimplementierungen als auch von den Implementierungen dynamischer Terminals verwendet, die sich in Termmgr.dll. Der MSP kann sie auch verwenden, um zusätzliche Terminals zu implementieren.
-   Verwendet den Terminal-Manager, um dynamische Terminals zu verarbeiten. Erstellt dynamische Terminals in einem Arbeitsthread mit einer Nachrichtenpumpe (um Konsolenanwendungen von der Verarbeitung von Fenstermeldungen für Videorenderingterminals und zur Vereinfachung von Synchronisierungsproblemen frei zu machen).
-   Unterstützt Aufrufe, die ein Filterdiagramm pro Stream verwenden.
-   Implementiert die Behandlung von Graphereignissen.
-   Verwendet die Threadpooling-APIs in Verbindung mit einem eigenen Arbeitsthread, um Ereignisse zu behandeln.
-   Verwendet die Ablaufverfolgungs-APIs von Windows 2000 (ursprünglich für das Routingprojekt entwickelt) zusammen mit zusätzlicher Logik, um einen flexiblen, generischen Protokollierungsmechanismus zu bieten, der gleichzeitig in einer beliebigen Kombination der folgenden Dateien protokollieren kann: einem Benutzer- oder Kernelmodusdebugger; ein separates Konsolenfenster mit Protokollmeldungen, die nach Komponente getrennt sind; eine Protokolldatei.
-   Führt Freethreading aus.

 

 
