---
description: Verwalten Sie die assemblyfreigabe und die dll-Versionsverwaltung im nebeneinander gespeicherten Assemblyspeicher über Programme. Schreiben von Assemblymanifesten und selbst beschreibenden Anwendungen für das Freigeben und Umleiten von DLLs.
ms.assetid: 2f841eb6-9a6c-4c9b-b057-a3da6cd6b0b0
title: Isolierte Anwendungen und parallele Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59abfbd5392040856c66ef9eb786b66d2a84500f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128821"
---
# <a name="isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="54f2a-104">Isolierte Anwendungen und parallele Assemblys</span><span class="sxs-lookup"><span data-stu-id="54f2a-104">Isolated Applications and Side-by-side Assemblies</span></span>

## <a name="purpose"></a><span data-ttu-id="54f2a-105">Zweck</span><span class="sxs-lookup"><span data-stu-id="54f2a-105">Purpose</span></span>

<span data-ttu-id="54f2a-106">Isolierte Anwendungen und parallele Assemblys sind eine Microsoft Windows-Lösung, mit der die Versions Konflikte in Windows-Client Anwendungen verringert werden.</span><span class="sxs-lookup"><span data-stu-id="54f2a-106">Isolated Applications and Side-by-side Assemblies is a Microsoft Windows solution that reduces versioning conflicts in Windows-client applications.</span></span> <span data-ttu-id="54f2a-107">Mit Windows können Anwendungsentwickler isolierte Anwendungen erstellen, die vollständig selbst beschreibend sind und von Änderungen an der Registrierung, anderen Anwendungen oder anderen Versionen von Assemblys, die auf dem System ausgeführt werden, nicht betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="54f2a-107">With Windows, application developers can build isolated applications that are fully self-describing and unaffected by changes to the registry, other applications, or other versions of assemblies running on the system.</span></span> <span data-ttu-id="54f2a-108">Anwendungs Autoren und Administratoren können Manifeste verwenden, um die Freigabe von parallelen Assemblys nach der Bereitstellung entweder auf globaler oder pro Anwendung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="54f2a-108">Application authors and administrators can use manifests to manage the sharing of side-by-side assemblies after deployment on either a global or per-application basis.</span></span> <span data-ttu-id="54f2a-109">Kunden profitieren von isolierten Anwendungen, die stabiler und zuverlässiger aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="54f2a-109">Customers benefit from isolated applications that are more stable and more reliably updated.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="54f2a-110">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="54f2a-110">Where applicable</span></span>

<span data-ttu-id="54f2a-111">Isolierte Anwendungen und parallele assemblyfreigabe können verwendet werden, um Anwendungen zu entwickeln, die Betriebs Systemassemblys sicher freigeben.</span><span class="sxs-lookup"><span data-stu-id="54f2a-111">Isolated applications and side-by-side assembly sharing can be used to develop applications that safely share operating system assemblies.</span></span> <span data-ttu-id="54f2a-112">Entwickler können diese Technologie verwenden, um dll-Versions Verwaltungs Konflikte zu beheben, die durch eine nicht kompatible Version einer freigegebenen Assembly verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="54f2a-112">Developers can use this technology to correct DLL versioning conflicts caused by an incompatible version of a shared assembly.</span></span>

<span data-ttu-id="54f2a-113">Wenn Ihre Anwendung die Version einer Komponente, die Sie getestet haben, konsistent finden muss, ist es möglich, die Anwendung so zu isolieren, dass Sie immer mit der getesteten Version der Komponente auf dem Computer des Benutzers ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54f2a-113">If your application must consistently get the version of a component you have tested, it is possible to isolate your application so that it will always be run with the tested version of the component on the user's computer.</span></span>

<span data-ttu-id="54f2a-114">Isolierte Anwendungen und parallele Assemblys sind für die Entwicklung von Anwendungen im Desktop Stil vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="54f2a-114">Isolated Applications and Side-by-side Assemblies is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="54f2a-115">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="54f2a-115">Developer audience</span></span>

<span data-ttu-id="54f2a-116">Diese Dokumentation richtet sich hauptsächlich an Softwareentwickler, Anwendungsentwickler und Netzwerkadministratoren:</span><span class="sxs-lookup"><span data-stu-id="54f2a-116">This documentation is primarily intended for software developers, application developers, and network administrators:</span></span>

-   <span data-ttu-id="54f2a-117">Software Entwickler, die isolierte Anwendungen erstellen möchten, die die parallelen Assemblys verwenden, die von Microsoft und anderen parallelen assemblyverlegern zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="54f2a-117">Software developers who want to create isolated applications that will use the side-by-side assemblies made available by Microsoft and other side-by-side assembly publishers.</span></span>
-   <span data-ttu-id="54f2a-118">Anwendungsentwickler, die daran interessiert sind, eigene parallele Assemblys zu erstellen, um Ihre Anwendungen zu isolieren.</span><span class="sxs-lookup"><span data-stu-id="54f2a-118">Application developers who are interested in creating their own side-by-side assemblies to isolate their applications.</span></span>
-   <span data-ttu-id="54f2a-119">Netzwerkadministratoren, die weitere Informationen zu isolierten Anwendungen benötigen.</span><span class="sxs-lookup"><span data-stu-id="54f2a-119">Network administrators who want more information about isolated applications.</span></span>

<span data-ttu-id="54f2a-120">In dieser Dokumentation finden Sie als Haupt Referenz für parallele assemblyfreigabe und isolierte Anwendungen allgemeine Hintergrundinformationen zum Erstellen von Manifesten und parallelen Assemblys, zum Installieren von isolierten Anwendungen und parallelen Assemblys sowie zur Verwendung der Aktivierungs Kontext-API.</span><span class="sxs-lookup"><span data-stu-id="54f2a-120">As the primary reference for side-by-side assembly sharing and isolated applications, this documentation provides general background information about authoring manifests and side-by-side assemblies, installing isolated applications and side-by-side assemblies, and using the Activation Context API.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="54f2a-121">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="54f2a-121">Run-time requirements</span></span>

<span data-ttu-id="54f2a-122">Windows Server 2003 und höher oder Windows XP und höher müssen parallele Assemblys und Manifeste verwenden, um Anwendungen zu isolieren und die Aktivierungs Kontext-API zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="54f2a-122">Windows Server 2003 and later or Windows XP and later is required to use side-by-side assemblies and manifests to isolate applications and to use the Activation Context API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="54f2a-123">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="54f2a-123">In this section</span></span>



| <span data-ttu-id="54f2a-124">Thema</span><span class="sxs-lookup"><span data-stu-id="54f2a-124">Topic</span></span>                                                         | <span data-ttu-id="54f2a-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54f2a-125">Description</span></span>                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="54f2a-126">Verweis</span><span class="sxs-lookup"><span data-stu-id="54f2a-126">Reference</span></span>](side-by-side-assemblies-reference.md)<br/> | <span data-ttu-id="54f2a-127">Dokumentation zu isolierten Anwendungen und parallelen Assemblys.</span><span class="sxs-lookup"><span data-stu-id="54f2a-127">Documentation of Isolated Applications and Side-by-side Assemblies.</span></span><br/> |



 

 

 




