---
description: SSPI-Optionen für verteilte Anwendungen
ms.assetid: e67cc054-7e48-43e7-a4b0-d1d90e9511f2
title: SSPI-Optionen für verteilte Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdfeef5cb52494c50b8b16911f70de238a7a86493297ec59bf6d46637810bf26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118916790"
---
# <a name="sspi-options-for-distributed-applications"></a>SSPI-Optionen für verteilte Anwendungen

Entwickler haben viele Optionen zum Erstellen verteilter Anwendungen. [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) stellt eine Abstraktionsschicht zwischen Protokollen auf Anwendungsebene und [*Sicherheitsprotokollen*](../secgloss/s-gly.md)bereit. Anwendungen können die SSPI-Sicherheitsprotokolle auf verschiedene Weise nutzen:

-   Rufen Sie SSPI-Routinen direkt auf (für herkömmliche, socketbasierte Anwendungen).

    Die Routinen verwenden Anforderungs-/Antwortnachrichten, um das [*Anwendungsprotokoll*](../secgloss/a-gly.md) zu implementieren, das sicherheitsbezogene SSPI-Daten enthält.

-   Verwenden Sie COM, um Sicherheitsoptionen aufzurufen, die mithilfe von authentifizierten RPC- und SSPI-Werten auf niedrigeren Ebenen implementiert werden.

    Diese Anwendungen rufen SSPI-Funktionen nicht direkt auf.

-   Verwenden Sie [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (WinSock) mit der erweiterten WinSock-Schnittstelle, um Transportanbietern die Verwendung von Sicherheitsfeatures zu ermöglichen.

    Dieser Ansatz integriert den [*Sicherheitsunterstützungsanbieter (Security Support Provider,*](../secgloss/s-gly.md) SSP) in den Netzwerkstapel und bietet sowohl Sicherheits- als auch Transportdienste über eine gemeinsame Schnittstelle.

-   Verwenden Sie die [Windows-Interneterweiterungs-API](../wininet/portal.md) (WinInet) und eine Schnittstelle, die für die Unterstützung von Internetsicherheitsprotokollen wie dem [*ssl-Protokoll (Secure Sockets Layer)*](../secgloss/s-gly.md) entwickelt wurde.

    Anwendungen verwenden die SSPI-Schnittstelle zum Sicherheitsanbieter [Secure Channel](secure-channel.md) (Schannel), um WinInet-Sicherheit zu implementieren. Schannel ist die Microsoft-Implementierung von SSL.

Mehrere SSPI-Funktionen geben Zeitstempel zurück, die die Lebensdauer verschiedener Objekte darstellen. [*Sicherheitspakete*](../secgloss/s-gly.md) können Zeit beibehalten und Zeitstempel auf unterschiedliche Weise bereitstellen, aber die Verwendung von Ortszeit vereinfacht die Arbeit von Anwendungen, die SSPI-Funktionen verwenden.

 

 
