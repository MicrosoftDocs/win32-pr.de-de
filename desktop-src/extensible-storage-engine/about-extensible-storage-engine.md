---
description: 'Weitere Informationen finden Sie hier: Informationen zum Extensible Storage Engine'
title: Informationen zur Extensible Storage-Engine
TOCTitle: About Extensible Storage Engine
ms:assetid: 06d1526e-169d-4677-b409-2ed415287de6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269181(v=EXCHG.10)
ms:contentKeyID: 32765484
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 17e2277deaef54c04bf6a53a8464479fd67295a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958666"
---
# <a name="about-extensible-storage-engine"></a><span data-ttu-id="02e54-103">Informationen zur Extensible Storage-Engine</span><span class="sxs-lookup"><span data-stu-id="02e54-103">About Extensible Storage Engine</span></span>


<span data-ttu-id="02e54-104">_**Gilt für:** Exchange Server 2013 | Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="02e54-104">_**Applies to:** Exchange Server 2013 | Windows | Windows Server_</span></span>

## <a name="about-extensible-storage-engine"></a><span data-ttu-id="02e54-105">Informationen zur Extensible Storage-Engine</span><span class="sxs-lookup"><span data-stu-id="02e54-105">About Extensible Storage Engine</span></span>

<span data-ttu-id="02e54-106">Bei der Extensible Storage Engine (ESE) handelt es sich um eine Datenbank-Engine, die Informationen in einer logischen Sequenz speichert.</span><span class="sxs-lookup"><span data-stu-id="02e54-106">The extensible storage engine (ESE) is a database engine that stores information in a logical sequence.</span></span> <span data-ttu-id="02e54-107">Informationen können entweder sequenziell oder durch Zugriff auf definierte Indizes abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="02e54-107">Information can be retrieved either sequentially or by accessing defined indices.</span></span> <span data-ttu-id="02e54-108">Aktualisierungen der Datenbank werden mit einer Transaktion implementiert, um sichere Vorgänge sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="02e54-108">Updates to the database are implemented with a transaction in order to ensure secure operations.</span></span> <span data-ttu-id="02e54-109">ESE ermöglicht den gleichzeitigen Zugriff auf mehrere Datenbanken, einschließlich der Datenbanken für Transaktionsprotokoll Dateien, die für die Systemwiederherstellung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="02e54-109">ESE enables simultaneous access to multiple databases, including transaction-log file databases that can be used for system recovery.</span></span> <span data-ttu-id="02e54-110">ESE ist für große oder kleine Anwendungen skalierbar.</span><span class="sxs-lookup"><span data-stu-id="02e54-110">ESE is scalable to large or small applications.</span></span> <span data-ttu-id="02e54-111">Die folgenden Features sind für die ESE-Anwendungsprogrammierschnittstelle (Application Programming Interface, API) verfügbar:</span><span class="sxs-lookup"><span data-stu-id="02e54-111">The following features are available with the ESE application programming interface (API):</span></span>

  - <span data-ttu-id="02e54-112">Sicherung und Wiederherstellung: eine Anwendung kann konsistente Kopien des Daten Zustands erstellen, während Sie online ist, und den Daten Zustand Aktiv ändern.</span><span class="sxs-lookup"><span data-stu-id="02e54-112">Backup and restore: An application can make consistent copies of the data state while it is on-line and actively modifying data state.</span></span>

  - <span data-ttu-id="02e54-113">Cursor Navigation: die Anwendung kann mit dem Cursor navigieren, um entweder sequenziell oder mithilfe von Indizes auf Daten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="02e54-113">Cursor Navigation: The application can navigate with the cursor to access data either sequentially or by using indices.</span></span>

  - <span data-ttu-id="02e54-114">Database: eine Sammlung von Tabellen, die als einzelne Einheit gesichert und wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="02e54-114">Database: A collection of tables that are backed up and restored as a single unit.</span></span>

  - <span data-ttu-id="02e54-115">Protokollierung und Wiederherstellung von Abstürzen: die ESE-API stellt sicher, dass die Anwendungs definierte Datenkonsistenz auch bei einem Systemabsturz berücksichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="02e54-115">Logging and crash recovery: The ESE API ensures that application-defined data consistency is honored even in the event of a system crash.</span></span>

  - <span data-ttu-id="02e54-116">Tables: die grundlegende Struktur der ESE-Datenbank, die zum Speichern von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="02e54-116">Tables: The fundamental structure of the ESE database that is used to store data.</span></span>

  - <span data-ttu-id="02e54-117">Transaktion: das ESE-Datenbankmodul stellt atomarische, isolierte, dauerhafte (ACID) Transaktionen bereit, die es Anwendungen ermöglichen, Daten nur aus zuverlässigen Daten Zuständen abzurufen, und behält die Datenkonsistenz bei einer unerwarteten Beendigung des Prozesses oder beim Herunterfahren des Systems bei.</span><span class="sxs-lookup"><span data-stu-id="02e54-117">Transaction: The ESE database engine provides Atomic Consistent Isolated Durable (ACID) transactions that allow applications to retrieve data only from reliable data states and maintains data consistency in the event of an unexpected process termination or system shutdown.</span></span>

  - <span data-ttu-id="02e54-118">Skalierbar: die Anwendung kann Datenbanken mit einer Größe von 100 GB oder bis zu 1 MB erstellen.</span><span class="sxs-lookup"><span data-stu-id="02e54-118">Scalable: The application can create databases as large as 100 GB or as small as 1MB.</span></span>

