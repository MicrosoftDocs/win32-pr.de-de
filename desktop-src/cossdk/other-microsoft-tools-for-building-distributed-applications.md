---
description: Weitere Microsoft-Tools zum entwickeln verteilter Anwendungen
ms.assetid: 518ca5b5-4285-4d69-abfe-bf6444a1deb5
title: Weitere Microsoft-Tools zum entwickeln verteilter Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d65bd7c61a73bedb9463e8558415c7b27fe04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346648"
---
# <a name="other-microsoft-tools-for-building-distributed-applications"></a><span data-ttu-id="db69d-103">Weitere Microsoft-Tools zum entwickeln verteilter Anwendungen</span><span class="sxs-lookup"><span data-stu-id="db69d-103">Other Microsoft Tools for Building Distributed Applications</span></span>

<span data-ttu-id="db69d-104">Zusätzlich zu den Tools in com+ bietet Microsoft die folgenden Tools zum unterstützen des Entwicklers bei der Erstellung verteilter Anwendungen:</span><span class="sxs-lookup"><span data-stu-id="db69d-104">In addition to the tools in COM+, Microsoft provides the following tools to assist the developer in creating distributed applications:</span></span>

-   <span data-ttu-id="db69d-105">Microsoft Data Access Components (MDAC).</span><span class="sxs-lookup"><span data-stu-id="db69d-105">Microsoft Data Access Components (MDAC).</span></span> <span data-ttu-id="db69d-106">Microsoft bietet mehrere Möglichkeiten zum Abrufen von Daten aus einer Vielzahl von Quellen.</span><span class="sxs-lookup"><span data-stu-id="db69d-106">Microsoft provides several avenues for retrieving data from a myriad of sources.</span></span> <span data-ttu-id="db69d-107">OLE DB bietet z. b. eine Reihe von COM-Schnittstellen zum Entwickeln von Datenbankkomponenten.</span><span class="sxs-lookup"><span data-stu-id="db69d-107">For example, OLE DB offers a set of COM interfaces for building database components.</span></span> <span data-ttu-id="db69d-108">Die Schnittstellen sind so definiert, dass Datenanbieter unterschiedliche Unterstützungs Ebenen implementieren können, basierend auf den Funktionen des zugrunde liegenden Datenspeicher.</span><span class="sxs-lookup"><span data-stu-id="db69d-108">The interfaces are defined so that data providers can implement different levels of support, based on the capabilities of the underlying data store.</span></span> <span data-ttu-id="db69d-109">Da OLE DB com-basiert ist, kann es problemlos erweitert werden, und Erweiterungen werden als neue Schnittstellen implementiert.</span><span class="sxs-lookup"><span data-stu-id="db69d-109">Because OLE DB is COM-based, it can easily be extended, and extensions are implemented as new interfaces.</span></span> <span data-ttu-id="db69d-110">OLE DB umfasst auch eine Programmierschnittstelle auf Anwendungsebene mit dem Namen ActiveX Data Objects (ADO).</span><span class="sxs-lookup"><span data-stu-id="db69d-110">OLE DB also includes an application-level programming interface, called ActiveX Data Objects (ADO).</span></span> <span data-ttu-id="db69d-111">ADO stellt duale Schnittstellen zur Verfügung, sodass es problemlos von Skriptsprachen sowie Microsoft Visual C++, Visual Basic und anderen Entwicklertools verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="db69d-111">ADO exposes dual interfaces, so it can easily be used from scripting languages as well as Microsoft Visual C++, Visual Basic, and other developer tools.</span></span>

    > [!Note]  
    > <span data-ttu-id="db69d-112">Entwickler können auch eine generische, Anbieter neutrale API verwenden, wie z. b. die Microsoft Open Database Connectivity (ODBC)-API (Application Programming Interface).</span><span class="sxs-lookup"><span data-stu-id="db69d-112">Developers can also choose to use a generic, vendor-neutral API such as the Microsoft Open Database Connectivity (ODBC) application programming interface (API).</span></span> <span data-ttu-id="db69d-113">Die ODBC-API ist eine Schnittstelle der Programmiersprache C für den Zugriff auf Daten in einem DBMS mithilfe von Structured Query Language (SQL).</span><span class="sxs-lookup"><span data-stu-id="db69d-113">The ODBC API is a C language interface for accessing data in a DBMS by using Structured Query Language (SQL).</span></span> <span data-ttu-id="db69d-114">Ein ODBC-Treiber-Manager stellt die Programmierschnittstelle und Laufzeitkomponenten zum Auffinden von DBMS-spezifischen Treibern bereit.</span><span class="sxs-lookup"><span data-stu-id="db69d-114">An ODBC driver manager provides the programming interface and run-time components to locate DBMS-specific drivers.</span></span> <span data-ttu-id="db69d-115">ODBC-Treiber, die in der Regel vom DBMS-Anbieter bereitgestellt werden, übersetzen generische Aufrufe aus dem ODBC-Treiber-Manager in Aufrufe der systemeigenen Datenzugriffs Methode.</span><span class="sxs-lookup"><span data-stu-id="db69d-115">ODBC drivers, typically supplied by the DBMS vendor, translate generic calls from the ODBC driver manager into calls to the native data access method.</span></span> <span data-ttu-id="db69d-116">Der Hauptvorteil der Verwendung der ODBC-API besteht darin, dass Sie nur eine API erlernen müssen, um auf eine große Bandbreite von DBMSs zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="db69d-116">The primary advantage of using the ODBC API is that you need to learn only one API to access a wide range of DBMSs.</span></span>

     

