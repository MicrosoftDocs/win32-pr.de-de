---
title: Details zur EAP-Implementierung
description: Zugriffspunkte (APS), z. b. RAS (RAS), interagieren mit EAP-Implementierungen durch die Verwendung von Funktionsaufrufen, die von der EAP-dll von Drittanbietern exportiert werden müssen.
ms.assetid: 85775c03-7538-41a1-9f83-42e71025a79c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41115b16d843b0c1b087eac1c348a0491df1173a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314883"
---
# <a name="eap-implementation-details"></a>Details zur EAP-Implementierung

Zugriffspunkte (APS), z. b. RAS (RAS), interagieren mit EAP-Implementierungen durch die Verwendung von Funktionsaufrufen, die von der EAP-dll von Drittanbietern exportiert werden müssen. Das heißt, dass EAP eine Anbieter-API ist, was bedeutet, dass Plug-ins oder DLLs Code implementieren, um einen EAP-Anbieter zu werden, aber nicht die EAP-APIs selbst aufrufen dürfen. Beispielsweise erstellt ein Programmierer einer EAP-DLL Code für eine EAP-Initialisierungs Routine und platziert diesen Code in der vordefinierten EAP-Funktion [**raseapinitialize**](/previous-versions/windows/desktop/legacy/aa363527(v=vs.85)). Dann ruft der AP-Verbindungs-Manager zur Laufzeit die **raseapinitialize** -Funktion auf, die den Code enthält, um die EAP-Implementierung zu initialisieren.

In den folgenden Themen wird diese Interaktion ausführlich erläutert:

-   [Zugriffspunkt Initialisierung von EAP](ras-initialization-of-eap.md)
-   [Initialisierung des Authentifizierungs Protokolls](authentication-protocol-initialization.md)
-   [Interaktion zwischen Zugriffspunkt und Authentifizierungsprotokoll](ras-and-authentication-protocol-interaction-during-authentication.md)
-   [Abschluss der Authentifizierungs Sitzung](completion-of-the-authentication-session.md)

 

 