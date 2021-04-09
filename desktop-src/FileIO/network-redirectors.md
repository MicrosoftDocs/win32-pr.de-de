---
description: Beschreibt die Funktionalität eines Netzwerkredirector.
ms.assetid: 3cf36f88-b282-4f75-84fe-8106fea66825
title: Netzwerkredirectors
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce8c887cba779fe3f6aee9811819c6638d926f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868915"
---
# <a name="network-redirectors"></a>Netzwerkredirectors

Ein Netzwerkredirector ist ein Dateisystem Treiber (oder eine voll qualifizierte Datei), der wie folgt funktioniert:

-   Als Client in einem Netzwerk-e/a-Vorgang durch Senden von e/a-Anforderungen an Server und Verarbeiten der Antworten von den Servern.
-   Als Server in einem Netzwerk-e/a-Vorgang durch empfangen von e/a-Anforderungen von Servern und Verarbeiten der Anforderungen.

Sie führt die gesamte Interaktion auf niedriger Ebene mit dem Server durch, wobei der von der Anwendung bereitgestellte Dateiname mit dem Speicherort der Ressource auf dem Remote Server aufgelöst wird. Auf diese Weise ermöglicht der Redirector der Anwendung den Zugriff auf und das Bearbeiten von Ressourcen auf Remote Servern, als ob Sie sich auf dem lokalen Computer befinden.

Redirectors arbeiten vollständig im Kernel Modus. Dies bietet die folgenden Leistungsvorteile im Vergleich zu benutzermodusalternativen:

-   Die Anwendung kann mit auf dem Server ausgeführt werden, die auf dem Server ausgeführt wird, z. b. auf der FSD des Servers, ohne dass der Benutzer-zu-Kernel-Modus und Kontextwechsel zwischen Kernel und Benutzermodus erforderlich sind.
-   Sie kann im Kernel Modus mit dem Cache-Manager auf dem Server interagieren, um e/a-Daten zwischenzuspeichern, die vom Server Cache-Manager auf dem Client gesendet werden.
-   API-Funktionen, die für Remote-e/a-Anforderungen erstellt wurden, und Änderungen an den standardmäßigen Datei-e/a-Funktionen, um diese Funktionalität bereitzustellen, sind nicht erforderlich.

 

 



