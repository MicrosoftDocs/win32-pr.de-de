---
description: Transaktionale NTFS (TxF) integriert Transaktionen in das NTFS-Dateisystem, wodurch Anwendungsentwicklern und Administratoren das ordnungsgemäße behandeln von Fehlern und das Beibehalten der Datenintegrität vereinfachen.
ms.assetid: 52341315-0412-4a87-aca0-9adea7aae62f
title: Informationen zu Transaktions-NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcf8cd99dfb1ff18ef7da88d3b3c7b0a647417e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343639"
---
# <a name="about-transactional-ntfs"></a><span data-ttu-id="54f16-103">Informationen zu Transaktions-NTFS</span><span class="sxs-lookup"><span data-stu-id="54f16-103">About Transactional NTFS</span></span>

<span data-ttu-id="54f16-104">\[Microsoft empfiehlt Entwicklern dringend, Alternative Möglichkeiten zum Erreichen der Anforderungen Ihrer Anwendung zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="54f16-104">\[Microsoft strongly recommends developers utilize alternative means to achieve your application s needs.</span></span> <span data-ttu-id="54f16-105">Viele Szenarios, für die TxF entwickelt wurde, können mithilfe einfacherer und leichter verfügbarer Techniken erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="54f16-105">Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques.</span></span> <span data-ttu-id="54f16-106">Außerdem ist TxF in zukünftigen Versionen von Microsoft Windows möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="54f16-106">Furthermore, TxF may not be available in future versions of Microsoft Windows.</span></span> <span data-ttu-id="54f16-107">Weitere Informationen und Alternativen zu TxF finden Sie unter [Alternativen zur Verwendung von transaktionalen NTFS](deprecation-of-txf.md).\]</span><span class="sxs-lookup"><span data-stu-id="54f16-107">For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](deprecation-of-txf.md).\]</span></span>

<span data-ttu-id="54f16-108">Transaktionale NTFS (TxF) integriert Transaktionen in das NTFS-Dateisystem, wodurch Anwendungsentwicklern und Administratoren das ordnungsgemäße behandeln von Fehlern und das Beibehalten der Datenintegrität vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="54f16-108">Transactional NTFS (TxF) integrates transactions into the NTFS file system, which makes it easier for application developers and administrators to gracefully handle errors and preserve data integrity.</span></span>

<span data-ttu-id="54f16-109">TxF kann an verteilten Transaktionen teilnehmen, die die [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) -Koordinaten enthalten, sodass Sie TxF für Folgendes verwenden können:</span><span class="sxs-lookup"><span data-stu-id="54f16-109">TxF can participate in distributed transactions that the [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)) coordinates, which allows you to use TxF for the following:</span></span>

-   <span data-ttu-id="54f16-110">Transaktionen, die mehrere Datenspeicher umfassen, z. b. eine einzelne Transaktion für Datei-und SQL-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="54f16-110">Transactions that span multiple data stores, for example, a single transaction for file and SQL operations</span></span>
-   <span data-ttu-id="54f16-111">Transaktionen, die mehrere Computer umfassen, z. b. eine einzelne Transaktion für Datei Updates auf mehreren Computern</span><span class="sxs-lookup"><span data-stu-id="54f16-111">Transactions that span multiple computers, for example, a single transaction for file updates on multiple computers</span></span>

## <a name="in-this-section"></a><span data-ttu-id="54f16-112">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="54f16-112">In this section</span></span>



| <span data-ttu-id="54f16-113">Thema</span><span class="sxs-lookup"><span data-stu-id="54f16-113">Topic</span></span>                                                                                                                 | <span data-ttu-id="54f16-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54f16-114">Description</span></span>                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54f16-115">Verwendungszwecke von transaktionalen NTFS</span><span class="sxs-lookup"><span data-stu-id="54f16-115">When to Use Transactional NTFS</span></span>](when-to-use-transactional-ntfs.md)<br/>                                       | <span data-ttu-id="54f16-116">Verwenden Sie Transaktions-NTFS, um die Datenintegrität beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="54f16-116">Use Transactional NTFS to maintain data integrity.</span></span><br/>                                                                        |
| [<span data-ttu-id="54f16-117">Bereitstellen von transaktionalen NTFS</span><span class="sxs-lookup"><span data-stu-id="54f16-117">Deploying Transactional NTFS</span></span>](deploying-transactional-ntfs.md)<br/>                                           | <span data-ttu-id="54f16-118">Caching-Steuerelement in transaktionalen NTFS.</span><span class="sxs-lookup"><span data-stu-id="54f16-118">Caching control in Transactional NTFS.</span></span><br/>                                                                                    |
| [<span data-ttu-id="54f16-119">Verwenden von transaktionalen NTFS</span><span class="sxs-lookup"><span data-stu-id="54f16-119">How to Use Transactional NTFS</span></span>](how-to-use-transactional-ntfs.md)<br/>                                         | <span data-ttu-id="54f16-120">Verwalten von transaktiven Datei Handles in Transaktions-NTFS.</span><span class="sxs-lookup"><span data-stu-id="54f16-120">Managing transacted file handles in Transactional NTFS.</span></span><br/>                                                                   |
| [<span data-ttu-id="54f16-121">Grundlegende TxF-Konzepte</span><span class="sxs-lookup"><span data-stu-id="54f16-121">Basic TxF Concepts</span></span>](txf-basic-concepts.md)<br/>                                                               | <span data-ttu-id="54f16-122">Beschreibt die Konsistenz mit Lese-und Schreibzugriff, die Isolation mit Lese-und Schreibzugriff sowie die Konzepte von Transaktions Sperren in Transaktions-NTFS.</span><span class="sxs-lookup"><span data-stu-id="54f16-122">Describes read-committed consistency, read-committed isolation, and transactional locking concepts in Transactional NTFS.</span></span><br/> |
| [<span data-ttu-id="54f16-123">Überlegungen zur Programmierung für transaktionale NTFS</span><span class="sxs-lookup"><span data-stu-id="54f16-123">Programming Considerations for Transactional NTFS</span></span>](programming-considerations-for-transacted-fileio-.md)<br/> | <span data-ttu-id="54f16-124">Beschreibt verschiedene Programmier Überlegungen für Transaktions-NTFS.</span><span class="sxs-lookup"><span data-stu-id="54f16-124">Describes various programming considerations for Transactional NTFS.</span></span><br/>                                                      |
| [<span data-ttu-id="54f16-125">Überlegungen zur Leistung von transaktionalen NTFS</span><span class="sxs-lookup"><span data-stu-id="54f16-125">Performance Considerations for Transactional NTFS</span></span>](performance-considerations-for-transactional-ntfs.md)<br/> | <span data-ttu-id="54f16-126">Empfehlungen für optimale Dateisystem Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="54f16-126">Recommendations for optimal file system transactions.</span></span><br/>                                                                     |



 

 

