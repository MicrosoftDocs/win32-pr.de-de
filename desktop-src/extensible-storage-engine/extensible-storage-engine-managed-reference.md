---
description: Weitere Informationen finden Sie in der verwalteten Referenz zu Extensible Storage Engine.
title: Verwaltete Referenz zu Extensible Storage Engine
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: a1323d662cc7252ff6bda1eda53108751d3aedfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041916"
---
# <a name="extensible-storage-engine-managed-reference"></a><span data-ttu-id="089a4-103">Verwaltete Referenz zu Extensible Storage Engine</span><span class="sxs-lookup"><span data-stu-id="089a4-103">Extensible Storage Engine Managed Reference</span></span>

<span data-ttu-id="089a4-104">Suchen Sie nach Referenzinformationen für die managedesent-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="089a4-104">Find reference information for the ManagedESENT library.</span></span> <span data-ttu-id="089a4-105">Die managedesent-Bibliothek bietet verwalteten Zugriff auf ESENT, das einbettbare Datenbankmodul, das in Windows System eigen ist.</span><span class="sxs-lookup"><span data-stu-id="089a4-105">The ManagedESENT library provides managed access to ESENT, the embeddable database engine that is native to Windows.</span></span>


<span data-ttu-id="089a4-106">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="089a4-106">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="089a4-107">**Inhalt dieses Artikels:**</span><span class="sxs-lookup"><span data-stu-id="089a4-107">**In this article**</span></span>  
<span data-ttu-id="089a4-108">Wie unterscheidet sich die managedesent-Bibliothek von ESENT?</span><span class="sxs-lookup"><span data-stu-id="089a4-108">How is the ManagedESENT library different than ESENT?</span></span>  
<span data-ttu-id="089a4-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="089a4-109">Requirements</span></span>  
<span data-ttu-id="089a4-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="089a4-110">In this section</span></span>  

## <a name="how-is-the-managedesent-library-different-than-esent"></a><span data-ttu-id="089a4-111">Wie unterscheidet sich die managedesent-Bibliothek von ESENT?</span><span class="sxs-lookup"><span data-stu-id="089a4-111">How is the ManagedESENT library different than ESENT?</span></span>

<span data-ttu-id="089a4-112">ESENT ist eine einbettbare, transaktionale Datenbank-Engine, mit der Sie benutzerdefinierte Anwendungen erstellen können, die eine zuverlässige, hochleistungsfähige Speicherung von Daten benötigen.</span><span class="sxs-lookup"><span data-stu-id="089a4-112">ESENT is an embeddable, transactional database engine that allows you to create custom applications that need reliable, high-performance, low-overhead storage of data.</span></span> <span data-ttu-id="089a4-113">Die ESENT-Engine kann bei Datenanforderungen helfen, die von etwas einfachem wie einer zu großen Hash Tabelle, die zu groß für die Speicherung im Arbeitsspeicher ist, bis hin zu komplexen Daten, wie z. b. einer Anwendung mit Tabellen, Spalten und Indizes, reichen.</span><span class="sxs-lookup"><span data-stu-id="089a4-113">The ESENT engine can help with data needs that range from something as simple as a hash table that is too large to store in memory, to something more complex, such as an application with tables, columns, and indexes.</span></span> <span data-ttu-id="089a4-114">Um eine Anwendung mit ESENT zu erstellen, verwenden Sie die esent.dll-dll, die Teil des Windows-Betriebssystems ist, und schreiben Ihren Code mit C/C++.</span><span class="sxs-lookup"><span data-stu-id="089a4-114">To create an application with ESENT, you use the esent.dll DLL that is part of the Windows operating system and write your code with C/C++.</span></span> <span data-ttu-id="089a4-115">Weitere Informationen zu ESENT finden Sie unter [Extensible Storage Engine Reference](./extensible-storage-engine-reference.md).</span><span class="sxs-lookup"><span data-stu-id="089a4-115">For more information about ESENT, see [Extensible Storage Engine Reference](./extensible-storage-engine-reference.md).</span></span>

<span data-ttu-id="089a4-116">Managedesent baut auf esent.dll auf, die Teil von Windows ist, sodass keine zusätzlichen nicht verwalteten Binärdateien zum herunterladen und installieren vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="089a4-116">ManagedESENT is built on top of esent.dll, which is part of Windows, so there are no extra unmanaged binaries to download and install.</span></span> <span data-ttu-id="089a4-117">Mit der managedesent-Bibliothek können Sie die Anwendung erstellen, indem Sie eine verwaltete Sprache, wie z. b. c, \# anstelle von c/C++ verwenden.</span><span class="sxs-lookup"><span data-stu-id="089a4-117">With the ManagedESENT library, you can create your application by using a managed language such as C\# instead of C/C++.</span></span> <span data-ttu-id="089a4-118">Die Bibliothek verwendet die gleichen Typen-und Elementnamen, um die ESE-API verfügbar zu machen. Wenn Sie also bereits mit der Struktur dieser API vertraut sind, können Sie problemlos zu dieser verwalteten Bibliothek wechseln.</span><span class="sxs-lookup"><span data-stu-id="089a4-118">The library uses the same type and member names to expose the ESE API, so if you are already familiar with the structure of this API, you can easily transition to this managed library.</span></span>

## <a name="requirements"></a><span data-ttu-id="089a4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="089a4-119">Requirements</span></span>

<span data-ttu-id="089a4-120">Für diese verwaltete Bibliothek ist Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="089a4-120">This managed library requires the following:</span></span>

  - <span data-ttu-id="089a4-121">Ein Computer, auf dem eine Windows-Version ab Windows Vista ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="089a4-121">A computer running a version of Windows starting with Windows Vista</span></span>

  - <span data-ttu-id="089a4-122">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="089a4-122">Visual Studio 2012</span></span>

  - <span data-ttu-id="089a4-123">Das .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="089a4-123">The .NET Framework 4.5</span></span>

## <a name="in-this-section"></a><span data-ttu-id="089a4-124">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="089a4-124">In this section</span></span>

  - [<span data-ttu-id="089a4-125">Microsoft. ISAM. ESENT</span><span class="sxs-lookup"><span data-stu-id="089a4-125">Microsoft.Isam.Esent</span></span>](./microsoft.isam.esent-namespace.md)

  - [<span data-ttu-id="089a4-126">Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="089a4-126">Microsoft.Isam.Esent.Interop</span></span>](./microsoft.isam.esent.interop-namespace.md)

  - [<span data-ttu-id="089a4-127">Microsoft. ISAM. ESENT. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="089a4-127">Microsoft.Isam.Esent.Interop.Server2003</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [<span data-ttu-id="089a4-128">Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="089a4-128">Microsoft.Isam.Esent.Interop.Vista</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)

  - [<span data-ttu-id="089a4-129">Microsoft. ISAM. ESENT. Interop. Windows7</span><span class="sxs-lookup"><span data-stu-id="089a4-129">Microsoft.Isam.Esent.Interop.Windows7</span></span>](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [<span data-ttu-id="089a4-130">Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="089a4-130">Microsoft.Isam.Esent.Interop.Windows8</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
