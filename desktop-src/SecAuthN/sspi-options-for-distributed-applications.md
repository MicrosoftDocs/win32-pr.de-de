---
description: SSPI-Optionen für verteilte Anwendungen
ms.assetid: e67cc054-7e48-43e7-a4b0-d1d90e9511f2
title: SSPI-Optionen für verteilte Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7729b3c479c69b674120fe1fc9827f5edfd878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861883"
---
# <a name="sspi-options-for-distributed-applications"></a>SSPI-Optionen für verteilte Anwendungen

Entwickler haben viele Optionen zum entwickeln verteilter Anwendungen. Die [*Security Support Provider-Schnittstelle*](../secgloss/s-gly.md) (SSPI) bietet eine Abstraktions Ebene zwischen Protokollen auf Anwendungsebene und [*Sicherheitsprotokollen*](../secgloss/s-gly.md). Anwendungen können die SSPI-Sicherheitsprotokolle auf verschiedene Weise nutzen:

-   Direkte Aufrufe von SSPI-Routinen (für herkömmliche, socketbasierte Anwendungen).

    Die Routinen verwenden Anforderungs-/Antwort-Nachrichten, um das [*Anwendungsprotokoll*](../secgloss/a-gly.md) zu implementieren, das sicherheitsrelevante SSPI-Daten enthält.

-   Verwenden Sie com, um Sicherheitsoptionen aufzurufen, die mithilfe von authentifizierter RPC und SSPI auf niedrigeren Ebenen implementiert werden.

    Von diesen Anwendungen werden keine SSPI-Funktionen direkt aufgerufen.

-   Verwenden Sie [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (Winsock) mit der erweiterten Winsock-Schnittstelle, damit Transportanbieter Sicherheitsfeatures verwenden können.

    Bei diesem Ansatz wird der [*Security Support Provider*](../secgloss/s-gly.md) (SSP) in den Netzwerk Stapel integriert, und es werden Sicherheits-und Transportdienste über eine gemeinsame Oberfläche bereitstellt.

-   Verwenden Sie die [Windows Internet Extensions-API](../wininet/portal.md) (WinInet) und eine Schnittstelle, die für die Unterstützung von Internet Sicherheitsprotokollen wie dem [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL)-Protokoll konzipiert ist.

    Anwendungen verwenden die SSPI-Schnittstelle für den Sicherheitsanbieter [Secure Channel](secure-channel.md) (SChannel), um die WinInet-Sicherheit zu implementieren. SChannel ist die Microsoft-Implementierung von SSL.

Mehrere SSPI-Funktionen geben Zeitstempel zurück, die die Lebensdauer verschiedener Objekte darstellen. [*Sicherheitspakete*](../secgloss/s-gly.md) können Zeit in Anspruch nehmen und Zeitstempel auf unterschiedliche Weise bereitstellen, aber die lokale Zeit vereinfacht die Arbeit von Anwendungen, die SSPI-Funktionen verwenden.

 

 
