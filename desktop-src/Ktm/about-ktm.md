---
description: Der Kerneltransaktions-Manager (KTM) ist ein Transaktions Verwaltungsdienst. Transaktionen werden als Kernel Objekte zur Verfügung gestellt, und es werden Transaktions Verwaltungsdienste für Systemkomponenten wie Transaktions-NTFS (TxF) bereitgestellt.
ms.assetid: 85a79698-a1ae-45a4-805e-25175034fa65
title: Informationen zu KTM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1c477c7f9ae54b86fcee03435310416b38ea8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050488"
---
# <a name="about-ktm"></a><span data-ttu-id="6426c-104">Informationen zu KTM</span><span class="sxs-lookup"><span data-stu-id="6426c-104">About KTM</span></span>

<span data-ttu-id="6426c-105">Der Kerneltransaktions-Manager (KTM) ist ein Transaktions Verwaltungsdienst.</span><span class="sxs-lookup"><span data-stu-id="6426c-105">Kernel Transaction Manager (KTM) is a transaction management service.</span></span> <span data-ttu-id="6426c-106">Transaktionen werden als Kernel Objekte zur Verfügung gestellt, und es werden Transaktions Verwaltungsdienste für Systemkomponenten wie [Transaktions-NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF) bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6426c-106">It makes transactions available as kernel objects and provides transaction management services to system components such as [Transactional NTFS](/windows/desktop/FileIO/transactional-ntfs-portal) (TxF).</span></span>

<span data-ttu-id="6426c-107">In den folgenden Themen werden die Verwendungsmöglichkeiten und Funktionen von KTM beschrieben:</span><span class="sxs-lookup"><span data-stu-id="6426c-107">The following topics describe the uses and features of KTM:</span></span>

-   [<span data-ttu-id="6426c-108">Was ist eine Transaktion?</span><span class="sxs-lookup"><span data-stu-id="6426c-108">What is a Transaction?</span></span>](what-is-a-transaction.md)
-   [<span data-ttu-id="6426c-109">Arbeiten mit Transaktionen</span><span class="sxs-lookup"><span data-stu-id="6426c-109">Working With Transactions</span></span>](programming-model.md)
-   [<span data-ttu-id="6426c-110">Schreiben einer Ressourcen-Manager</span><span class="sxs-lookup"><span data-stu-id="6426c-110">Writing a Resource Manager</span></span>](writing-a-resource-manager.md)
-   [<span data-ttu-id="6426c-111">Interoperabilität mit anderen Windows-Features</span><span class="sxs-lookup"><span data-stu-id="6426c-111">Interoperability With Other Windows Features</span></span>](interoperability-with-other-windows-features.md)
-   [<span data-ttu-id="6426c-112">Sicherheit und Zugriffsrechte für KTM</span><span class="sxs-lookup"><span data-stu-id="6426c-112">KTM Security and Access Rights</span></span>](ktm-security-and-access-rights.md)

<span data-ttu-id="6426c-113">KTM basiert auf der [gemeinsames Protokolldateisystem](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) für seinen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="6426c-113">KTM relies on the [Common Log File System](/previous-versions/windows/desktop/clfs/common-log-file-system-portal) for its operation.</span></span> <span data-ttu-id="6426c-114">CLFS ist ein Protokollierungs System, das Transaktionen aktivieren kann.</span><span class="sxs-lookup"><span data-stu-id="6426c-114">CLFS is a logging system that is capable of enabling transactions.</span></span>

 

 
