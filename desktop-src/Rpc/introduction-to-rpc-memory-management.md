---
title: Einführung in die RPC-Speicherverwaltung
description: Einführung in die Speicherverwaltung für Remote Prozedur Aufrufe (RPC).
ms.assetid: 3474d79c-93ef-4221-b9ea-9173978e2929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ac4b6aecb2fd78448ebe31c72587fafb8f6fde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316064"
---
# <a name="introduction-to-rpc-memory-management"></a><span data-ttu-id="40f78-103">Einführung in die RPC-Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="40f78-103">Introduction to RPC Memory Management</span></span>

<span data-ttu-id="40f78-104">Im Zusammenhang mit RPC umfasst die Speicherverwaltung Folgendes:</span><span class="sxs-lookup"><span data-stu-id="40f78-104">In the context of RPC, memory management involves:</span></span>

-   <span data-ttu-id="40f78-105">Zuweisen und Aufheben der Zuordnung des Speichers, der zum Simulieren eines einzelnen konzeptionellen Adressraums zwischen dem Client und dem Server in den unterschiedlichen Adressräumen der Client-und Serverthreads benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="40f78-105">Allocating and deallocating the memory needed to simulate a single conceptual address space between the client and the server in the different address spaces of the client and server's threads.</span></span>
-   <span data-ttu-id="40f78-106">Ermitteln der Softwarekomponente, die für die Verwaltung des Arbeitsspeichers zuständig ist – der Anwendung oder dem von der Mitte generierten Stub.</span><span class="sxs-lookup"><span data-stu-id="40f78-106">Determining which software component is responsible for managing memory — the application or the MIDL-generated stub.</span></span>
-   <span data-ttu-id="40f78-107">Auswählen von "Mittel l"-Attributen, die sich auf die Speicherverwaltung auswirken: Direktionale Attribute, Zeiger Attribute, Array Attribute und die ACF-Attribute \[ [Byte \_ Anzahl](/windows/desktop/Midl/byte-count) \] , \[ [zuordnen](/windows/desktop/Midl/allocate) \] und \[ [Aktivierung \_ ](/windows/desktop/Midl/enable-allocate) \] von Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="40f78-107">Selecting MIDL attributes that affect memory management: directional attributes, pointer attributes, array attributes, and the ACF attributes \[ [byte\_count](/windows/desktop/Midl/byte-count)\], \[ [allocate](/windows/desktop/Midl/allocate)\], and \[ [enable\_allocate](/windows/desktop/Midl/enable-allocate)\].</span></span>

<span data-ttu-id="40f78-108">Wenn ein Programm eine Funktion oder Prozedur im Adressraum aufruft, ist die Speicherverwaltung einfacher als in einer verteilten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="40f78-108">When a program calls a function or procedure in its address space, memory management is more straightforward than in a distributed application.</span></span> <span data-ttu-id="40f78-109">Um dies zu veranschaulichen, stellt das folgende Diagramm eine binäre Struktur dar.</span><span class="sxs-lookup"><span data-stu-id="40f78-109">To illustrate, the following diagram depicts a binary tree.</span></span> <span data-ttu-id="40f78-110">Um diese Datenstruktur an eine Prozedur im Adressraum zu übergeben, übergibt ein Programm einfach einen Zeiger an den Stamm der Struktur.</span><span class="sxs-lookup"><span data-stu-id="40f78-110">To pass this data structure to a procedure in its address space, a program simply passes a pointer to the root of the tree.</span></span>

![eine binäre Struktur mit Zeigern auf Strukturdaten, die im Stamm der Struktur abgelegt sind.](images/bintree.png)

<span data-ttu-id="40f78-112">Client-/Server-RPC-Anwendungen nutzen Daten über zwei verschiedene Speicherplätze hinweg gemeinsam.</span><span class="sxs-lookup"><span data-stu-id="40f78-112">Client/server RPC applications share data across two different memory spaces.</span></span> <span data-ttu-id="40f78-113">Diese Speicherplätze können sich auf demselben Computer befinden oder nicht.</span><span class="sxs-lookup"><span data-stu-id="40f78-113">These memory spaces may or may not be on the same computer.</span></span> <span data-ttu-id="40f78-114">Der Client und der Server haben in beiden Fällen keinen direkten Zugriff auf den Arbeitsspeicher Bereich der anderen.</span><span class="sxs-lookup"><span data-stu-id="40f78-114">Either way, the client and server have no direct access to each other's memory space.</span></span> <span data-ttu-id="40f78-115">RPC hängt von der Fähigkeit ab, den Adressraum des Client Programms im Adressraum des Server Programms zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="40f78-115">RPC depends on the ability to simulate the client program's address space in the server program's address space.</span></span> <span data-ttu-id="40f78-116">Außerdem müssen Daten, einschließlich neuer und geänderter Daten, vom Server in den Client Speicher zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="40f78-116">It must also return data, including new and changed data, from the server to the client memory.</span></span>

<span data-ttu-id="40f78-117">In Fällen wie der binär Struktur, die im vorangehenden Diagramm dargestellt ist, reicht es nicht aus, einen Zeiger auf den Stamm Knoten an eine Remote Prozedur zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="40f78-117">In cases such as the binary tree depicted in the preceding diagram, it is not sufficient to pass a pointer to the root node to a remote procedure.</span></span> <span data-ttu-id="40f78-118">Entweder das Programm oder die Stub muss die gesamte Struktur an den Adressbereich des Servers übergeben, damit das Remote Verfahren darauf angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="40f78-118">Either the program or the stubs must pass the entire tree to the server's address space for the remote procedure to operate on it.</span></span>

 

 