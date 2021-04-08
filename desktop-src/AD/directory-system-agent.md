---
title: Verzeichnis System-Agent
description: Der Verzeichnis System-Agent (DSA) ist eine Sammlung von Diensten und Prozessen, die auf jedem Domänen Controller ausgeführt werden und Zugriff auf den Datenspeicher bietet.
ms.assetid: a921a822-6b2e-4a84-8112-0ae516443667
ms.tgt_platform: multiple
keywords:
- Verzeichnis System-Agent-Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df39d1670f6668f933c20bcd2b9a8771ce83ec56
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858155"
---
# <a name="directory-system-agent"></a><span data-ttu-id="4666e-104">Verzeichnis System-Agent</span><span class="sxs-lookup"><span data-stu-id="4666e-104">Directory System Agent</span></span>

<span data-ttu-id="4666e-105">Der [*Verzeichnis System-Agent*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) ist eine Sammlung von Diensten und Prozessen, die auf jedem Domänen Controller ausgeführt werden und Zugriff auf den Datenspeicher bietet.</span><span class="sxs-lookup"><span data-stu-id="4666e-105">The [*directory system agent*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) is a collection of services and processes that run on each domain controller and provides access to the data store.</span></span> <span data-ttu-id="4666e-106">Der Datenspeicher ist der physische Speicher der Verzeichnis Daten auf einer Festplatte.</span><span class="sxs-lookup"><span data-stu-id="4666e-106">The data store is the physical store of directory data located on a hard disk.</span></span> <span data-ttu-id="4666e-107">In Active Directory Domain Services ist das DSA Teil des Local System Authority (LSA)-Subsystems.</span><span class="sxs-lookup"><span data-stu-id="4666e-107">In Active Directory Domain Services, the DSA is part of the local system authority (LSA) subsystem.</span></span> <span data-ttu-id="4666e-108">Clients greifen mithilfe eines der folgenden Mechanismen, die von DSA unterstützt werden, auf das Verzeichnis zu:</span><span class="sxs-lookup"><span data-stu-id="4666e-108">Clients access the directory using one of the following mechanisms supported by the DSA:</span></span>

-   <span data-ttu-id="4666e-109">LDAP-Clients stellen eine Verbindung mit dem DSA mithilfe von LDAP (Lightweight Directory Access Protocol) her.</span><span class="sxs-lookup"><span data-stu-id="4666e-109">LDAP clients connect to the DSA using the Lightweight Directory Access Protocol (LDAP).</span></span> <span data-ttu-id="4666e-110">Active Directory Domain Services Unterstützung von LDAP 3,0, definiert durch RFC 3377 und LDAP 2,0, definiert durch RFC 1777.</span><span class="sxs-lookup"><span data-stu-id="4666e-110">Active Directory Domain Services support LDAP 3.0, defined by RFC 3377, and LDAP 2.0, defined by RFC 1777.</span></span> <span data-ttu-id="4666e-111">Windows-Clients verwenden LDAP 3,0, um eine Verbindung mit dem DSA herzustellen.</span><span class="sxs-lookup"><span data-stu-id="4666e-111">Windows clients use LDAP 3.0 to connect to the DSA.</span></span>
-   <span data-ttu-id="4666e-112">MAPI-Clients wie Microsoft Exchange Server stellen mithilfe der MAPI-Schnittstelle für Remote Prozedur Aufrufe eine Verbindung mit dem DSA her.</span><span class="sxs-lookup"><span data-stu-id="4666e-112">MAPI clients such as Microsoft Exchange Server connect to the DSA using the MAPI remote procedure call interface.</span></span>
-   <span data-ttu-id="4666e-113">Die DSAs in Active Directory Domain Services eine Verbindung untereinander herstellen, um die Replikation über eine proprietäre Remote Prozedur aufrufsschnittstelle auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4666e-113">The DSAs in Active Directory Domain Services connect to each other to perform replication using a proprietary remote procedure call interface.</span></span>

 

 