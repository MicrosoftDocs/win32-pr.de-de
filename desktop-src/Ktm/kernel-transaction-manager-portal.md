---
description: Implementieren Sie Transaktions-NTFS (TxF) und Transaktions Registrierung (TxR). TxF ermöglicht Transaktions Dateisystem Vorgänge innerhalb von NTFS. TxR ermöglicht transaktive Registrierungs Vorgänge. Koordinieren Sie Dateisystem-und Registrierungs Vorgänge mit einer Transaktion.
ms.assetid: 2f601994-db1e-4aac-8db1-9a36c702664b
title: Kerneltransaktions-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 281050461163d5fd0cde64af79e70569d613888e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352509"
---
# <a name="kernel-transaction-manager"></a><span data-ttu-id="f5d76-106">Kerneltransaktions-Manager</span><span class="sxs-lookup"><span data-stu-id="f5d76-106">Kernel Transaction Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="f5d76-107">Zweck</span><span class="sxs-lookup"><span data-stu-id="f5d76-107">Purpose</span></span>

<span data-ttu-id="f5d76-108">Der Kerneltransaktions-Manager (KTM) ermöglicht die Entwicklung von Anwendungen, die Transaktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5d76-108">The Kernel Transaction Manager (KTM) enables the development of applications that use transactions.</span></span> <span data-ttu-id="f5d76-109">Die Transaktions-Engine selbst befindet sich innerhalb des Kernels, Transaktionen können jedoch für Kernel-oder benutzermodustransaktionen und innerhalb eines einzelnen Hosts oder verteilter Hosts entwickelt werden.</span><span class="sxs-lookup"><span data-stu-id="f5d76-109">The transaction engine itself is within the kernel, but transactions can be developed for kernel- or user-mode transactions, and within a single host or among distributed hosts.</span></span>

<span data-ttu-id="f5d76-110">Der KTM wird zum Implementieren von transaktionalen NTFS (TxF) und Transaktions Registrierung (TxR) verwendet.</span><span class="sxs-lookup"><span data-stu-id="f5d76-110">The KTM is used to implement Transactional NTFS (TxF) and Transactional Registry (TxR).</span></span> <span data-ttu-id="f5d76-111">TxF ermöglicht Transaktions Dateisystem Vorgänge innerhalb des NTFS-Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="f5d76-111">TxF allows transacted file system operations within the NTFS file system.</span></span> <span data-ttu-id="f5d76-112">TxR ermöglicht transaktive Registrierungs Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="f5d76-112">TxR allows transacted registry operations.</span></span> <span data-ttu-id="f5d76-113">KTM ermöglicht Client Anwendungen das Koordinieren von Dateisystem-und Registrierungs Vorgängen mit einer Transaktion.</span><span class="sxs-lookup"><span data-stu-id="f5d76-113">KTM enables client applications to coordinate file system and registry operations with a transaction.</span></span>

<span data-ttu-id="f5d76-114">Zum Entwickeln einer Anwendung, die Transaktionen mit anderen Ressourcen als TxF oder TxR koordiniert, müssen Sie zunächst einen Dienst für die Win32-Transaktion entwickeln, der auch als Ressourcen-Manager bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="f5d76-114">To develop an application that coordinates transactions with resources other than TxF or TxR, you must first develop a Win32 transaction-aware service, also called a resource manager.</span></span>

<span data-ttu-id="f5d76-115">Verwaltete und com+-Anwendungen sollten ihre nativen Transaktions-Manager verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5d76-115">Managed and COM+ applications should use their native transaction managers.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="f5d76-116">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="f5d76-116">Where applicable</span></span>

<span data-ttu-id="f5d76-117">KTM kann mit Anwendungen und Ressourcen-Managern verwendet werden, die unter Windows Vista oder Windows Server 2008 gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="f5d76-117">KTM can be used with applications and resource managers hosted on Windows Vista or Windows Server 2008.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="f5d76-118">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="f5d76-118">Developer audience</span></span>

<span data-ttu-id="f5d76-119">Die KTM-API ist für die Verwendung durch C-und C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="f5d76-119">The KTM API is designed for use by C and C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f5d76-120">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="f5d76-120">Run-time requirements</span></span>

<span data-ttu-id="f5d76-121">KTM wird ab Windows Vista unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f5d76-121">KTM is supported starting with Windows Vista.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f5d76-122">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f5d76-122">In this section</span></span>



| <span data-ttu-id="f5d76-123">Thema</span><span class="sxs-lookup"><span data-stu-id="f5d76-123">Topic</span></span>                                     | <span data-ttu-id="f5d76-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5d76-124">Description</span></span>                                                                                                       |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5d76-125">Info</span><span class="sxs-lookup"><span data-stu-id="f5d76-125">About</span></span>](about-ktm.md)<br/>         | <span data-ttu-id="f5d76-126">Allgemeine Informationen zu Transaktionen und den von KTM bereitgestellten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="f5d76-126">General information about transactions and the capabilities provided by KTM.</span></span><br/>                           |
| [<span data-ttu-id="f5d76-127">Verweis</span><span class="sxs-lookup"><span data-stu-id="f5d76-127">Reference</span></span>](ktm-reference.md)<br/> | <span data-ttu-id="f5d76-128">Dokumentation für die Funktionen, Datenstrukturen, Enumerationen und andere Programmier Elemente von KTM.</span><span class="sxs-lookup"><span data-stu-id="f5d76-128">Documentation for the functions, data structures, enumerations, and other programming elements of KTM.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f5d76-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f5d76-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5d76-130">Gemeinsames Protokolldateisystem</span><span class="sxs-lookup"><span data-stu-id="f5d76-130">Common Log File System</span></span>](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)
</dt> <dt>

[<span data-ttu-id="f5d76-131">Transaktionale NTFS (TxF)</span><span class="sxs-lookup"><span data-stu-id="f5d76-131">Transactional NTFS (TxF)</span></span>](/windows/desktop/FileIO/transactional-ntfs-portal)
</dt> <dt>

<span data-ttu-id="f5d76-132">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f5d76-132">[Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85))</span></span>
</dt> </dl>

 

