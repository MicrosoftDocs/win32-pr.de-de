---
description: In Windows 7 implementierte WMI die Win32 \_ optionalfeature-Klasse. Diese Klasse ruft den Status der optionalen Features auf, die auf einem Computer vorhanden sind.
ms.assetid: d756b0c0-b9f4-4b71-9f07-963a0dd5e585
ms.tgt_platform: multiple
title: Abfragen des Status optionaler Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c190b2a2143dae1e22c30b3e5e803908bcb4116
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755336"
---
# <a name="querying-the-status-of-optional-features"></a><span data-ttu-id="6913f-104">Abfragen des Status optionaler Funktionen</span><span class="sxs-lookup"><span data-stu-id="6913f-104">Querying the Status of Optional Features</span></span>

<span data-ttu-id="6913f-105">In Windows 7 implementierte WMI die [**Win32 \_ optionalfeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="6913f-105">In Windows 7, WMI implemented the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class.</span></span> <span data-ttu-id="6913f-106">Diese Klasse ruft den Status der optionalen Features auf, die auf einem Computer vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6913f-106">This class retrieves the status of the optional features that are present on a computer.</span></span>

<span data-ttu-id="6913f-107">Sie können Windows PowerShell-Cmdlets verwenden, um den Status optionaler Funktionen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="6913f-107">You can use Windows PowerShell cmdlets to query the status of optional features.</span></span> <span data-ttu-id="6913f-108">In allen Beispielen in diesem Thema wird das Cmdlet "Get-WmiObject" verwendet.</span><span class="sxs-lookup"><span data-stu-id="6913f-108">All of the examples in this topic use the Get-WmiObject cmdlet.</span></span> <span data-ttu-id="6913f-109">Weitere Informationen finden Sie unter [Get-WMIObject](/previous-versions//dd315295(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="6913f-109">For more information, see [Get-WmiObject](/previous-versions//dd315295(v=technet.10)).</span></span>

<span data-ttu-id="6913f-110">**So rufen Sie alle Instanzen optionaler Features ab, die auf einem Computer vorhanden sind**</span><span class="sxs-lookup"><span data-stu-id="6913f-110">**To retrieve all instances of optional features present on a computer**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="6913f-111">PowerShell</span><span class="sxs-lookup"><span data-stu-id="6913f-111">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject Win32_OptionalFeature</code></pre></td>
    </tr>
    </tbody>
    </table>

    

<span data-ttu-id="6913f-112">**So Fragen Sie eine optionale Funktion durch Angabe des Funktionsnamens ab**</span><span class="sxs-lookup"><span data-stu-id="6913f-112">**To query for an optional feature by specifying the feature name**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="6913f-113">PowerShell</span><span class="sxs-lookup"><span data-stu-id="6913f-113">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from Win32_OptionalFeature where name = &#39;TelnetClient&#39;&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    > [!Note]  
    > <span data-ttu-id="6913f-114">Bei der Eigenschaft **Name** wird die Groß-/Kleinschreibung beachtet</span><span class="sxs-lookup"><span data-stu-id="6913f-114">The **name** property is case-sensitive.</span></span>

     

<span data-ttu-id="6913f-115">**So Fragen Sie optionale Features ab, indem Sie den Installationsstatus angeben**</span><span class="sxs-lookup"><span data-stu-id="6913f-115">**To query for optional features by specifying the install state**</span></span>

-   <span codelanguage="PowerShell"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="6913f-116">PowerShell</span><span class="sxs-lookup"><span data-stu-id="6913f-116">PowerShell</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>Get-WmiObject -query &quot;select * from win32_optionalfeature where installstate= 1&quot;</code></pre></td>
    </tr>
    </tbody>
    </table>

    

    <span data-ttu-id="6913f-117">Weitere Informationen zu den möglichen Werten für die **InstallState** -Eigenschaft finden Sie unter [**Win32 \_ optionalfeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).</span><span class="sxs-lookup"><span data-stu-id="6913f-117">For more information about the possible values for the **InstallState** property, see [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6913f-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6913f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6913f-119">**Win32- \_ optionalfeature**</span><span class="sxs-lookup"><span data-stu-id="6913f-119">**Win32\_OptionalFeature**</span></span>](/windows/desktop/CIMWin32Prov/win32-optionalfeature)
</dt> </dl>

 

 
