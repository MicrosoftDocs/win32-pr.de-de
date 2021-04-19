---
description: Der Distributed Transaction Coordinator (DTC) ermöglicht verteilte Transaktionen oder Transaktionen, die über mehrere Ressourcen-Manager auf einem oder mehreren Systemen gesteuert werden. KTM und DTC arbeiten zusammen, um dies zu erreichen.
ms.assetid: 468379e2-c5f6-479f-9d5d-42afb395ec9b
title: Interoperabilität mit anderen Windows-Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa3aeac3d920b408a9a18c32eab83cf747525e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373138"
---
# <a name="interoperability-with-other-windows-features"></a><span data-ttu-id="65342-104">Interoperabilität mit anderen Windows-Features</span><span class="sxs-lookup"><span data-stu-id="65342-104">Interoperability With Other Windows Features</span></span>

<span data-ttu-id="65342-105">Der [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) ermöglicht *verteilte Transaktionen* oder Transaktionen, die über mehrere Ressourcen-Manager auf einem oder mehreren Systemen gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="65342-105">The [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) enables *distributed transactions*, or transactions that are under the control of multiple resource managers on one or more systems.</span></span> <span data-ttu-id="65342-106">KTM und DTC arbeiten zusammen, um dies zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="65342-106">KTM and DTC work closely together to accomplish this.</span></span>

<span data-ttu-id="65342-107">Com+ macht ein deklaratives Modell für die transaktionale Programmierung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="65342-107">COM+ exposes a declarative model for transactional programming.</span></span> <span data-ttu-id="65342-108">Das heißt, der Programmierer deklariert den Umfang, in dem ein Objekt Transaktionen nutzen kann, und die com+-Laufzeit verwaltet die Transaktionen im Auftrag des Objekts.</span><span class="sxs-lookup"><span data-stu-id="65342-108">In other words, the programmer declares the extent to which an object can take advantage of transactions, and the COM+ runtime manages the transactions on the object's behalf.</span></span> <span data-ttu-id="65342-109">Beispielsweise kann ein Objekt so deklariert werden, dass es nur dann an einer Transaktion teilnimmt, wenn bereits eine Transaktion vorhanden ist, eine Transaktion erforderlich ist (wenn Sie noch nicht vorhanden ist), damit eine neue Transaktion erforderlich ist (eine wird unabhängig davon erstellt, ob bereits eine vorhanden ist) oder nicht transaktional ist.</span><span class="sxs-lookup"><span data-stu-id="65342-109">For example, an object can be declared to participate in a transaction only if one already exists, to require a transaction (one is created if it does not already exist), to require a new transaction (one is created regardless of whether one already exists), or is not transactional.</span></span> <span data-ttu-id="65342-110">Diese deklarativ verwalteten Transaktionen werden automatisch für Datenbankverbindungen verwendet, die von COM+-Objekten erstellt werden, die im Kontext einer Transaktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="65342-110">These declaratively-managed transactions are automatically used on database connections created by COM+ objects that are executing in the context of a transaction.</span></span>

 

 
