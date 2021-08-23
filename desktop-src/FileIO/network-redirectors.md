---
description: Beschreibt die Funktionalität eines Netzwerk-Redirectors.
ms.assetid: 3cf36f88-b282-4f75-84fe-8106fea66825
title: Netzwerkumleitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed44bb8479c4aea5056b667688cb27ae0f1fe1ebf4f43d066a49143d5bfeadc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951079"
---
# <a name="network-redirectors"></a>Netzwerkumleitung

Ein Netzwerk-Redirector ist ein Dateisystemtreiber (File System Driver, FSD), der wie folgt funktioniert:

-   Als Client in einem Netzwerk-E/A-Vorgang durch Senden von E/A-Anforderungen an Server und Verarbeiten der Antworten von den Servern.
-   Als Server in einem Netzwerk-E/A-Vorgang, indem E/A-Anforderungen von Servern empfangen und die Anforderungen verarbeitet werden.

Er führt die gesamte Low-Level-Interaktion mit dem Server durch, um den von der Anwendung bereitgestellten Dateinamen mit dem Speicherort der Ressource auf dem Remoteserver aufzulösen. Auf diese Weise ermöglicht der Redirector der Anwendung den Zugriff auf und die Bearbeitung von Ressourcen auf Remoteservern, als ob sie sich auf dem lokalen Computer befinden würden.

Umleitungen werden vollständig im Kernelmodus ausgeführt. Dies bietet die folgenden Leistungsvorteile gegenüber Alternativen im Benutzermodus:

-   Sie kann mit Kernelmodus-FSDs interagieren, die auf dem Server ausgeführt werden, z. B. der Server-FSD, ohne dass Kontextwechsel zwischen Benutzern und Kernel-zu-Benutzer-Modus erforderlich sind.
-   Sie kann im Kernelmodus mit dem Cache-Manager auf dem Server interagieren, um E/A-Daten zwischenzuspeichern, die der Servercache-Manager auf dem Client sendet.
-   API-Funktionen, die für Remote-E/A-Anforderungen angepasst wurden, und Änderungen an den Standarddatei-E/A-Funktionen zur Bereitstellung dieser Funktionalität sind nicht erforderlich.

 

 



