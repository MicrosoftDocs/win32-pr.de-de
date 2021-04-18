---
title: Beispiele (RPC)
description: Beispiele zur Veranschaulichung von RPC-Konzepten (Remote Prozedur Aufruf).
ms.assetid: d5db3085-6df0-4539-a605-d60055f4f4ec
keywords:
- Remote Prozedur Aufruf RPC, Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e6a814d78afbfc7fefa979c890cbbb8c3d4ce0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106340745"
---
# <a name="examples-rpc"></a>Beispiele (RPC)

Das Platform Software Development Kit (SDK) enthält Beispiele, die eine Vielzahl von Remote Prozedur Aufruf-Konzepten (RPC) veranschaulichen, wie im folgenden dargestellt:

-   Asyncrpc veranschaulicht die Struktur einer RPC-Anwendung, die asynchrone Remote Prozedur Aufrufe verwendet. Außerdem werden verschiedene Benachrichtigungs Methoden für den Abschluss des Aufrufes veranschaulicht.
-   Cluuid veranschaulicht die Verwendung der Client-Objekt-UUID, um es einem Client zu ermöglichen, aus mehreren Implementierungen einer Remote Prozedur auszuwählen.
-   Das Datenverzeichnis enthält vier Programme: dunion veranschaulicht diskriminierte (nicht gekapselte) Unions; "INOUT" veranschaulicht [ \[ in \] ](../midl/in.md)-, [ \[ out \] ](../midl/out-idl.md) -Parameter; Repas zeigt die [Darstellung \_ als](/windows/desktop/Midl/represent-as) Attribut an. Xmit veranschaulicht das über [tragen \_ als](/windows/desktop/Midl/transmit-as) -Attribut.
-   Dynetpt veranschaulicht, wie eine Client Anwendung über dynamische Endpunkte eine Verbindung mit dem Server verwaltet.
-   Das Verzeichnis filerep enthält vier Beispiele, die veranschaulichen, wie Entwickler einen einfachen Datei Replikations Dienst, einen Datei Replikations Dienst für mehrere Benutzer, einen Dienst zur Unterstützung von Sicherheitsfunktionen und einen Dienst mit asynchronen RPC-Pipes schreiben können.
-   Das Handles-Verzeichnis enthält die drei Programme Auto, cxhndl, rdef, die die [automatische \_ Handhabung](/windows/desktop/Midl/auto-handle), das \[ Kontext \_ handle \] und generische (benutzerdefinierte) Handles veranschaulichen.
-   Hello ist eine Client/Server-Implementierung von "Hello, World".
-   Das Pickle-Verzeichnis enthält zwei Programme: picklp veranschaulicht die Serialisierung von Daten Prozeduren. Picklt veranschaulicht die Serialisierung des Datentyps. Beide Programme verwenden die Attribute [ \[ Codieren \] ](../midl/encode.md) und [ \[ decodieren \] ](../midl/decode.md) .
-   Pipes veranschaulicht die Verwendung des pipetypkonstruktors.
-   Rpcsvc veranschaulicht die Implementierung eines Dienstanbieter mit RPC.
-   StrOut veranschaulicht, wie Arbeitsspeicher auf einem Server für ein zweidimensionales Objekt (ein Array von Zeigern) belegt und als \[ nur-Out-Parameter an den Client zurückgegeben wird \] . Der Client gibt dann den Arbeitsspeicher frei. Diese Technik ermöglicht es dem Stub, den Server aufzurufen, ohne im Voraus zu wissen, wie viele Daten zurückgegeben werden.

    Dieses Programm ermöglicht es dem Benutzer auch, für Unicode oder ANSI zu kompilieren.

Alle Quelldateien und Makefiles für diese Programme befinden sich im Platform SDK.

Informationen zur grundlegenden Entwicklung von RPC-Anwendungen und einfacheren Beispielen finden Sie in den Themen zum [Tutorial](tutorial.md) .

 

 
