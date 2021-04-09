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
# <a name="network-redirectors"></a><span data-ttu-id="8917d-103">Netzwerkredirectors</span><span class="sxs-lookup"><span data-stu-id="8917d-103">Network Redirectors</span></span>

<span data-ttu-id="8917d-104">Ein Netzwerkredirector ist ein Dateisystem Treiber (oder eine voll qualifizierte Datei), der wie folgt funktioniert:</span><span class="sxs-lookup"><span data-stu-id="8917d-104">A network redirector is a file system driver (or FSD) that functions in the following manner:</span></span>

-   <span data-ttu-id="8917d-105">Als Client in einem Netzwerk-e/a-Vorgang durch Senden von e/a-Anforderungen an Server und Verarbeiten der Antworten von den Servern.</span><span class="sxs-lookup"><span data-stu-id="8917d-105">As a client in a network I/O operation by sending I/O requests to servers and processing the responses from the servers.</span></span>
-   <span data-ttu-id="8917d-106">Als Server in einem Netzwerk-e/a-Vorgang durch empfangen von e/a-Anforderungen von Servern und Verarbeiten der Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="8917d-106">As a server in a network I/O operation by receiving I/O requests from servers and processing the requests.</span></span>

<span data-ttu-id="8917d-107">Sie führt die gesamte Interaktion auf niedriger Ebene mit dem Server durch, wobei der von der Anwendung bereitgestellte Dateiname mit dem Speicherort der Ressource auf dem Remote Server aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="8917d-107">It performs all of the low-level interaction with the server in resolving the file name provided by the application with the location of the resource on the remote server.</span></span> <span data-ttu-id="8917d-108">Auf diese Weise ermöglicht der Redirector der Anwendung den Zugriff auf und das Bearbeiten von Ressourcen auf Remote Servern, als ob Sie sich auf dem lokalen Computer befinden.</span><span class="sxs-lookup"><span data-stu-id="8917d-108">In this way, the redirector enables the application to access and manipulate resources on remote servers as if they were located on the local machine.</span></span>

<span data-ttu-id="8917d-109">Redirectors arbeiten vollständig im Kernel Modus.</span><span class="sxs-lookup"><span data-stu-id="8917d-109">Redirectors operate entirely within kernel mode.</span></span> <span data-ttu-id="8917d-110">Dies bietet die folgenden Leistungsvorteile im Vergleich zu benutzermodusalternativen:</span><span class="sxs-lookup"><span data-stu-id="8917d-110">This provides the following performance advantages over user-mode alternatives:</span></span>

-   <span data-ttu-id="8917d-111">Die Anwendung kann mit auf dem Server ausgeführt werden, die auf dem Server ausgeführt wird, z. b. auf der FSD des Servers, ohne dass der Benutzer-zu-Kernel-Modus und Kontextwechsel zwischen Kernel und Benutzermodus erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8917d-111">It can interact with kernel-mode FSDs running on the server, such as the server FSD, without the need for user-to-kernel mode and kernel-to-user mode context switches.</span></span>
-   <span data-ttu-id="8917d-112">Sie kann im Kernel Modus mit dem Cache-Manager auf dem Server interagieren, um e/a-Daten zwischenzuspeichern, die vom Server Cache-Manager auf dem Client gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="8917d-112">It can interact in kernel mode with the cache manager on the server to cache I/O data that the server cache manager sends on the client.</span></span>
-   <span data-ttu-id="8917d-113">API-Funktionen, die für Remote-e/a-Anforderungen erstellt wurden, und Änderungen an den standardmäßigen Datei-e/a-Funktionen, um diese Funktionalität bereitzustellen, sind nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8917d-113">API functions custom-made for remote I/O requests, and changes to the standard file I/O functions to provide this functionality, are not necessary.</span></span>

 

 



