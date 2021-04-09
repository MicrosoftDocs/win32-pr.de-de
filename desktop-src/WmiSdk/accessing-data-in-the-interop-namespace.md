---
description: Mithilfe von Zuordnungs Anbietern können Windows-Verwaltungsinstrumentation (WMI)-Clients Profile und zugehörige Klassen Instanzen aus unterschiedlichen Namespaces durchlaufen und abrufen.
ms.assetid: 00c654d1-a5de-40c5-a190-99382949486a
ms.tgt_platform: multiple
title: Zugreifen auf Daten im Interop-Namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a217a7a44651b1a6c94476b53193eedac7f0d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960618"
---
# <a name="accessing-data-in-the-interop-namespace"></a><span data-ttu-id="f1c5d-103">Zugreifen auf Daten im Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f1c5d-103">Accessing Data in the Interop Namespace</span></span>

<span data-ttu-id="f1c5d-104">Mithilfe von Zuordnungs Anbietern können Windows-Verwaltungsinstrumentation (WMI)-Clients Profile und zugehörige Klassen Instanzen aus unterschiedlichen Namespaces durchlaufen und abrufen.</span><span class="sxs-lookup"><span data-stu-id="f1c5d-104">Association providers enable Windows Management Instrumentation (WMI) clients to traverse and retrieve profiles and associated class instances from different namespaces.</span></span>

<span data-ttu-id="f1c5d-105">Zuordnungs Anbieter und-Klassen befinden sich im \\ \\ \\ Namespace "root Interop".</span><span class="sxs-lookup"><span data-stu-id="f1c5d-105">Association providers and classes reside in the \\\\root\\interop namespace.</span></span> <span data-ttu-id="f1c5d-106">Weitere Informationen finden Sie unter [Cross Namespace Association Traversal](cross-namespace-association-traversal.md) und [Writing a Association Provider](writing-an-association-provider-for-interop.md).</span><span class="sxs-lookup"><span data-stu-id="f1c5d-106">For more information, see [Cross Namespace Association Traversal](cross-namespace-association-traversal.md) and [Writing an Association Provider](writing-an-association-provider-for-interop.md).</span></span>

<span data-ttu-id="f1c5d-107">Zuordnungs Anbieter machen Standardprofile wie z. b. ein Power Profile verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f1c5d-107">Association providers expose standard profiles, like a power profile.</span></span> <span data-ttu-id="f1c5d-108">In den folgenden Beispielen wird das Power Profile verwendet, um zu veranschaulichen, wie Sie Daten mithilfe des Interop-Namespace ermitteln und darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="f1c5d-108">The following examples use the power profile to illustrate how to discover and access data through the interop namespace.</span></span>

<span data-ttu-id="f1c5d-109">Windows PowerShell bietet einen einfachen Mechanismus zum Durchlaufen der entsprechenden Zuordnung, zum Abrufen eines Geräte Profils und zum Aufrufen einer Methode.</span><span class="sxs-lookup"><span data-stu-id="f1c5d-109">Windows PowerShell provides a simple mechanism to traverse through the appropriate association, retrieve a device profile, and call a method.</span></span>

## <a name="enumerating-profiles-in-the-rootinterop-namespace"></a><span data-ttu-id="f1c5d-110">Auflisten von Profilen im Root/Interop-Namespace</span><span class="sxs-lookup"><span data-stu-id="f1c5d-110">Enumerating profiles in the root/interop namespace</span></span>

<span data-ttu-id="f1c5d-111">Mit dem folgenden Windows PowerShell-Befehl werden die von der[DMTF](https://www.dmtf.org/standards/wsman)(verteilte Management Task Force) unterstützten Profile auf einem Windows 7-Computer aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="f1c5d-111">The following Windows PowerShell command enumerates the Distributed Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman))-supported profiles on a Windows 7 computer:</span></span>


```PowerShell
Get-WmiObject CIM_RegisteredProfile  -namespace root\interop
```



## <a name="retrieving-instances-of-a-specific-device-profile"></a><span data-ttu-id="f1c5d-112">Abrufen von Instanzen eines bestimmten Geräte Profils</span><span class="sxs-lookup"><span data-stu-id="f1c5d-112">Retrieving instances of a specific device profile</span></span>

<span data-ttu-id="f1c5d-113">Mit dem folgenden Windows PowerShell-Befehl werden alle Instanzen eines angegebenen Profils über [**CIM \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="f1c5d-113">The following Windows PowerShell command returns all instances of a specified profile through [**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85)):</span></span>


```PowerShell
Get-WmiObject -namespace root\interop -query "Associators of {CIM_RegisteredProfile.InstanceID='Power Supply'}"
```



## <a name="assigning-the-power-profile-to-a-variable"></a><span data-ttu-id="f1c5d-114">Zuweisen des Power Profile zu einer Variablen</span><span class="sxs-lookup"><span data-stu-id="f1c5d-114">Assigning the power profile to a variable</span></span>

<span data-ttu-id="f1c5d-115">Der folgende Windows PowerShell-Befehl weist die Power profile-Instanz einer Variablen zu:</span><span class="sxs-lookup"><span data-stu-id="f1c5d-115">The following Windows PowerShell command assigns the power profile instance to a variable:</span></span>


```PowerShell
$pplan = Get-WmiObject -query "Select * from Win32_PowerPlan" -Namespace root\cimv2\power
```



## <a name="enumerating-the-power-plans-on-a-computer"></a><span data-ttu-id="f1c5d-116">Auflisten von Energie Sparplänen auf einem Computer</span><span class="sxs-lookup"><span data-stu-id="f1c5d-116">Enumerating the power plans on a computer</span></span>

<span data-ttu-id="f1c5d-117">Der folgende Windows PowerShell-Befehl listet die verfügbaren Energieprofil Pläne auf:</span><span class="sxs-lookup"><span data-stu-id="f1c5d-117">The following Windows PowerShell command enumerates the available power profile plans:</span></span>


```PowerShell
$pplan
```



## <a name="calling-a-method"></a><span data-ttu-id="f1c5d-118">Aufrufen einer Methode</span><span class="sxs-lookup"><span data-stu-id="f1c5d-118">Calling a method</span></span>

<span data-ttu-id="f1c5d-119">Der folgende Windows PowerShell-Befehl ruft die [**Aktivierungs**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) Methode für den Energie Sparplan auf:</span><span class="sxs-lookup"><span data-stu-id="f1c5d-119">The following Windows PowerShell command calls the [**Activate**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) method for the power plan:</span></span>


```PowerShell
$pplan[2].Activate()
```



## <a name="related-topics"></a><span data-ttu-id="f1c5d-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f1c5d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1c5d-121">Cross-Namespace Association Traversal</span><span class="sxs-lookup"><span data-stu-id="f1c5d-121">Cross Namespace Association Traversal</span></span>](cross-namespace-association-traversal.md)
</dt> <dt>

[<span data-ttu-id="f1c5d-122">Schreiben eines Zuordnungs Anbieters</span><span class="sxs-lookup"><span data-stu-id="f1c5d-122">Writing an Association Provider</span></span>](writing-an-association-provider-for-interop.md)
</dt> <dt>

<span data-ttu-id="f1c5d-123">[**CIM- \_ registeredprofile**](/previous-versions//ee309375(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1c5d-123">[**CIM\_RegisteredProfile**](/previous-versions//ee309375(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="f1c5d-124">[**Win32- \_ PowerPlan**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f1c5d-124">[**Win32\_PowerPlan**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))</span></span>
</dt> </dl>

 

 
