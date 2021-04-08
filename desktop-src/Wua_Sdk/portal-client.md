---
description: Die Windows Update Agent-API (WUA) ist ein Satz von COM-Schnittstellen, mit denen Systemadministratoren und Programmierer auf Windows Update und Windows Server Update Services (WSUS) zugreifen können.
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: Windows Update-Agent-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c34cb76619c9739c84e650a32590fdc4f61022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750000"
---
# <a name="windows-update-agent-api"></a><span data-ttu-id="1875b-103">Windows Update-Agent-API</span><span class="sxs-lookup"><span data-stu-id="1875b-103">Windows Update Agent API</span></span>

## <a name="purpose"></a><span data-ttu-id="1875b-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="1875b-104">Purpose</span></span>

<span data-ttu-id="1875b-105">Die Windows Update Agent-API (WUA) ist ein Satz von COM-Schnittstellen, mit denen Systemadministratoren und Programmierer auf Windows Update und [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85))zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="1875b-105">The Windows Update Agent (WUA) API is a set of COM interfaces that enable system administrators and programmers to access Windows Update and [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85)).</span></span> <span data-ttu-id="1875b-106">Skripts und Programme können geschrieben werden, um zu überprüfen, welche Updates derzeit für einen Computer verfügbar sind. Anschließend können Sie Updates installieren oder deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="1875b-106">Scripts and programs can be written to examine which updates are currently available for a computer, and then you can install or uninstall updates.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="1875b-107">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="1875b-107">Where applicable</span></span>

<span data-ttu-id="1875b-108">System Administratoren können WUA verwenden, um Programm gesteuert zu ermitteln, welche Updates auf einen Computer angewendet werden sollen, diese Updates herunterzuladen und dann mit geringem oder ohne Benutzereingriff zu installieren.</span><span class="sxs-lookup"><span data-stu-id="1875b-108">System administrators can use WUA to programmatically determine which updates should be applied to a computer, download those updates, and then install them with little or no user intervention.</span></span>

<span data-ttu-id="1875b-109">Unabhängige Softwareanbieter (Independent Softwareanbieters, ISV) und Endbenutzer Entwickler können WUA-Features in die Computer Verwaltung oder Update Verwaltungssoftware integrieren, um eine nahtlose Betriebsumgebung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="1875b-109">Independent software vendors (ISV) and end-user developers can integrate WUA features into computer management or update management software to provide a seamless operating environment.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="1875b-110">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="1875b-110">Developer audience</span></span>

<span data-ttu-id="1875b-111">WUA-Anwendungen können in mehreren Programmiersprachen geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1875b-111">You can write WUA applications in several programming languages.</span></span> <span data-ttu-id="1875b-112">WUA definiert Schnittstellen und Objekte, auf die von Visual Basic, Visual Basic Scripting Edition (VBScript), JScript und von C und C++ aus zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="1875b-112">WUA defines interfaces and objects that are accessible from Visual Basic, Visual Basic Scripting Edition (VBScript), JScript, and from C and C++.</span></span> <span data-ttu-id="1875b-113">Eine Vertrautheit mit der com-Programmierung ist für den WUA-Programmierer nützlich.</span><span class="sxs-lookup"><span data-stu-id="1875b-113">A familiarity with COM programming is useful to the WUA programmer.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1875b-114">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="1875b-114">Run-time requirements</span></span>

<span data-ttu-id="1875b-115">WUA wird ab Windows XP unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1875b-115">WUA is supported starting with Windows XP.</span></span> <span data-ttu-id="1875b-116">WUA wird auf dem Server ab Windows Server 2003 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1875b-116">WUA is supported on the server starting with Windows Server 2003.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1875b-117">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="1875b-117">In this section</span></span>

-   [<span data-ttu-id="1875b-118">Verwenden der Windows Update-Agent-API</span><span class="sxs-lookup"><span data-stu-id="1875b-118">Using the Windows Update Agent API</span></span>](using-the-windows-update-agent-api.md)
-   [<span data-ttu-id="1875b-119">WUA-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="1875b-119">WUA API Reference</span></span>](windows-update-agent--wua--api-reference.md)

 

 
