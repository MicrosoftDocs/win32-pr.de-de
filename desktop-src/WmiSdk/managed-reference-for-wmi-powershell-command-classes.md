---
description: Verwaltete Referenz für WMI-Windows PowerShell-Befehls Klassen
ms.assetid: 30e77956-8428-4259-9218-b93f143fd987
ms.tgt_platform: multiple
title: Verwaltete Referenz für WMI-Windows PowerShell-Befehls Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb309a9ca421a3966f84ba1ae825bd0c81eee8ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352252"
---
# <a name="managed-reference-for-wmi-windows-powershell-command-classes"></a><span data-ttu-id="a3dd1-103">Verwaltete Referenz für WMI-Windows PowerShell-Befehls Klassen</span><span class="sxs-lookup"><span data-stu-id="a3dd1-103">Managed Reference for WMI Windows PowerShell Command Classes</span></span>

<span data-ttu-id="a3dd1-104">Windows PowerShell implementiert Windows-Verwaltungsinstrumentation (WMI)-Funktionalität durch eine Reihe von Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="a3dd1-104">Windows PowerShell implements Windows Management Instrumentation (WMI) functionality through a set of cmdlets.</span></span> <span data-ttu-id="a3dd1-105">Sie können diese Cmdlets verwenden, um die End-to-End-Aufgaben abzuschließen, die zum Verwalten von lokalen Computern und Remote Computern notwendig sind.</span><span class="sxs-lookup"><span data-stu-id="a3dd1-105">You can use these cmdlets to complete the end-to-end tasks that are necessary to manage local and remote computers.</span></span>

<span data-ttu-id="a3dd1-106">Weitere Informationen finden Sie in der [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="a3dd1-106">See [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) for more information.</span></span>

## <a name="wmi-powershell-classes"></a><span data-ttu-id="a3dd1-107">WMI-PowerShell-Klassen</span><span class="sxs-lookup"><span data-stu-id="a3dd1-107">WMI PowerShell Classes</span></span>

<span data-ttu-id="a3dd1-108">**Namespace**: Microsoft. PowerShell. Commands</span><span class="sxs-lookup"><span data-stu-id="a3dd1-108">**Namespace**: Microsoft.PowerShell.Commands</span></span>

<span data-ttu-id="a3dd1-109">**Assembly**: Microsoft. PowerShell. Commands. Management</span><span class="sxs-lookup"><span data-stu-id="a3dd1-109">**Assembly**: Microsoft.PowerShell.Commands.Management</span></span>

<span data-ttu-id="a3dd1-110">**Dll**: Microsoft.PowerShell.Commands.Management.dll</span><span class="sxs-lookup"><span data-stu-id="a3dd1-110">**DLL**: Microsoft.PowerShell.Commands.Management.dll</span></span>

<span data-ttu-id="a3dd1-111">Diese WMI-Befehls Klassen werden von Windows PowerShell implementiert.</span><span class="sxs-lookup"><span data-stu-id="a3dd1-111">These WMI command classes are implemented by Windows PowerShell.</span></span> <span data-ttu-id="a3dd1-112">Diese Klassen sind nur aus Gründen der Vollständigkeit in diesem Software Development Kit (SDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="a3dd1-112">These classes are included in this software development kit (SDK) for completeness only.</span></span> <span data-ttu-id="a3dd1-113">Die Member dieser Klassen können nicht direkt verwendet werden und sollten nicht zum Ableiten anderer Klassen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a3dd1-113">The members of these classes cannot be used directly, nor should they be used to derive other classes.</span></span>



| <span data-ttu-id="a3dd1-114">Klasse</span><span class="sxs-lookup"><span data-stu-id="a3dd1-114">Class</span></span>                   | <span data-ttu-id="a3dd1-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a3dd1-115">Description</span></span>                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3dd1-116">Getwmiobjectcommand</span><span class="sxs-lookup"><span data-stu-id="a3dd1-116">GetWmiObjectCommand</span></span>     | <span data-ttu-id="a3dd1-117">Ruft Instanzen von WMI-Klassen oder Informationen zu den verfügbaren Klassen ab.</span><span class="sxs-lookup"><span data-stu-id="a3dd1-117">Gets instances of WMI classes or information about the available classes.</span></span><br/> <span data-ttu-id="a3dd1-118">Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet " [Get-WMIObject](/previous-versions//dd315295(v=technet.10)) ".</span><span class="sxs-lookup"><span data-stu-id="a3dd1-118">See the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/> |
| <span data-ttu-id="a3dd1-119">Invokewmimethod</span><span class="sxs-lookup"><span data-stu-id="a3dd1-119">InvokeWmiMethod</span></span>         | <span data-ttu-id="a3dd1-120">Ruft WMI-Methoden auf.</span><span class="sxs-lookup"><span data-stu-id="a3dd1-120">Calls WMI methods.</span></span><br/> <span data-ttu-id="a3dd1-121">Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet " [Aufruf-WmiMethod](/previous-versions//dd315300(v=technet.10)) ".</span><span class="sxs-lookup"><span data-stu-id="a3dd1-121">See the [Invoke-WmiMethod](/previous-versions//dd315300(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                                                     |
| <span data-ttu-id="a3dd1-122">Registerwmieventcommand</span><span class="sxs-lookup"><span data-stu-id="a3dd1-122">RegisterWmiEventCommand</span></span> | <span data-ttu-id="a3dd1-123">Abonniert ein WMI-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="a3dd1-123">Subscribes to a WMI event.</span></span><br/> <span data-ttu-id="a3dd1-124">Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet " [Register-wmievent](/previous-versions//dd315242(v=technet.10)) ".</span><span class="sxs-lookup"><span data-stu-id="a3dd1-124">See the [Register-WmiEvent](/previous-versions//dd315242(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                                            |
| <span data-ttu-id="a3dd1-125">Removewmiobject</span><span class="sxs-lookup"><span data-stu-id="a3dd1-125">RemoveWmiObject</span></span>         | <span data-ttu-id="a3dd1-126">Löscht eine Instanz einer vorhandenen WMI-Klasse.</span><span class="sxs-lookup"><span data-stu-id="a3dd1-126">Deletes an instance of an existing WMI class.</span></span><br/> <span data-ttu-id="a3dd1-127">Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet [Remove-WMIObject](/previous-versions//dd347605(v=technet.10)) .</span><span class="sxs-lookup"><span data-stu-id="a3dd1-127">See the [Remove-WmiObject](/previous-versions//dd347605(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                          |
| <span data-ttu-id="a3dd1-128">-Instanz</span><span class="sxs-lookup"><span data-stu-id="a3dd1-128">SetWmiInstance</span></span>          | <span data-ttu-id="a3dd1-129">Erstellt oder aktualisiert eine Instanz einer vorhandenen WMI-Klasse.</span><span class="sxs-lookup"><span data-stu-id="a3dd1-129">Creates or updates an instance of an existing WMI class.</span></span><br/> <span data-ttu-id="a3dd1-130">Beispiele und ausführliche Informationen zu den Parametern finden Sie im Cmdlet " [Set-wmiinstance](/previous-versions//dd315391(v=technet.10)) ".</span><span class="sxs-lookup"><span data-stu-id="a3dd1-130">See the [Set-WmiInstance](/previous-versions//dd315391(v=technet.10)) cmdlet for examples and detailed information about the parameters.</span></span><br/>                |



 

 