-   <span data-ttu-id="db69d-117">Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="db69d-117">Microsoft SQL Server.</span></span> <span data-ttu-id="db69d-118">Zusätzlich zur Bereitstellung eines robusten und eloquenten relationalen Datenbanksystems können Microsoft SQL Server eine verteilte Anwendung mit Verbindungspooling und Sicherheit bereitstellen, die in das Windows-Sicherheitsmodell integriert werden können.</span><span class="sxs-lookup"><span data-stu-id="db69d-118">In addition to providing a robust and eloquent relational database system, Microsoft SQL Server can provide a distributed application with connection pooling and security that can integrate with the Windows security model.</span></span>

-   <span data-ttu-id="db69d-119">COM-Transaktions Integration (com Transaction Integration, COMTI)</span><span class="sxs-lookup"><span data-stu-id="db69d-119">COM Transaction Integration (COMTI).</span></span> <span data-ttu-id="db69d-120">COMTI kann verwendet werden, um Main Frame-Systeme in Windows-Systeme zu integrieren, einschließlich com+-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="db69d-120">COMTI can be used to integrate mainframe systems into Windows systems, including COM+ applications.</span></span> <span data-ttu-id="db69d-121">COMTI verwendet Standard Kommunikationsprotokolle (z. b. lu 6,2) für die Kommunikation zwischen Windows-Computern und Main Frame und Minicomputers.</span><span class="sxs-lookup"><span data-stu-id="db69d-121">COMTI uses standard communication protocols (for example, LU 6.2) for communicating between Windows computers and mainframe and minicomputers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db69d-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="db69d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db69d-123">Com+-Entwurfs Annahmen und-Prinzipien</span><span class="sxs-lookup"><span data-stu-id="db69d-123">COM+ Design Assumptions and Principles</span></span>](com--design-assumptions-and-principles.md)
</dt> <dt>

[<span data-ttu-id="db69d-124">Entwerfen der com+-Anwendung mithilfe von UML</span><span class="sxs-lookup"><span data-stu-id="db69d-124">Designing the COM+ Application Using UML</span></span>](designing-the-com--application-using-uml.md)
</dt> <dt>

[<span data-ttu-id="db69d-125">Allgemeine Entwurfs Tipps für die Verwendung von com+</span><span class="sxs-lookup"><span data-stu-id="db69d-125">General Design Tips for Using COM+</span></span>](general-design-tips-for-using-com-.md)
</dt> <dt>

[<span data-ttu-id="db69d-126">Optimieren von Interaktionen mit der com+-Geschäftslogik Ebene</span><span class="sxs-lookup"><span data-stu-id="db69d-126">Optimizing Interactions with the COM+ Business Logic Tier</span></span>](optimizing-interactions-with-the-com--business-logic-tier.md)
</dt> </dl>

 

 



