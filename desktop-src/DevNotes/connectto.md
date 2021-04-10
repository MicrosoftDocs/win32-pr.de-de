---
description: HKLM \\ Software \\ Microsoft \\ MSSQLSERVER- \\ Client.
ms.assetid: d6eb774b-d7ae-4f51-9947-90fb176e9acf
title: ConnectTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b1f77fc90bca467e90a3c3b7f407b8ba6d33d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041405"
---
# <a name="connectto"></a><span data-ttu-id="22f5e-103">ConnectTo</span><span class="sxs-lookup"><span data-stu-id="22f5e-103">ConnectTo</span></span>

<span data-ttu-id="22f5e-104">**HKLM \\ Software \\ Microsoft \\ MSSQLSERVER- \\ Client**</span><span class="sxs-lookup"><span data-stu-id="22f5e-104">**HKLM\\SOFTWARE\\Microsoft\\MSSQLServer\\Client**</span></span>

## <a name="description"></a><span data-ttu-id="22f5e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22f5e-105">Description</span></span>

<span data-ttu-id="22f5e-106">Der **ConnectTo** -Unterschlüssel speichert Verbindungsinformationen für Windows-basierte Clients, die eine Verbindung mit Instanzen der Microsoft SQL Server Datenbank-Engine herstellen.</span><span class="sxs-lookup"><span data-stu-id="22f5e-106">The **ConnectTo** subkey stores connection information for Windows-based clients that connect to instances of the Microsoft SQL Server database engine.</span></span> <span data-ttu-id="22f5e-107">Registrierungseinträge in diesem Unterschlüssel sind vom Datentyp reg \_ SZ, und ihre Werte geben die Net-Library an, die zum Herstellen einer Verbindung mit der Instanz verwendet werden sollen, sowie Netzwerk spezifische Parameter.</span><span class="sxs-lookup"><span data-stu-id="22f5e-107">Registry entries in this subkey are of data type REG\_SZ, and their values specify the Net-Library to use for connecting to the instance, as well as any network-specific parameters.</span></span>

<span data-ttu-id="22f5e-108">Die in diesem Unterschlüssel gespeicherten Verbindungsinformationen werden vom OLE DB Anbieter für SQL Server, dem SQL Server ODBC-Treiber oder dem SQL Server DB-Library Dynamic Link Library (dll) gelesen.</span><span class="sxs-lookup"><span data-stu-id="22f5e-108">The connection information stored in this subkey is read by the OLE DB Provider for SQL Server, the SQL Server ODBC driver, or the SQL Server DB-Library dynamic-link library (DLL).</span></span>

## <a name="change-method"></a><span data-ttu-id="22f5e-109">Methode ändern</span><span class="sxs-lookup"><span data-stu-id="22f5e-109">Change Method</span></span>

<span data-ttu-id="22f5e-110">Sie sollten die Einträge in diesem Unterschlüssel nicht mithilfe des Registrierungs-Editors ändern.</span><span class="sxs-lookup"><span data-stu-id="22f5e-110">You should not modify entries in this subkey by using the registry editor.</span></span> <span data-ttu-id="22f5e-111">Verwenden Sie das Netzwerk Hilfsprogramm SQL Server Client, um den Server Namen und die Verbindungsinformationen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="22f5e-111">Use the SQL Server Client Network Utility to configure server name and connection information.</span></span> <span data-ttu-id="22f5e-112">Weitere Anweisungen finden Sie unter SQL Server Hilfe zum Client Netzwerk Hilfsprogramm.</span><span class="sxs-lookup"><span data-stu-id="22f5e-112">See SQL Server Client Network Utility Help for further instructions.</span></span>

## <a name="notes"></a><span data-ttu-id="22f5e-113">Notizen</span><span class="sxs-lookup"><span data-stu-id="22f5e-113">Notes</span></span>

-   <span data-ttu-id="22f5e-114">Der Unterschlüssel **ConnectTo** wird vom OLE DB Anbieter für SQL Server, vom SQL Server ODBC-Treiber und von der SQL Server DB-Library dll verwendet.</span><span class="sxs-lookup"><span data-stu-id="22f5e-114">The **ConnectTo** subkey is used by the OLE DB Provider for SQL Server, the SQL Server ODBC Driver, and the SQL Server DB-Library DLL.</span></span> <span data-ttu-id="22f5e-115">Einträge in diesem Unterschlüssel identifizieren, welche Net-Library diese Datenzugriffs-API-Komponenten aufrufen.</span><span class="sxs-lookup"><span data-stu-id="22f5e-115">Entries in this subkey identify which Net-Library these data access application programming interface (API) components call.</span></span>
-   <span data-ttu-id="22f5e-116">Net-Libraries sind SQL Server Komponenten, die die Datenzugriffs-API-Komponenten vor den Details der Verwendung verschiedener IPC-Methoden (Interprocess Communication) verwenden, um mit einem instanzess des SQL Server Datenbank-Engine zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="22f5e-116">Net-Libraries are SQL Server components that shield the data access API components from the details of using different Interprocess Communication (IPC) methods to communicate with an instancess of the SQL Server database engine.</span></span>
-   <span data-ttu-id="22f5e-117">Das nicht ordnungsgemäße Aktualisieren des **ConnectTo** -unter Schlüssels verhindert möglicherweise, dass Anwendungen eine Verbindung mit einer Instanz der SQL Server Datenbank-Engine herstellen.</span><span class="sxs-lookup"><span data-stu-id="22f5e-117">Improperly updating the **ConnectTo** subkey might prevent applications from successfully connecting to an instance of the SQL Server database engine.</span></span>

 

 



