---
description: Skripts können auf alle WMI-Klassen für Hardware-und Software Objekte zugreifen.
ms.assetid: dbb29bc8-a675-4538-99f4-00613c83eeaa
ms.tgt_platform: multiple
title: Skripterstellung für den WMI-Zugriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd487c127c670f9ddee9596e44c4b2b9691ed880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215335"
---
# <a name="scripting-access-to-wmi"></a><span data-ttu-id="2d682-103">Skripterstellung für den WMI-Zugriff</span><span class="sxs-lookup"><span data-stu-id="2d682-103">Scripting Access to WMI</span></span>

<span data-ttu-id="2d682-104">Skripts können auf alle WMI-Klassen für Hardware-und Software Objekte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="2d682-104">Scripts can access all WMI classes for hardware and software objects.</span></span> <span data-ttu-id="2d682-105">WSH-Skripts (Windows Script Host) können Vorgänge für Dateisystem Objekte, zum Bearbeiten von Netzwerkdruckern oder zum Ändern von Umgebungsvariablen ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d682-105">Windows Script Host (WSH) scripts can perform operations on file system objects, manipulate network printers, or change environment variables.</span></span> <span data-ttu-id="2d682-106">Sie finden eine Vielzahl von Administrator Aufgaben und eine kurze Anleitung dazu, wie Sie diese in WMI unter [WMI-Tasks für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md)ausführen.</span><span class="sxs-lookup"><span data-stu-id="2d682-106">You can find a variety of administrator tasks and brief guidance on how to accomplish them in WMI at [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md).</span></span> <span data-ttu-id="2d682-107">Weitere Informationen und Beispiele finden Sie im technet scriptcenter [Script-Repository](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx).</span><span class="sxs-lookup"><span data-stu-id="2d682-107">For more information and examples, see the TechNet ScriptCenter [Script Repository](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx).</span></span>

<span data-ttu-id="2d682-108">Wenn Sie mit der Skripterstellung oder WMI-spezifischer Skripterstellung noch nicht vertraut sind, lesen Sie den Abschnitt [zu](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx)den ersten Schritten im technet scriptcenter.</span><span class="sxs-lookup"><span data-stu-id="2d682-108">If you are new to scripting or to WMI-specific scripting, see the TechNet ScriptCenter section [Getting Started](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx).</span></span>

<span data-ttu-id="2d682-109">Mit der [Skript-API für WMI](scripting-api-for-wmi.md)können Sie schnelle, einfache Skripts oder komplexe Anwendungen entwickeln.</span><span class="sxs-lookup"><span data-stu-id="2d682-109">With the [Scripting API for WMI](scripting-api-for-wmi.md), you can develop quick, simple scripts or complex applications.</span></span> <span data-ttu-id="2d682-110">Mithilfe der Skripterstellung erhalten Sie die gleichen Möglichkeiten, Informationen zu erhalten oder die meisten Objekte in einem Unternehmen zu konfigurieren, wie Sie dies über eine C++-oder c#-Anwendung tun würden.</span><span class="sxs-lookup"><span data-stu-id="2d682-110">Scripting gives you the same capability of getting information or of configuring most objects in an enterprise as you would have through a C++ or C# application.</span></span> <span data-ttu-id="2d682-111">Weitere Informationen finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2d682-111">For more information, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="2d682-112">Ein [*WMI-Anbieter*](gloss-p.md) kann nicht in ein Skript geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2d682-112">You cannot write a [*WMI provider*](gloss-p.md) in script.</span></span> <span data-ttu-id="2d682-113">Weitere Informationen finden Sie unter [Bereitstellen von Daten für WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2d682-113">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="2d682-114">WMI-Skripts können in jeder Skriptsprache geschrieben werden, die mit ActiveX-Objekten interagieren kann.</span><span class="sxs-lookup"><span data-stu-id="2d682-114">WMI scripts can be written in any scripting language that can interact with ActiveX objects.</span></span>

<span data-ttu-id="2d682-115">Windows PowerShell stellt eine einfache Umgebung für die WMI-Administration und-Skripterstellung bereit.</span><span class="sxs-lookup"><span data-stu-id="2d682-115">Windows PowerShell provides a simple environment for WMI administration and scripting.</span></span> <span data-ttu-id="2d682-116">Weitere Informationen zu PowerShell finden Sie unter [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="2d682-116">For more information about PowerShell, see [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span></span>

<span data-ttu-id="2d682-117">Active Directory Service Interfaces (ADSI)-Skripts ermöglichen den Zugriff auf Active Directory Domain Services Objekte (AD DS).</span><span class="sxs-lookup"><span data-stu-id="2d682-117">Active Directory Service Interfaces (ADSI) scripts provides access to Active Directory Domain Services (AD DS) objects.</span></span> <span data-ttu-id="2d682-118">Sowohl WSH-als auch ADSI-Skripts greifen auf Objekte und Zulassungs Prozeduren zu</span><span class="sxs-lookup"><span data-stu-id="2d682-118">Both WSH and ADSI scripts access objects and allow procedures not available through batch files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d682-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2d682-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d682-120">Informationen zu WMI</span><span class="sxs-lookup"><span data-stu-id="2d682-120">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="2d682-121">Skript-API für WMI</span><span class="sxs-lookup"><span data-stu-id="2d682-121">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 
