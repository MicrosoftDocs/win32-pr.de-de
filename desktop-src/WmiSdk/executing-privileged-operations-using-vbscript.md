---
description: Wenn Sie die Skript-API für WMI verwenden, können Sie bestimmte Sicherheits Berechtigungen festlegen.
ms.assetid: 65b923d5-5244-498d-9644-d4978fb84f85
ms.tgt_platform: multiple
title: Ausführen privilegierter Vorgänge mit VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13a7cf29aa444856e4da2fc9a73eeda0d8a3ccc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131976"
---
# <a name="executing-privileged-operations-using-vbscript"></a><span data-ttu-id="26fad-103">Ausführen privilegierter Vorgänge mit VBScript</span><span class="sxs-lookup"><span data-stu-id="26fad-103">Executing Privileged Operations Using VBScript</span></span>

<span data-ttu-id="26fad-104">Wenn Sie die Skript-API für WMI verwenden, können Sie bestimmte Sicherheits Berechtigungen festlegen.</span><span class="sxs-lookup"><span data-stu-id="26fad-104">If you use the scripting API for WMI, you can set specific security privileges.</span></span> <span data-ttu-id="26fad-105">Beispielsweise können Sie die Sicherheits Privilegien festlegen, um das Herunterfahren eines Betriebssystems anzufordern oder das Sicherheits Ereignisprotokoll zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="26fad-105">For example, you can set the security privileges to request an operating system shutdown, or to examine the security event log.</span></span> <span data-ttu-id="26fad-106">Weitere Informationen finden Sie unter [Ausführen mit speziellen Berechtigungen](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="26fad-106">For more information, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="26fad-107">Sie müssen nur Berechtigungen festlegen, wenn Sie auf dem Computer auf WMI zugreifen.</span><span class="sxs-lookup"><span data-stu-id="26fad-107">You only need to set privileges when you are accessing WMI on your computer.</span></span> <span data-ttu-id="26fad-108">Wenn Sie auf einen Remote Host zugreifen, werden die Berechtigungen von com RPC automatisch festgelegt.</span><span class="sxs-lookup"><span data-stu-id="26fad-108">When you are accessing a remote host, COM RPC automatically sets the privileges.</span></span> <span data-ttu-id="26fad-109">Informationen zu den erforderlichen Berechtigungen finden Sie in der Dokumentation für die spezifischen WMI-Klassen, auf die Sie zugreifen möchten, z. b. [**Win32- \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span><span class="sxs-lookup"><span data-stu-id="26fad-109">To determine all the required privileges, consult the documentation for the specific WMI classes that you want to access, such as [**Win32\_OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).</span></span> <span data-ttu-id="26fad-110">Weitere Informationen finden Sie unter [wbemprivilege-um](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="26fad-110">For more information, see [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)</span></span>

<span data-ttu-id="26fad-111">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="26fad-111">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="26fad-112">Festlegen einer Berechtigung aus dem Sicherheits \_ Objekt</span><span class="sxs-lookup"><span data-stu-id="26fad-112">Setting a Privilege from the Security\_ Object</span></span>](/windows)
-   [<span data-ttu-id="26fad-113">Festlegen einer Berechtigung als Teil eines Monikers</span><span class="sxs-lookup"><span data-stu-id="26fad-113">Setting a Privilege as Part of a Moniker</span></span>](#setting-a-privilege-as-part-of-a-moniker)
-   [<span data-ttu-id="26fad-114">Aufheben und Zurücksetzen von Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="26fad-114">Revoking and Resetting Privileges</span></span>](#revoking-and-resetting-privileges)
-   [<span data-ttu-id="26fad-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26fad-115">Related topics</span></span>](#related-topics)

## <a name="setting-a-privilege-from-the-security_-object"></a><span data-ttu-id="26fad-116">Festlegen einer Berechtigung aus dem Sicherheits \_ Objekt</span><span class="sxs-lookup"><span data-stu-id="26fad-116">Setting a Privilege from the Security\_ Object</span></span>

<span data-ttu-id="26fad-117">Verwenden Sie das folgende Verfahren, um Sicherheits Privilegien in Visual Basic festzulegen.</span><span class="sxs-lookup"><span data-stu-id="26fad-117">Use the following procedure to set security privileges in Visual Basic.</span></span>

<span data-ttu-id="26fad-118">**So legen Sie Berechtigungen in Visual Basic fest**</span><span class="sxs-lookup"><span data-stu-id="26fad-118">**To set privileges in Visual Basic**</span></span>

1.  <span data-ttu-id="26fad-119">Erstellen Sie ein Objekt vom Typ " [**Swap-Locator**](swbemlocator.md)".</span><span class="sxs-lookup"><span data-stu-id="26fad-119">Create an object of type [**SWbemLocator**](swbemlocator.md).</span></span>
2.  <span data-ttu-id="26fad-120">Fügen Sie dem Objekt " [**Swap. Security \_**](swbemlocator-security-.md) " die neue Berechtigung hinzu.</span><span class="sxs-lookup"><span data-stu-id="26fad-120">Add the new privilege to the [**SWbemLocator.Security\_**](swbemlocator-security-.md) object.</span></span>

    <span data-ttu-id="26fad-121">Das [**Sicherheits \_**](swbemlocator-security-.md) Objekt enthält eine Auflistung von [**Swap**](swbemobjectset.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="26fad-121">The [**Security\_**](swbemlocator-security-.md) object contains an [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span> <span data-ttu-id="26fad-122">Die Objekte in der Gruppe sind " [**Swap Security**](swbemsecurity.md) "-Objekte.</span><span class="sxs-lookup"><span data-stu-id="26fad-122">The objects in the set are [**SWbemSecurity**](swbemsecurity.md) objects.</span></span> <span data-ttu-id="26fad-123">Weitere Informationen finden Sie unter [zugreifen auf eine Sammlung](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="26fad-123">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

3.  <span data-ttu-id="26fad-124">Melden Sie sich bei WMI an, und rufen Sie ein [**Swap Services**](swbemservices.md) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="26fad-124">Log on to WMI and retrieve an [**SWbemServices**](swbemservices.md) object.</span></span>

    <span data-ttu-id="26fad-125">Das Objekt " [**Swap Services**](swbemservices.md) " erbt die Berechtigung, die im vorherigen Schritt festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="26fad-125">The [**SWbemServices**](swbemservices.md) object inherits the privilege that is set in the previous step.</span></span>

<span data-ttu-id="26fad-126">Sie können auch eine Berechtigung mithilfe der Methode " [**Swap. addasstring**](swbemprivilegeset-addasstring.md) " festlegen.</span><span class="sxs-lookup"><span data-stu-id="26fad-126">You can also set a privilege using the [**SWbemPrivilegeSet.AddAsString**](swbemprivilegeset-addasstring.md) method.</span></span>

## <a name="setting-a-privilege-as-part-of-a-moniker"></a><span data-ttu-id="26fad-127">Festlegen einer Berechtigung als Teil eines Monikers</span><span class="sxs-lookup"><span data-stu-id="26fad-127">Setting a Privilege as Part of a Moniker</span></span>

<span data-ttu-id="26fad-128">Sie können eine Berechtigung als Teil eines Monikers festlegen.</span><span class="sxs-lookup"><span data-stu-id="26fad-128">You can set a privilege as part of a moniker.</span></span>

<span data-ttu-id="26fad-129">Im folgenden Beispiel wird gezeigt, wie einem Moniker eine Debugberechtigung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="26fad-129">The following example shows you how to add a debug privilege to a moniker.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



## <a name="revoking-and-resetting-privileges"></a><span data-ttu-id="26fad-130">Aufheben und Zurücksetzen von Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="26fad-130">Revoking and Resetting Privileges</span></span>

<span data-ttu-id="26fad-131">Im folgenden Beispiel wird gezeigt, wie Sie die **sedebug** Privilege-Berechtigung festlegen und die **SeRemoteShutdownPrivilege** -Berechtigung widerrufen.</span><span class="sxs-lookup"><span data-stu-id="26fad-131">The following example shows you how to set the **SeDebugPrivilege** privilege, and revoke the **SeRemoteShutdownPrivilege** privilege.</span></span>


```VB
Set Service = GetObject("winmgmts:{impersonate,(Debug,!RemoteShutdown)}")
```



## <a name="related-topics"></a><span data-ttu-id="26fad-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26fad-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26fad-133">**Berechtigungs Konstanten**</span><span class="sxs-lookup"><span data-stu-id="26fad-133">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> <dt>

[<span data-ttu-id="26fad-134">Ausführen privilegierter Vorgänge</span><span class="sxs-lookup"><span data-stu-id="26fad-134">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> </dl>

 

 
