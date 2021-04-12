---
title: einfacher sessionstatechangetype-Typ
description: Definiert Werte für die Art der Sitzungs Zustandsänderung des Terminal Servers, die Sie verwenden können, um einen Task zu starten.
ms.assetid: 56e19ec0-ea6c-4434-ab9d-a1069108920f
keywords:
- sessionstatechangetype-Typ "Simple" Taskplaner
topic_type:
- apiref
api_name:
- sessionStateChangeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a77fb563b59ccd8d63d38c6c85f16ff74ac404b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478378"
---
# <a name="sessionstatechangetype-simple-type"></a><span data-ttu-id="99f86-104">einfacher sessionstatechangetype-Typ</span><span class="sxs-lookup"><span data-stu-id="99f86-104">sessionStateChangeType Simple Type</span></span>

<span data-ttu-id="99f86-105">Definiert Werte für die Art der Sitzungs Zustandsänderung des Terminal Servers, die Sie verwenden können, um einen Task zu starten.</span><span class="sxs-lookup"><span data-stu-id="99f86-105">Defines values for the kind of Terminal Server session state change you can use to trigger a task to start.</span></span>

``` syntax
<xs:simpleType name="sessionStateChangeType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="ConsoleConnect"
         />
        <xs:enumeration
            value="ConsoleDisconnect"
         />
        <xs:enumeration
            value="RemoteConnect"
         />
        <xs:enumeration
            value="RemoteDisconnect"
         />
        <xs:enumeration
            value="SessionLock"
         />
        <xs:enumeration
            value="SessionUnlock"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="99f86-106">Enumerationswerte</span><span class="sxs-lookup"><span data-stu-id="99f86-106">Enumeration values</span></span>

<span data-ttu-id="99f86-107">Der einfache Typ **sessionstatechangetype** definiert die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="99f86-107">The **sessionStateChangeType** simple type defines the following values.</span></span>



| <span data-ttu-id="99f86-108">Wert</span><span class="sxs-lookup"><span data-stu-id="99f86-108">Value</span></span>             | <span data-ttu-id="99f86-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99f86-109">Description</span></span>                                                                                                                                                                                       |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99f86-110">Consoleconnetct</span><span class="sxs-lookup"><span data-stu-id="99f86-110">ConsoleConnect</span></span>    | <span data-ttu-id="99f86-111">Statusänderung der Terminal Server-Konsolen Verbindung.</span><span class="sxs-lookup"><span data-stu-id="99f86-111">Terminal Server console connection state change.</span></span> <span data-ttu-id="99f86-112">Wenn Sie z. b. eine Verbindung mit einer Benutzersitzung auf dem lokalen Computer herstellen, indem Sie die Benutzer auf dem Computer wechseln.</span><span class="sxs-lookup"><span data-stu-id="99f86-112">For example, when you connect to a user session on the local computer by switching users on the computer.</span></span> <br/>                            |
| <span data-ttu-id="99f86-113">Consoledisconnect</span><span class="sxs-lookup"><span data-stu-id="99f86-113">ConsoleDisconnect</span></span> | <span data-ttu-id="99f86-114">Statusänderung der Terminal Server Konsole wird getrennt.</span><span class="sxs-lookup"><span data-stu-id="99f86-114">Terminal Server console disconnection state change.</span></span> <span data-ttu-id="99f86-115">Wenn Sie z. b. eine Verbindung mit einer Benutzersitzung auf dem lokalen Computer trennen, indem Sie die Benutzer auf dem Computer wechseln.</span><span class="sxs-lookup"><span data-stu-id="99f86-115">For example, when you disconnect to a user session on the local computer by switching users on the computer.</span></span> <br/>                      |
| <span data-ttu-id="99f86-116">Verbindung "</span><span class="sxs-lookup"><span data-stu-id="99f86-116">RemoteConnect</span></span>     | <span data-ttu-id="99f86-117">Statusänderung für Terminal Server-Remote Verbindung.</span><span class="sxs-lookup"><span data-stu-id="99f86-117">Terminal Server remote connection state change.</span></span> <span data-ttu-id="99f86-118">Dies ist beispielsweise der Fall, wenn ein Benutzer mithilfe des Remotedesktopverbindung Programms von einem Remote Computer aus eine Verbindung mit einer Benutzersitzung herstellt.</span><span class="sxs-lookup"><span data-stu-id="99f86-118">For example, when a user connects to a user session by using the Remote Desktop Connection program from a remote computer.</span></span> <br/>            |
| <span data-ttu-id="99f86-119">Remotedisconnect</span><span class="sxs-lookup"><span data-stu-id="99f86-119">RemoteDisconnect</span></span>  | <span data-ttu-id="99f86-120">Statusänderung des Terminal Server-Remote Verbindungs Wechsels.</span><span class="sxs-lookup"><span data-stu-id="99f86-120">Terminal Server remote disconnection state change.</span></span> <span data-ttu-id="99f86-121">Dies ist beispielsweise der Fall, wenn ein Benutzer die Verbindung mit einer Benutzersitzung trennt, während das Remotedesktopverbindung Programm von einem Remote Computer aus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="99f86-121">For example, when a user disconnects from a user session while using the Remote Desktop Connection program from a remote computer.</span></span> <br/> |
| <span data-ttu-id="99f86-122">Sessionlock</span><span class="sxs-lookup"><span data-stu-id="99f86-122">SessionLock</span></span>       | <span data-ttu-id="99f86-123">Statusänderung für Terminal Server Sitzung gesperrt.</span><span class="sxs-lookup"><span data-stu-id="99f86-123">Terminal Server session locked state change.</span></span> <span data-ttu-id="99f86-124">Diese Statusänderung bewirkt beispielsweise, dass die Aufgabe ausgeführt wird, wenn der Computer gesperrt wird.</span><span class="sxs-lookup"><span data-stu-id="99f86-124">For example, this state change causes the task to run when the computer is locked.</span></span> <br/>                                                       |
| <span data-ttu-id="99f86-125">Sessionunlock</span><span class="sxs-lookup"><span data-stu-id="99f86-125">SessionUnlock</span></span>     | <span data-ttu-id="99f86-126">Die Statusänderung der Terminal Server Sitzung wurde aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="99f86-126">Terminal Server session unlocked state change.</span></span> <span data-ttu-id="99f86-127">Diese Statusänderung bewirkt beispielsweise, dass die Aufgabe ausgeführt wird, wenn der Computer entsperrt wird.</span><span class="sxs-lookup"><span data-stu-id="99f86-127">For example, this state change causes the task to run when the computer is unlocked.</span></span><br/>                                                    |



## <a name="requirements"></a><span data-ttu-id="99f86-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99f86-128">Requirements</span></span>



| <span data-ttu-id="99f86-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99f86-129">Requirement</span></span> | <span data-ttu-id="99f86-130">Wert</span><span class="sxs-lookup"><span data-stu-id="99f86-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="99f86-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="99f86-131">Minimum supported client</span></span><br/> | <span data-ttu-id="99f86-132">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99f86-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="99f86-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="99f86-133">Minimum supported server</span></span><br/> | <span data-ttu-id="99f86-134">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="99f86-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





