---
title: Beispiele (RPC)
description: Beispiele, die RPC-Konzepte (Remote Procedure Call) veranschaulichen.
ms.assetid: d5db3085-6df0-4539-a605-d60055f4f4ec
keywords:
- Remoteprozeduraufruf RPC , Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e75dca3866e325a4f10eb446d209b834b62ff0407e7edd19f92ec70ac700df85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930049"
---
# <a name="examples-rpc"></a>Beispiele (RPC)

Das Platform Software Development Kit (SDK) enthält Beispiele, die wie folgt eine Vielzahl von RPC-Konzepten (Remote Procedure Call) veranschaulichen:

-   ASYNCRPC veranschaulicht die Struktur einer RPC-Anwendung, die asynchrone Remoteprozeduraufrufe verwendet. Außerdem werden verschiedene Methoden zur Benachrichtigung über den Abschluss des Aufrufs veranschaulicht.
-   CLUUID veranschaulicht die Verwendung der Clientobjekt-UUID, um einem Client die Auswahl aus mehreren Implementierungen einer Remoteprozedur zu ermöglichen.
-   Das Verzeichnis DATA enthält vier Programme: DUNION veranschaulicht unterscheidungsverschlüsselte (nicht gekapselte) Unions; INOUT veranschaulicht [ \[ in \] ](../midl/in.md) [ \[ \] out-Parameter.](../midl/out-idl.md) REPAS veranschaulicht die [Darstellung \_ als](/windows/desktop/Midl/represent-as) Attribut. XMIT veranschaulicht die [Übertragung \_ als](/windows/desktop/Midl/transmit-as) Attribut.
-   DLIPPT veranschaulicht eine Clientanwendung, die ihre Verbindung mit dem Server über dynamische Endpunkte verwaltet.
-   Das Verzeichnis FILEREP enthält vier Beispiele, die veranschaulichen, wie Entwickler einen einfachen Dateireplikationsdienst, einen Dateireplikationsdienst mit mehreren Benutzern, einen Dienst, der Sicherheitsfeatures unterstützt, und einen Dienst mit rpc-asynchronen Pipes schreiben können.
-   Das Handles-Verzeichnis enthält die drei Programme AUTO, CXHNDL und USRDEF, die das [automatische \_ Handle,](/windows/desktop/Midl/auto-handle) \[ das \_ Kontexthandle \] und generische (benutzerdefinierte) Handles veranschaulichen.
-   HELLO ist eine Client/Server-Implementierung von "Hello, world".
-   Das VERZEICHNIS PICKLE enthält zwei Programme: PICKLP veranschaulicht die Datenprozedurserialisierung. PICKLT veranschaulicht die Datentypserialisierung. beide Programme verwenden die [ \[ Codierungs- \] ](../midl/encode.md) und [ \[ \] Decodierungsattribute.](../midl/decode.md)
-   PIPES veranschaulicht die Verwendung des Pipetypkonstruktors.
-   RPCSVC veranschaulicht die Implementierung eines Diensts mit RPC.
-   STROUT veranschaulicht, wie Speicher auf einem Server für ein zweidimensionales Objekt (ein Array von Zeigern) belegt und als \[ out-only-Parameter an den Client übergeben \] wird. Der Client gibt dann den Arbeitsspeicher frei. Diese Technik ermöglicht es dem Stub, den Server aufzurufen, ohne im Voraus zu wissen, wie viele Daten zurückgegeben werden.

    Dieses Programm ermöglicht es dem Benutzer auch, entweder für UNICODE oder ANSI zu kompilieren.

Alle Quelldateien und Makefiles für diese Programme befinden sich im Plattform-SDK.

Grundlegende Informationen zur ENTWICKLUNG von RPC-Anwendungen und einfachere Beispiele finden Sie in den [Tutorialthemen.](tutorial.md)

 

 
