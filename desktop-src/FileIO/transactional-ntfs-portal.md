---
description: Transaktionale NTFS (TxF) ermöglicht die Ausführung von Datei Vorgängen auf einem NTFS-Dateisystem Volume in einer Transaktion.
ms.assetid: e8c3ceed-d391-4934-b3f7-12c2123c8c23
title: Transaktionale NTFS (TxF)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7553bfc7cae0b5389762527f0ac726c674a6a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524926"
---
# <a name="transactional-ntfs-txf"></a><span data-ttu-id="b72be-103">Transaktionale NTFS (TxF)</span><span class="sxs-lookup"><span data-stu-id="b72be-103">Transactional NTFS (TxF)</span></span>

<span data-ttu-id="b72be-104">\[Microsoft empfiehlt Entwicklern dringend, Alternative Möglichkeiten zum Erreichen der Anforderungen Ihrer Anwendung zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="b72be-104">\[Microsoft strongly recommends developers utilize alternative means to achieve your application s needs.</span></span> <span data-ttu-id="b72be-105">Viele Szenarios, für die TxF entwickelt wurde, können mithilfe einfacherer und leichter verfügbarer Techniken erreicht werden.</span><span class="sxs-lookup"><span data-stu-id="b72be-105">Many scenarios that TxF was developed for can be achieved through simpler and more readily available techniques.</span></span> <span data-ttu-id="b72be-106">Außerdem ist TxF in zukünftigen Versionen von Microsoft Windows möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b72be-106">Furthermore, TxF may not be available in future versions of Microsoft Windows.</span></span> <span data-ttu-id="b72be-107">Weitere Informationen und Alternativen zu TxF finden Sie unter [Alternativen zur Verwendung von transaktionalen NTFS](deprecation-of-txf.md).\]</span><span class="sxs-lookup"><span data-stu-id="b72be-107">For more information, and alternatives to TxF, please see [Alternatives to using Transactional NTFS](deprecation-of-txf.md).\]</span></span>

## <a name="purpose"></a><span data-ttu-id="b72be-108">Zweck</span><span class="sxs-lookup"><span data-stu-id="b72be-108">Purpose</span></span>

<span data-ttu-id="b72be-109">Transaktionale NTFS (TxF) ermöglicht die Ausführung von Datei Vorgängen auf einem NTFS-Dateisystem Volume in einer Transaktion.</span><span class="sxs-lookup"><span data-stu-id="b72be-109">Transactional NTFS (TxF) allows file operations on an NTFS file system volume to be performed in a transaction.</span></span> <span data-ttu-id="b72be-110">TxF-Transaktionen erhöhen die Anwendungs Zuverlässigkeit, indem Sie die Datenintegrität über Fehler hinweg schützen und die Anwendungsentwicklung vereinfachen, indem Sie den Code für die Fehlerbehandlung erheblich verringern.</span><span class="sxs-lookup"><span data-stu-id="b72be-110">TxF transactions increase application reliability by protecting data integrity across failures and simplify application development by greatly reducing the amount of error handling code.</span></span>

<span data-ttu-id="b72be-111">TxF verwendet das Transaktions Framework, das vom [Kerneltransaktions-Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal) (KTM) bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b72be-111">TxF uses the transaction framework provided by the [Kernel Transaction Manager](/windows/desktop/Ktm/kernel-transaction-manager-portal) (KTM).</span></span> <span data-ttu-id="b72be-112">Dies ermöglicht die Ausführung von TxF-Datei Vorgängen in eine Transaktion mit anderen Datenquellen, z. b. SQL Server und Transaktions Registrierung (TxR).</span><span class="sxs-lookup"><span data-stu-id="b72be-112">This allows TxF file operations to be part of a transaction involving other data sources such as SQL Server and Transacted Registry (TxR).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="b72be-113">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="b72be-113">Where applicable</span></span>

<span data-ttu-id="b72be-114">Eine Anwendung kann TxF verwenden, um die Integrität der Daten auf dem Datenträger beizubehalten, die durch unerwartete Fehlerbedingungen verursacht werden, und unterstützt die Auflösung paralleler Dateisystem-Benutzer Szenarien, indem Ihre Änderungen von anderen isoliert werden, während die Änderungen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="b72be-114">An application can use TxF to preserve the integrity of data on disk caused by unexpected error conditions and help resolve concurrent file-system user scenarios by isolating your changes from others while the changes are being made.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b72be-115">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="b72be-115">Developer audience</span></span>

<span data-ttu-id="b72be-116">Vor der Verwendung von TxF sollten Sie über ein funktionierendes wissen über Transaktionen verfügen, indem Sie entweder KTM oder [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85))verwenden.</span><span class="sxs-lookup"><span data-stu-id="b72be-116">Before using TxF, you should have a working knowledge of transactions using either KTM or [Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/ms684146(v=vs.85)).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b72be-117">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="b72be-117">Run-time requirements</span></span>

<span data-ttu-id="b72be-118">TxF ist ab Windows Vista verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b72be-118">TxF is available starting with Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b72be-119">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="b72be-119">In this section</span></span>



| <span data-ttu-id="b72be-120">Thema</span><span class="sxs-lookup"><span data-stu-id="b72be-120">Topic</span></span>                                                    | <span data-ttu-id="b72be-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b72be-121">Description</span></span>                                                                                                |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b72be-122">Info</span><span class="sxs-lookup"><span data-stu-id="b72be-122">About</span></span>](about-transactional-ntfs.md)<br/>         | <span data-ttu-id="b72be-123">Allgemeine Informationen zu Transaktions-NTFS.</span><span class="sxs-lookup"><span data-stu-id="b72be-123">General information about Transactional NTFS.</span></span><br/>                                                   |
| [<span data-ttu-id="b72be-124">Verweis</span><span class="sxs-lookup"><span data-stu-id="b72be-124">Reference</span></span>](transactional-ntfs-reference.md)<br/> | <span data-ttu-id="b72be-125">Dokumentation für die Funktionen, Datenstrukturen, Enumerationen und andere Programmier Elemente.</span><span class="sxs-lookup"><span data-stu-id="b72be-125">Documentation for the functions, data structures, enumerations, and other programming elements.</span></span><br/> |



 

 

